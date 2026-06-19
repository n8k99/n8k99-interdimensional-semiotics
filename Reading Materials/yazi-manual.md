# Yazi Manual

*Snapshot of [yazi-rs.github.io](https://yazi-rs.github.io) docs at commit `59aae61`, built 2026-05-12.*

*This is a single-file concatenation of the official docs for offline reading. Section order follows the upstream sidebar.*

## Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Configuration](#configuration)
- [yazi.toml](#yazitoml)
- [keymap.toml](#keymaptoml)
- [theme.toml](#themetoml)
- [vfs.toml](#vfstoml)
- [Image Preview](#image-preview)
- [Plugins (BETA)](#plugins-beta)
- [Types](#types)
- [Layout](#layout)
- [Context](#context)
- [Runtime](#runtime)
- [Utils](#utils)
- [Builtins](#builtins)
- [Aliases](#aliases)
- [Flavors (BETA)](#flavors-beta)
- [CLI](#cli)
- [DDS](#dds)
- [Tips](#tips)
- [Resources](#resources)
- [Terminology](#terminology)
- [Frequently Asked Questions](#frequently-asked-questions)

---

## Installation

To use Yazi, you must have the following prerequisites installed:

- [`file`](https://github.com/file/file) (for file type detection)

Yazi can be **optionally** extended with other command-line tools to enable additional features.

- [nerd-fonts](https://www.nerdfonts.com/) ([_recommended_](/docs/faq#dont-like-nerd-fonts))
- [`ffmpeg`](https://www.ffmpeg.org/) (for video thumbnails)
- [7-Zip](https://www.7-zip.org/) (for archive extraction and preview, requires non-standalone version)
- [`jq`](https://jqlang.github.io/jq/) (for JSON preview)
- [`poppler`](https://poppler.freedesktop.org/) (for PDF preview)
- [`fd`](https://github.com/sharkdp/fd) (for file searching)
- [`rg`](https://github.com/BurntSushi/ripgrep) (for file content searching)
- [`fzf`](https://github.com/junegunn/fzf) (for quick file subtree navigation, >= 0.53.0)
- [`zoxide`](https://github.com/ajeetdsouza/zoxide) (for historical directories navigation, requires `fzf`)
- [`resvg`](https://github.com/linebender/resvg) (for SVG preview)
- [ImageMagick](https://imagemagick.org/) (for Font, HEIC, and JPEG XL preview, >= 7.1.1)
- [`xclip`](https://github.com/astrand/xclip) / [`wl-clipboard`](https://github.com/bugaevc/wl-clipboard) / [`xsel`](https://github.com/kfish/xsel) (for Linux clipboard support)

Upgrade these dependencies to their newest version if certain functionality is not working as expected.

### Packaging status {#packaging}

Most packages on this page are maintained by the community, and they **_may not always be the latest_**. Please check their versions before installation:

<a alt="Yazi packaging status" href="https://repology.org/project/yazi/versions">
	<img alt="Yazi packaging status" height="785" src="https://repology.org/badge/vertical-allrepos/yazi.svg" />
</a>

### Arch Linux {#arch}

```sh
sudo pacman -S yazi ffmpeg 7zip jq poppler fd ripgrep fzf zoxide resvg imagemagick
```

If you want to use the latest Git version, you can install it from [AUR](https://aur.archlinux.org/packages/yazi-git/) or [Arch Linux CN](https://github.com/archlinuxcn/repo/):

```sh
paru -S yazi-git ffmpeg 7zip jq poppler fd ripgrep fzf zoxide resvg imagemagick
```

You can also install the [official nightly release binary](https://github.com/sxyazi/yazi/releases/tag/nightly) from [AUR](https://aur.archlinux.org/packages/yazi-nightly-bin),
which is built from the latest code within the past 6 hours:

```sh
paru -S yazi-nightly-bin ffmpeg 7zip jq poppler fd ripgrep fzf zoxide resvg imagemagick
```

### Nix {#nix}

A [Nix package](https://search.nixos.org/packages?channel=unstable&show=yazi) for Yazi is available.

```sh
## NixOS:
nix-env -iA nixos.yazi

## Not NixOS:
nix-env -iA nixpkgs.yazi
```

Or add the following to your configuration:

```nix
## configuration.nix
environment.systemPackages = with pkgs; [
	(yazi.override {
		_7zz = _7zz-rar;  # Support for RAR extraction
	})
];
```

You can also manage Yazi's configuration using [home-manager](https://nix-community.github.io/home-manager/options.xhtml#opt-programs.yazi.enable), here is a configuration template example:

<details>
  <summary>Demonstrate configuring Yazi with home-manager</summary>

```nix
{pkgs, ...}: let
	yazi-plugins = pkgs.fetchFromGitHub {
		owner = "yazi-rs";
		repo = "plugins";
		rev = "...";
		hash = "sha256-...";
	};
in {
	programs.yazi = {
		enable = true;
		enableZshIntegration = true;
		shellWrapperName = "y";

		settings = {
			mgr = {
				show_hidden = true;
			};
			preview = {
				max_width = 1000;
				max_height = 1000;
			};
		};

		plugins = {
			chmod = "${yazi-plugins}/chmod.yazi";
			full-border = "${yazi-plugins}/full-border.yazi";
			toggle-pane = "${yazi-plugins}/toggle-pane.yazi";
			starship = pkgs.fetchFromGitHub {
				owner = "Rolv-Apneseth";
				repo = "starship.yazi";
				rev = "...";
				sha256 = "sha256-...";
			};
		};

		initLua = ''
			require("full-border"):setup()
			require("starship"):setup()
		'';

		keymap = {
			mgr.prepend_keymap = [
				{
					on = "T";
					run = "plugin toggle-pane max-preview";
					desc = "Maximize or restore the preview pane";
				}
				{
					on = ["c" "m"];
					run = "plugin chmod";
					desc = "Chmod on selected files";
				}
			];
		};
	};
}
```

</details>

### Nix flakes {#flakes}

The upstream repository provides a flake so that Nix users can easily keep up with the bleeding edge. A basic `flake.nix` setup to get you started:

```nix
{
	inputs = {
		nixpkgs.url = "github:NixOS/nixpkgs/nixos-23.11";

		home-manager = {
			url = "github:nix-community/home-manager/release-23.11";
			inputs.nixpkgs.follows = "nixpkgs";
		};

		yazi.url = "github:sxyazi/yazi";
	};

	outputs = { nixpkgs, home-manager, yazi, ... }: {
		# To install Yazi system-wide:
		nixosConfigurations = {
			nixos = nixpkgs.lib.nixosSystem {
				modules = [
					({ pkgs, ... }: {
						environment.systemPackages = [
							(yazi.packages.${pkgs.system}.default.override {
								_7zz = pkgs._7zz-rar;  # Support for RAR extraction
							})
						];
					})
				];
			};
		};

		# To install it for a specific user:
		homeConfigurations = {
			"alice@nixos" = home-manager.lib.homeManagerConfiguration {
				pkgs = nixpkgs.legacyPackages.x86_64-linux;
				modules = [
					({ pkgs, ... }: {
						home.packages = [
							(yazi.packages.${pkgs.system}.default.override {
								_7zz = pkgs._7zz-rar;  # Support for RAR extraction
							})
						];
					})
				];
			};
		};
	};
}
```

If you want to override the package inside nixpkgs with the one from the flake, you can use overlays:

```nix
nixpkgs.overlays = [ yazi.overlays.default ];
```

A module is also available for both NixOS and home-manager:

```nix
programs.yazi = {
	enable = true;
	# You can omit this if you use overlays
	package = yazi.packages.${pkgs.system}.default.override {
		_7zz = pkgs._7zz-rar;  # Support for RAR extraction
	};
};
```

#### Cache

Pre-built artifacts are served at https://yazi.cachix.org, so that Nix users don't have to build Yazi on their machine.
You can make use of it by adding the following options to `nix.settings`, either in your NixOS or home-manager configuration:

```nix
extra-substituters = [ "https://yazi.cachix.org" ];
extra-trusted-public-keys = [ "yazi.cachix.org-1:Dcdz63NZKfvUCbDGngQDAZq6kOroIrFoyO064uvLh8k=" ];
```

Note that the cache will only be applied _after_ you rebuild your Nix config. If you want to ensure that the cache gets applied right away, add the options above to your flake's `nixConfig` attribute.

If you're having any problems, refer to this [entry](https://docs.cachix.org/faq#why-is-nix-not-picking-up-on-any-of-the-pre-built-artifacts) from Cachix's FAQ.

### Homebrew {#homebrew}

First, make sure that Homebrew is fully up-to-date with `brew update`.

Then you can install Yazi (and the optional dependencies):

```sh
brew install yazi ffmpeg-full sevenzip jq poppler fd ripgrep fzf zoxide resvg imagemagick-full font-symbols-only-nerd-font
brew link ffmpeg-full imagemagick-full -f --overwrite
```

If you prefer to use the most recent code, use the `--HEAD` flag when installing Yazi.

```sh
brew install yazi --HEAD
```

### MacPorts {#macports}

```bash
sudo port install yazi ffmpeg 7zip jq poppler fd ripgrep fzf zoxide ImageMagick
```

### Solus Linux

```sh
sudo eopkg install yazi ffmpeg p7zip jq poppler fd ripgrep fzf zoxide resvg imagemagick
```

### Void Linux

```sh
sudo xbps-install -S yazi ffmpeg 7zip jq poppler fd ripgrep fzf zoxide resvg ImageMagick
```

### NetBSD {#netbsd}

```sh
pkgin install yazi ffmpeg7 p7zip jq poppler fd ripgrep fzf zoxide ImageMagick
```

### Windows {#windows}

Yazi relies on `file(1)` to detect the mime-type of the file, and the easiest and most reliable way to get it on Windows is to install Git for Windows and use the `file.exe` that comes with it.

1. Install Git for Windows by running [the official installer](https://git-scm.com/download/win), or through your package manager of choice.
2. To allow Yazi to use `file(1)`, add `<Git_Installed_Directory>\usr\bin\file.exe` to your `YAZI_FILE_ONE` environment variable, which differs depending on how you installed Git:
   - If you installed Git with the installer, it would be `C:\Program Files\Git\usr\bin\file.exe`.
   - If you installed Git with Scoop, it would be `C:\Users\<Username>\scoop\apps\git\current\usr\bin\file.exe`.
3. Restart your terminal.

This is **the ONLY way we recommend**. We do not recommend installing `file` via Scoop or Chocolatey, since they cannot handle Unicode filenames (such as `oliver-sjöström.jpg`) properly and lack some required parameters.

Most users already have Git installed, and Yazi is also hosted via Git, so this usually isn't an issue. But if you really don't have/want to install it, the [`mime-ext.yazi`](https://github.com/yazi-rs/plugins/tree/main/mime-ext.yazi) plugin can help, as it uses an extension database instead of relying on the `file(1)` binary.

#### Install with Scoop

```sh
scoop install yazi
## Install the optional dependencies (recommended):
scoop install ffmpeg 7zip jq poppler fd ripgrep fzf zoxide resvg imagemagick
```

#### Install with WinGet

```sh
winget install sxyazi.yazi
## Install the optional dependencies (recommended):
winget install Gyan.FFmpeg 7zip.7zip jqlang.jq oschwartz10612.Poppler sharkdp.fd BurntSushi.ripgrep.MSVC junegunn.fzf ajeetdsouza.zoxide ImageMagick.ImageMagick
```

resvg is not yet on WinGet, install with Scoop or manually download from [resvg](https://github.com/linebender/resvg/releases).

### Debian based Linux {#debian}

:::info
This uses an [unofficial deb repository](https://github.com/dariogriffo/yazi-debian) maintained by [Dario Griffo](https://github.com/dariogriffo).
:::

```sh
curl -sS https://debian.griffo.io/EA0F721D231FDD3A0A17B9AC7808B4DD62C41256.asc | gpg --dearmor --yes -o /etc/apt/trusted.gpg.d/debian.griffo.io.gpg
echo "deb https://debian.griffo.io/apt $(lsb_release -sc 2>/dev/null) main" | sudo tee /etc/apt/sources.list.d/debian.griffo.io.list
sudo apt update
sudo apt install yazi
```

This will install Yazi and its dependencies. Note that, some deps are pretty outdated and might cause Yazi to malfunction, in that case you'll need to build them from the latest source manually.

### Fedora/Centos Stream 9+/RHEL 9+ {#copr}

:::info
This uses an [unofficial COPR repository](https://copr.fedorainfracloud.org/coprs/lihaohong/yazi) maintained by [Peter Li](https://github.com/lihaohong6).
:::

```sh
dnf copr enable lihaohong/yazi
dnf install yazi
```

`dnf` will install recommended dependencies automatically. To install only Yazi:

```sh
dnf copr enable lihaohong/yazi
dnf install yazi --setopt=install_weak_deps=False
```

If `dnf` complains about "No such command: copr", run `dnf install dnf-plugins-core` and then rerun the commands above.

### Snapcraft

<a href="https://snapcraft.io/yazi">
	<img height="40" alt="Install Yazi from Snapcraft" src="https://snapcraft.io/en/dark/install.svg" />
</a>

You can install Yazi from the [Snap Store](https://snapcraft.io/yazi) with:

```sh
sudo snap install yazi --classic
```

If you want to keep up with the bleeding edge, get the nightly version with:

```sh
sudo snap install yazi --classic --edge
```

### Flatpak

:::warning
The Flatpak edition comes with many limitations due to sandboxing - see its [README](https://github.com/flathub/io.github.sxyazi.yazi) for details.

Power users are recommended to transition to an alternative installation to avoid unexpected breakages.
:::

<a href="https://flathub.org/apps/io.github.sxyazi.yazi">
	<img height="40" alt="Install Yazi from Flathub" src="https://flathub.org/api/badge?locale=en" />
</a>

After [installation](https://flathub.org/apps/io.github.sxyazi.yazi), you can run Yazi in the terminal with:

```sh
flatpak run io.github.sxyazi.yazi
```

You may want to create a shell alias:

```sh
alias yazi="flatpak run io.github.sxyazi.yazi"
```

See the Flatpak edition's [README](https://github.com/flathub/io.github.sxyazi.yazi) for more information.

### PyPI {#pypi}

:::info
This uses an [unofficial PyPI package](https://github.com/Bing-su/pip-binary-factory) maintained by [Dowon](https://github.com/Bing-su).
:::

```sh
pipx install yazi-bin
## Or
uv tool install yazi-bin
```

### AOSC OS {#aosc}

```sh
sudo oma install yazi ffmpeg p7zip jq poppler fd ripgrep fzf zoxide imagemagick
```

### x-cmd {#x-cmd}

```sh
x env use yazi ffmpeg 7zz jq fd rg fzf zoxide magick
```

### Official binaries {#binaries}

You can download the latest official binaries from GitHub Releases: https://github.com/sxyazi/yazi/releases

On this page, we offer GNU/Musl builds to meet the needs of different users.

This page also includes a [nightly release](https://github.com/sxyazi/yazi/releases/tag/nightly), which is built from the latest code within the past 6 hours.

### crates.io {#crates}

Yazi is available on [crates.io](https://crates.io/). Due to [Cargo's limitations](https://github.com/rust-lang/cargo/issues/11599), they must be installed via [`yazi-build`](https://crates.io/crates/yazi-build).

To install Yazi, setup the latest stable Rust toolchain via [rustup](https://rustup.rs/):

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update
```

Now you can install `yazi-build` via `cargo`, which will in turn install `yazi-fm` and `yazi-cli`:

```sh
cargo install --force yazi-build
```

Or install the latest Git version of Yazi:

```sh
cargo install --force --git https://github.com/sxyazi/yazi.git yazi-build
```

If it fails to build, please check if `make` and `gcc` is installed on your system.

### Cargo Binstall {#cargo-binstall}

To install Yazi's binary release with [`cargo-binstall`](https://github.com/cargo-bins/cargo-binstall):

```sh
cargo binstall yazi-fm
```

### Build from source {#source}

Setup the latest stable Rust toolchain via [rustup](https://rustup.rs/):

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update
```

Clone the repository and build Yazi:

<Tabs>
  <TabItem value="non-windows" label="non-Windows" default>

```sh
git clone https://github.com/sxyazi/yazi.git
cd yazi
cargo build --release --locked
```

  </TabItem>
  <TabItem value="windows" label="Windows">

```sh
git clone https://github.com/sxyazi/yazi.git
cd yazi
cargo build --profile release-windows --locked
```

  </TabItem>
</Tabs>

Then, add `yazi` and `ya` to your `$PATH`:

<Tabs>
  <TabItem value="non-windows" label="non-Windows" default>

```sh
mv target/release/yazi target/release/ya /usr/local/bin/
```

  </TabItem>
  <TabItem value="windows" label="Windows">

```sh
move target\release-windows\yazi.exe "%ProgramFiles%\yazi.exe"
move target\release-windows\ya.exe "%ProgramFiles%\ya.exe"
```

  </TabItem>
</Tabs>

If it fails to build, please check if `make` and `gcc` is installed on your system.

### Build from source in debug mode {#debug}

:::warning
Building Yazi in debug mode is for debugging purposes only, as it can speed up the build and provide more stack trace information.

It should not be used for daily purposes, as debug mode significantly reduces performance!
:::

Setup the latest stable Rust toolchain via [rustup](https://rustup.rs/):

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update
```

Clone the repository and build Yazi:

```sh
git clone https://github.com/sxyazi/yazi.git
cd yazi
cargo build --locked
```

Then, run `yazi` in debug mode:

<Tabs>
  <TabItem value="unix" label="Unix-like" default>

```sh
YAZI_LOG=debug RUST_BACKTRACE=1 ./target/debug/yazi
```

  </TabItem>

  <TabItem value="powershell" label="PowerShell">

```powershell
$env:YAZI_LOG = "debug"; $env:RUST_BACKTRACE = 1; .\target\debug\yazi.exe
```

  </TabItem>
</Tabs>

If it fails to build, please check if `make` and `gcc` is installed on your system.

---

## Quick Start

Once you've [installed Yazi](/docs/installation), start the program with:

```sh
yazi
```

Press <kbd>q</kbd> to quit, <kbd>F1</kbd> or <kbd>~</kbd> to open the help menu.

### Shell wrapper

We suggest using this `y` shell wrapper that provides the ability to change the current working directory when exiting Yazi.

<Tabs>
  <TabItem value="bash-zsh" label="Bash / Zsh" default>

```bash
function y() {
	local tmp="$(mktemp -t "yazi-cwd.XXXXXX")" cwd
	command yazi "$@" --cwd-file="$tmp"
	IFS= read -r -d '' cwd < "$tmp"
	[ "$cwd" != "$PWD" ] && [ -d "$cwd" ] && builtin cd -- "$cwd"
	command rm -f -- "$tmp"
}
```

  </TabItem>
  <TabItem value="fish" label="Fish">

```sh
function y
	set tmp (mktemp -t "yazi-cwd.XXXXXX")
	command yazi $argv --cwd-file="$tmp"
	if read -z cwd < "$tmp"; and [ "$cwd" != "$PWD" ]; and test -d "$cwd"
		builtin cd -- "$cwd"
	end
	command rm -f -- "$tmp"
end
```

  </TabItem>
  <TabItem value="nushell" label="Nushell">

```sh
def --env y [...args] {
	let tmp = (mktemp -t "yazi-cwd.XXXXXX")
	^yazi ...$args --cwd-file $tmp
	let cwd = (open $tmp)
	if $cwd != $env.PWD and ($cwd | path exists) {
		cd $cwd
	}
	rm -fp $tmp
}
```

  </TabItem>
  <TabItem value="posix" label="POSIX">

```sh
y() {
	set -- "$@" --cwd-file "$(mktemp -t yazi-cwd.XXXXXX)"
	command yazi "$@"
	shift $(($# - 1))
	set -- "$(command cat < "$1"; printf .; command rm -f -- "$1")"
	set -- "${1%.}"
	[ "$1" != "$PWD" ] && [ -d "$1" ] && command cd -- "$1"
}
```

  </TabItem>
  <TabItem value="elvish" label="Elvish">

```elvish
edit:add-var y~ {|@argv|
	use str
	use os
	use file
	var tmp = (os:temp-file)
	e:yazi $@argv --cwd-file=$tmp[name]
	var cwd = (slurp < $tmp)
	file:close $tmp
	os:remove $tmp[name]
 	if (and (not-eq $cwd $pwd) (os:is-dir $cwd)) {
 		cd $cwd
 	}
}
```

  </TabItem>
  <TabItem value="powershell" label="PowerShell">

```powershell
function y {
	$tmp = (New-TemporaryFile).FullName
	yazi.exe @args --cwd-file="$tmp"
	$cwd = Get-Content -Path $tmp -Encoding UTF8
	if ($cwd -and $cwd -ne $PWD.Path -and (Test-Path -LiteralPath $cwd -PathType Container)) {
		Set-Location -LiteralPath (Resolve-Path -LiteralPath $cwd).Path
	}
	Remove-Item -Path $tmp
}
```

  </TabItem>
  <TabItem value="command-prompt" label="Command Prompt">

Create the file `y.cmd` and place it in your `%PATH%`.

```cmd
@echo off

set tmpfile=%TEMP%\yazi-cwd.%random%

yazi.exe %* --cwd-file="%tmpfile%"

:: If the file does not exist, then exit
if not exist "%tmpfile%" exit /b 0

:: If the file exist, then read the content and change the directory
set /p cwd=<"%tmpfile%"
if not "%cwd%"=="" if exist "%cwd%\" (
	cd /d "%cwd%"
)
del "%tmpfile%"
```

  </TabItem>
  <TabItem value="xonsh" label="Xonsh">

```xonsh
def _y(args):
	tmp = $(mktemp -t "yazi-cwd.XXXXXX")
	args.append(f"--cwd-file={tmp}")
	$[yazi @(args)]
	with open(tmp) as f:
		cwd = f.read()
	import os
	if cwd != $PWD and os.path.isdir(cwd):
		cd @(cwd)
	rm -f -- @(tmp)

aliases["y"] = _y
```

  </TabItem>
</Tabs>

To use it, copy the function into the configuration file of your respective shell.

Then use `y` instead of `yazi` to start, and press <kbd>q</kbd> to quit, you'll see the CWD changed. Sometimes, you don't want to change, press <kbd>Q</kbd> to quit.

### Keybindings

:::tip
For all keybindings, see the [default `keymap.toml` file](https://github.com/sxyazi/yazi/blob/shipped/yazi-config/preset/keymap-default.toml).
:::

#### Navigation

To navigate between files and directories you can use the arrow keys <kbd>←</kbd>, <kbd>↓</kbd>, <kbd>↑</kbd> and <kbd>→</kbd>
or Vim-like keys such as <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd>, <kbd>l</kbd>:

| Key binding  | Alternate key | Action                                          |
| ------------ | ------------- | ----------------------------------------------- |
| <kbd>k</kbd> | <kbd>↑</kbd>  | Move the cursor up                              |
| <kbd>j</kbd> | <kbd>↓</kbd>  | Move the cursor down                            |
| <kbd>l</kbd> | <kbd>→</kbd>  | Enter hovered directory                         |
| <kbd>h</kbd> | <kbd>←</kbd>  | Leave the current directory and into its parent |

Further navigation actions can be found in the table below.

| Key binding                     | Action                                                                            |
| ------------------------------- | --------------------------------------------------------------------------------- |
| <kbd>K</kbd>                    | Seek up 5 units in the preview                                                    |
| <kbd>J</kbd>                    | Seek down 5 units in the preview                                                  |
| <kbd>g</kbd> ⇒ <kbd>g</kbd>     | Move cursor to the top                                                            |
| <kbd>G</kbd>                    | Move cursor to the bottom                                                         |
| <kbd>z</kbd>                    | [Cd][mgr.cd] to a directory or [reveal][mgr.reveal] a file via fzf                |
| <kbd>Z</kbd>                    | [Cd][mgr.cd] to a directory via zoxide                                            |
| <kbd>g</kbd> ⇒ <kbd>Space</kbd> | [Cd][mgr.cd] to a directory or [reveal][mgr.reveal] a file via interactive prompt |

[mgr.cd]: /docs/configuration/keymap#mgr.cd
[mgr.reveal]: /docs/configuration/keymap#mgr.reveal

#### Selection

To select files and directories, the following actions are available.

| Key binding                    | Action                                     |
| ------------------------------ | ------------------------------------------ |
| <kbd>Space</kbd>               | Toggle selection of hovered file/directory |
| <kbd>v</kbd>                   | Enter visual mode (selection mode)         |
| <kbd>V</kbd>                   | Enter visual mode (unset mode)             |
| <kbd>Ctrl</kbd> + <kbd>a</kbd> | Select all files                           |
| <kbd>Ctrl</kbd> + <kbd>r</kbd> | Inverse selection of all files             |
| <kbd>Esc</kbd>                 | Cancel selection                           |

#### File operations

To interact with selected files/directories use any of the actions below.

| Key binding                         | Action                                                                  |
| ----------------------------------- | ----------------------------------------------------------------------- |
| <kbd>o</kbd>                        | Open selected files                                                     |
| <kbd>O</kbd>                        | Open selected files interactively                                       |
| <kbd>Enter</kbd>                    | Open selected files                                                     |
| <kbd>Shift</kbd> + <kbd>Enter</kbd> | Open selected files interactively (some terminals don't support it yet) |
| <kbd>Tab</kbd>                      | Show the file information                                               |
| <kbd>y</kbd>                        | Yank selected files (copy)                                              |
| <kbd>x</kbd>                        | Yank selected files (cut)                                               |
| <kbd>p</kbd>                        | Paste yanked files                                                      |
| <kbd>P</kbd>                        | Paste yanked files (overwrite if the destination exists)                |
| <kbd>Y</kbd> or <kbd>X</kbd>        | Cancel the yank status                                                  |
| <kbd>d</kbd>                        | Trash selected files                                                    |
| <kbd>D</kbd>                        | Permanently delete selected files                                       |
| <kbd>a</kbd>                        | Create a file (ends with / for directories)                             |
| <kbd>r</kbd>                        | Rename selected file(s)                                                 |
| <kbd>.</kbd>                        | Toggle the visibility of hidden files                                   |

Further file operation actions can be found in the table below.

| Key binding                    | Action                                     |
| ------------------------------ | ------------------------------------------ |
| <kbd>;</kbd>                   | Run a shell command                        |
| <kbd>:</kbd>                   | Run a shell command (block until finishes) |
| <kbd>-</kbd>                   | Symlink the absolute path of yanked files  |
| <kbd>\_</kbd>                  | Symlink the relative path of yanked files  |
| <kbd>Ctrl</kbd> + <kbd>-</kbd> | Hardlink yanked files                      |

#### Copy paths

To copy paths, use any of the following actions below.

_Observation: <kbd>c</kbd> ⇒ <kbd>d</kbd> indicates pressing the <kbd>c</kbd> key followed by pressing the <kbd>d</kbd> key._

| Key binding                 | Action                              |
| --------------------------- | ----------------------------------- |
| <kbd>c</kbd> ⇒ <kbd>c</kbd> | Copy the file path                  |
| <kbd>c</kbd> ⇒ <kbd>d</kbd> | Copy the directory path             |
| <kbd>c</kbd> ⇒ <kbd>f</kbd> | Copy the filename                   |
| <kbd>c</kbd> ⇒ <kbd>n</kbd> | Copy the filename without extension |

#### Filter files

| Key binding  | Action       |
| ------------ | ------------ |
| <kbd>f</kbd> | Filter files |

#### Find files

| Key binding  | Action                   |
| ------------ | ------------------------ |
| <kbd>/</kbd> | Find next file           |
| <kbd>?</kbd> | Find previous file       |
| <kbd>n</kbd> | Go to the next found     |
| <kbd>N</kbd> | Go to the previous found |

#### Search files

| Key binding                    | Action                                                                         |
| ------------------------------ | ------------------------------------------------------------------------------ |
| <kbd>s</kbd>                   | Search files by name using [fd](https://github.com/sharkdp/fd)                 |
| <kbd>S</kbd>                   | Search files by content using [ripgrep](https://github.com/BurntSushi/ripgrep) |
| <kbd>Ctrl</kbd> + <kbd>s</kbd> | Cancel the ongoing search                                                      |

#### Sorting

To sort files/directories use the following actions.

_Observation: <kbd>,</kbd> ⇒ <kbd>a</kbd> indicates pressing the <kbd>,</kbd> key followed by pressing the <kbd>a</kbd> key._

| Key binding                 | Action                           |
| --------------------------- | -------------------------------- |
| <kbd>,</kbd> ⇒ <kbd>m</kbd> | Sort by modified time            |
| <kbd>,</kbd> ⇒ <kbd>M</kbd> | Sort by modified time (reverse)  |
| <kbd>,</kbd> ⇒ <kbd>b</kbd> | Sort by birth time               |
| <kbd>,</kbd> ⇒ <kbd>B</kbd> | Sort by birth time (reverse)     |
| <kbd>,</kbd> ⇒ <kbd>e</kbd> | Sort by file extension           |
| <kbd>,</kbd> ⇒ <kbd>E</kbd> | Sort by file extension (reverse) |
| <kbd>,</kbd> ⇒ <kbd>a</kbd> | Sort alphabetically              |
| <kbd>,</kbd> ⇒ <kbd>A</kbd> | Sort alphabetically (reverse)    |
| <kbd>,</kbd> ⇒ <kbd>n</kbd> | Sort naturally                   |
| <kbd>,</kbd> ⇒ <kbd>N</kbd> | Sort naturally (reverse)         |
| <kbd>,</kbd> ⇒ <kbd>s</kbd> | Sort by size                     |
| <kbd>,</kbd> ⇒ <kbd>S</kbd> | Sort by size (reverse)           |
| <kbd>,</kbd> ⇒ <kbd>r</kbd> | Sort randomly                    |

#### Multi-tab

| Key binding                                   | Action                             |
| --------------------------------------------- | ---------------------------------- |
| <kbd>t</kbd> ⇒ <kbd>t</kbd>                   | Create a new tab in CWD            |
| <kbd>1</kbd>, <kbd>2</kbd>, ..., <kbd>9</kbd> | Switch to the N-th tab             |
| <kbd>[</kbd>                                  | Switch to the previous tab         |
| <kbd>]</kbd>                                  | Switch to the next tab             |
| <kbd>\{</kbd>                                 | Swap current tab with previous tab |
| <kbd>}</kbd>                                  | Swap current tab with next tab     |
| <kbd>Ctrl</kbd> + <kbd>c</kbd>                | Close the current tab              |

### Flavors

Pick a color scheme you like from our [flavors repository](https://github.com/yazi-rs/flavors), or [cook a flavor](/docs/flavors/overview#cooking)!

---

## Configuration

There are three configuration files for Yazi:

- [`yazi.toml`](/docs/configuration/yazi) - General configuration.
- [`keymap.toml`](/docs/configuration/keymap) - Keybindings configuration.
- [`theme.toml`](/docs/configuration/theme) - Color scheme configuration.

You can find the default configuration files on the **_`shipped`_** tag, [https://github.com/sxyazi/yazi/tree/**_shipped_**/yazi-config/preset](https://github.com/sxyazi/yazi/tree/shipped/yazi-config/preset).

To override any of the defaults, begin by creating the corresponding file (from the directory linked above) to:

- `~/.config/yazi/` on Unix-like systems.
- `%AppData%\yazi\config\` on Windows.

For example, to change the visible status of hidden files, start by creating a `yazi.toml` file to:

- `~/.config/yazi/yazi.toml` on Unix-like systems.
- `%AppData%\yazi\config\yazi.toml` on Windows.

Then [copy the required part](https://github.com/sxyazi/yazi/blob/shipped/yazi-config/preset/yazi-default.toml) into it, here is `show_hidden`:

```toml
## yazi.toml
[mgr]
show_hidden = true
```

Yazi has already preset these default configurations in the release, so you don't need to copy the entire file unless you want to completely overwrite them.

### Configuration mixing {#mixing}

The options from your configuration file will be used to override the default. However, for key bindings, if you don't want to override the default directly:

```toml
## keymap.toml
[mgr]
keymap = [
	# ...
]
```

And instead want to customize your keys upon the default, you can use `prepend_*` or `append_*` directories to prepend or append them to the default (See [keymap.toml](/docs/configuration/keymap) for details):

```toml
## keymap.toml
[mgr]
prepend_keymap = [
	# ...
]
append_keymap = [
	# ...
]
```

They are also available for open, icon, previewer, and preloader rules.

### Custom config directory {#custom-directory}

You can change the Yazi configuration directory by exporting the `YAZI_CONFIG_HOME` environment variable. For example:

```sh
YAZI_CONFIG_HOME=~/.config/yazi-alt yazi
```

will start Yazi with `~/.config/yazi-alt` as the configuration directory, and can have its own `yazi.toml`, `keymap.toml`, `init.lua`, etc. files within it.

---

## yazi.toml

:::info
If you want to fine-tune the default settings, the first step is to [create your own configuration file](/docs/configuration/overview).
:::

### [mgr] {#mgr}

#### `ratio` {#mgr.ratio}

Manager layout by ratio, 3-element array. For example:

- `[1, 4, 3]`: 1/8 width for parent, 4/8 width for current, 3/8 width for preview

Set the value to `0` to hide the corresponding panel, but at least one panel must be visible (non-zero).

#### `sort_by` {#mgr.sort_by}

File sorting method.

- `"none"`: Don't sort.
- `"mtime"`: Sort by last modified time.
- `"btime"`: Sort by birth time.
- `"extension"`: Sort by file extension.
- `"alphabetical"`: Sort alphabetically, e.g. `1.md` < `10.md` < `2.md`
- `"natural"`: Sort naturally, e.g. `1.md` < `2.md` < `10.md`
- `"size"`: Sort by file size.
- `"random"`: Sort randomly.

#### `sort_sensitive` {#mgr.sort_sensitive}

Sort case-sensitively.

- `true`: Case-sensitive
- `false`: Case-insensitive

#### `sort_reverse` {#mgr.sort_reverse}

Display files in reverse order.

- `true`: Reverse order
- `false`: Normal order

#### `sort_dir_first` {#mgr.sort_dir_first}

Display directories first.

- `true`: Directories first
- `false`: Normal order

#### `sort_translit` {#mgr.sort_translit}

Transliterate filenames for sorting (i.e. replace `Â` with `A`, `Æ` with `AE`, etc.), only available if [`sort_by = "natural"`](#mgr.sort_by).

This is useful for files that contain Hungarian characters.

- `true`: Enabled
- `false`: Disabled

#### `linemode` {#mgr.linemode}

Line mode: display information associated with the file on the right side of the file list row.

- `"none"`: No line mode.
- `"size"`: Display the size in bytes of the file. Note that currently directory sizes are only evaluated when [`sort_by = "size"`](/docs/configuration/yazi#mgr.sort_by), and this might change in the future.
- `"btime"`: Display the birth time of the file.
- `"mtime"`: Display the last modified time of the file.
- `"permissions"`: Display the permissions of the file, only available on Unix-like systems.
- `"owner"`: Display the owner of the file, only available on Unix-like systems.

You can also specify any string from 1 to 20 characters and extend it with a UI plugin, which means you can implement your own linemode through the plugin system like this:

```toml
## ~/.config/yazi/yazi.toml
[mgr]
linemode = "size_and_mtime"
```

```lua
-- ~/.config/yazi/init.lua
function Linemode:size_and_mtime()
	local time = math.floor(self._file.cha.mtime or 0)
	if time == 0 then
		time = ""
	elseif os.date("%Y", time) == os.date("%Y") then
		time = os.date("%b %d %H:%M", time)
	else
		time = os.date("%b %d  %Y", time)
	end

	local size = self._file:size()
	return string.format("%s %s", size and ya.readable_size(size) or "-", time)
end
```

#### `show_hidden` {#mgr.show_hidden}

Show hidden files.

- `true`: Show
- `false`: Do not show

#### `show_symlink` {#mgr.show_symlink}

Show the path that the symlink points to after the filename.

- `true`: Show
- `false`: Do not show

#### `scrolloff` {#mgr.scrolloff}

The number of files to keep above and below the cursor when moving through the file list.

If the value is larger than half the screen height (e.g. `200`), the cursor will be centered.

#### `mouse_events` {#mgr.mouse_events}

Array of strings, the types of mouse events can be received by the plugin system, available values:

- `"click"`: Mouse click
- `"scroll"`: Mouse vertical scroll
- `"touch"`: Mouse horizontal scroll
- `"move"`: Mouse move
- `"drag"`: Mouse drag (Some terminals do not support this)

If the array is empty, disable the mouse.

Usually, you don't need to change it, unless the plugin you're using requires enabling a certain event.

### [preview] {#preview}

#### `wrap` {#preview.wrap}

Wrap long lines in the code preview.

- `"yes"`: Enable word wrap
- `"no"`: Disable word wrap

#### `tab_size` {#preview.tab_size}

The width of a tab character (`\t`) in spaces.

#### `max_width` {#preview.max_width}

Maximum preview width for images. Run `yazi --clear-cache` after changing this for it to take effect.

This value is also used for preloading images; the larger it is, the larger the image cache generated, which consumes more CPU.

#### `max_height` {#preview.max_height}

Maximum preview height for images. Run `yazi --clear-cache` after changing this for it to take effect.

This value is also used for preloading images; the larger it is, the larger the image cache generated, which consumes more CPU.

#### `cache_dir` {#preview.cache_dir}

The system cache directory is used by default, and the cached files will go away on a reboot automatically.

If you want to make it more persistent, you can specify the cache directory manually as an absolute path.

#### `image_delay` {#preview.image_delay}

Wait for at least the specified milliseconds before starting to send image preview data to the terminal.

This is to alleviate lag caused by some terminal emulators struggling to render images sent by Yazi in time when users scroll through the file list quickly.

See https://github.com/sxyazi/yazi/pull/1512 for more information.

#### `image_filter` {#preview.image_filter}

The filter used on image downscaling, available values:

- `"nearest"` - Nearest Neighbor
- `"triangle"` - Linear Triangle
- `"catmull-rom"` - Catmull-Rom
- `"lanczos3"` - Lanczos with window 3

They are arranged in order from fast to slow, and from poor to good quality - Lanczos3 provides the highest quality but is also the slowest.

See the example and benchmark here: https://docs.rs/image/0.24.8/image/imageops/enum.FilterType.html#examples

#### `image_quality` {#preview.image_quality}

Quality on pre-caching images, range 50-90.

The larger value, the better image quality, but slower with more CPU consumption, and generates larger cache files that occupy more storage space.

#### `ueberzug_scale` / `ueberzug_offset` {#preview.ueberzug_scale}

- ueberzug_scale (Float): Ueberzug image scaling ratio, `scale>1` for enlargement, `scale<1` for reduction. For example, `0.5` indicates a reduction to half.
- ueberzug_offset (`[x, y, width, height]`): Ueberzug image offset, in cell units. For example, `[0.5, 0.5, -0.5, -0.5]` indicates that the image is offset by half a cell in both directions, and the width and height are reduced by half a cell.

This is useful for solving [a bug of Überzug++ image size calculation](https://github.com/jstkdng/ueberzugpp/issues/122).

If your monitor has a `2.0` scale factor, and is running on Wayland under Hyprland, you may need to set `ueberzug_scale: 0.5`, and adjust the value of `ueberzug_offset` according to your case, to offset this issue.

### [opener] {#opener}

Configure available openers that can be used in [`[open]`](#open), for example:

```toml
[opener]
play = [
	{ run = "mpv %s", orphan = true, for = "unix" },
	{ run = '"C:\Program Files\mpv.exe" %s', orphan = true, for = "windows" }
]
edit = [
	{ run = "$EDITOR %s", block = true, for = "unix" },
	{ run = "%EDITOR% %s", block = true, for = "windows" },
]
open = [
	{ run = "xdg-open %s1", desc = "Open" },
]
## ...
```

Available options are as follows:

- `run`: The command to open the selected files, with the following formatting parameters available:
  - `%s`: Paths of all selected files
  - `%S`: URLs of all selected files
  - `%sN`: Path of the N-th selected file, e.g. `%s1`, `%s2`, etc.
  - `%SN`: URL of the N-th selected file, e.g. `%S1`, `%S2`, etc.
  - `%d`: Dirnames of all selected files
  - `%D`: Dirnames of all selected files, as URLs
  - `%dN`: Dirname of the N-th selected file, e.g. `%d1`, `%d2`, etc.
  - `%DN`: Dirname of the N-th selected file as URL, e.g. `%D1`, `%D2`, etc.
  - `%%`: Escape form of the `%` character itself
- `block`: Open in a blocking manner. After setting this, Yazi will hide into a secondary screen and display the program on the main screen until it exits. During this time, it can receive I/O signals, which is useful for interactive programs.
- `orphan`: Keep the process running even if Yazi has exited, once specified, the process will be detached from the task scheduling system.
- `desc`: Description of the opener, display in interactive components, such as "Open with" and help menu.
- `for`: The opener is only available on this system; if not specified, it's available on all systems. Available values:
  - `linux`: Linux
  - `macos`: macOS
  - `windows`: Windows
  - `android`: Android (Termux)
  - `unix`: Linux, macOS, and Android

### [open] {#open}

Set rules for opening specific files. You can prepend or append rules to the default through `prepend_rules` and `append_rules` (See [Configuration mixing](/docs/configuration/overview#mixing) for details):

```toml
[open]
prepend_rules = [
	{ url = "*.json", use = "edit" },

	# Multiple openers for a single rule
	{ url = "*.html", use = [ "open", "edit" ] },
]
append_rules = [
	{ url = "*", use = "my-fallback" },
]
```

If your `append_rules` contains wildcard rules, they will always take precedence over the default wildcard rules as the fallback.

Or, use `rules` to rewrite the entire default rules:

```toml
[open]
rules = [
	{ mime = "text/*", use = "edit" },
	{ mime = "video/*", use = "play" },

	# { mime = "application/json", use = "edit" },
	{ url = "*.json", use = "edit" },

	# Multiple openers for a single rule
	{ url = "*.html", use = [ "open", "edit" ] },
]
```

Available rule options are as follows:

- `url`: Glob expression for file URL matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `mime`: Glob expression for MIME-type matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `use`: Opener name corresponding to the names in the [`[opener]` section](#opener).

With that:

- You can [`spot`](/docs/configuration/keymap#mgr.spot) on a file to check it's mime-type with the default <kbd>Tab</kbd> key.
- If `use` is an array containing multiple openers, all commands in these openers will be merged. [`open`](/docs/configuration/keymap#mgr.open) will run the first of these commands; [`open --interactive`](/docs/configuration/keymap#mgr.open) will list all of these commands in the "open with" menu.

### [tasks] {#tasks}

#### `file_workers` {#tasks.file_workers}

Max concurrent file operations, such as copy, cut, delete, etc.

#### `plugin_workers` {#tasks.plugin_workers}

Max concurrent functional-plugin tasks.

#### `fetch_workers` {#tasks.fetch_workers}

Max concurrent fetch tasks.

#### `preload_workers` {#tasks.preload_workers}

Max concurrent preload tasks.

#### `process_workers` {#tasks.process_workers}

Max concurrent processes.

#### `bizarre_retry` {#tasks.bizarre_retry}

Maximum number of retries when a bizarre failure occurs.

#### `suppress_preload` {#tasks.suppress_preload}

Exclude the preload tasks created by the system from the task list, do not report their progress, and do not consider them on app exit confirming.

#### `image_alloc` {#tasks.image_alloc}

Maximum memory allocation limit in bytes for decoding a single image, `0` for unlimited.

#### `image_bound` {#tasks.image_bound}

An array of `[width, height]`, maximum image size (in pixels) for decoding a single image, and `0` for unlimited.

### [plugin] {#plugin}

#### fetchers {#plugin.fetchers}

:::warning
Fetchers are not complete yet, and the API is subject to change without prior notice!
:::

TODO

You can prepend or append new fetchers to the default `fetchers` under `[plugin]` by `prepend_fetchers` and `append_fetchers`, see [Configuration mixing](/docs/configuration/overview#mixing) for details.
Here are the available options for a single rule:

- `url`: Glob expression for file URL matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `run`: Name of the Lua plugin to be run.
- `if`: Run the fetcher only if the condition is met.
- `prio`: Task scheduling priority. One of `high`, `normal` or `low`.
- `group`: Group of the fetcher. Only the first matching fetcher in the same group will be run.

#### previewers {#plugin.previewers}

You can prepend or append new preview rules to the default `previewers` under `[plugin]` by `prepend_previewers` and `append_previewers`, see [Configuration mixing](/docs/configuration/overview#mixing) for details.
Here are the available options for a single rule:

- `url` (String): Glob expression for file URL matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `mime` (String): Glob expression for MIME-type matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `run` (String): Name of the Lua plugin to be run.

```toml
[plugin]
prepend_previewers = [
	# HEIC previewer
	{ mime = "image/heic", run = "heic" },
	# RAF previewer
	{ url = "*.raf", run = "raf" },
]

append_previewers = [
	# My fallback previewer
	{ url = "*", run = "binary" },
]
```

If your `append_previewers` contains wildcard `url` rules (`"*"` or `"*/"`), they will always take precedence over the default wildcard rules as the fallback.

Yazi comes with these previewer plugins:

- folder: bridge between the Yazi filesystem and the preview
- code: bridge between built-in code highlighting and the preview, providing async concurrent rendering
- json: bridge between `jq` and the preview, providing async concurrent rendering
- noop: no operation
- image: presentation layer of built-in image preview, offering mixed preview capabilities
- video: bridge between `ffmpeg` and the preview, offering mixed preview capabilities
- pdf: bridge between `pdftoppm` and the preview, offering mixed preview capabilities
- archive: bridge between 7-Zip and the preview, offering mixed preview and concurrent rendering capabilities

If you want to create your own previewer, see [Previewer API](/docs/plugins/overview#previewer).

#### preloaders {#plugin.preloaders}

You can prepend or append new preview rules to the default `preloaders` under `[plugin]` by `prepend_preloaders` and `append_preloaders`, see [Configuration mixing](/docs/configuration/overview#mixing) for details.
Here are the available options for a single rule:

- `url` (String): Glob expression for file URL matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `mime` (String): Glob expression for MIME-type matching. Case-insensitive by default, prepend `\s` to make it sensitive.
- `run` (String): Name of the Lua plugin to be run.
- `prio` (String): Preload priority, `low`, `normal` or `high`. The default is `normal` if not specified.

```toml
[plugin]
prepend_preloaders = [
	# HEIC preloader
	{ mime = "image/heic", run = "heic" },
]
```

Yazi comes with these preloader plugins:

- mime: preloads mime-type of files in chunks
- noop: no operation
- image: preloads and caches images
- video: preloads and caches videos
- pdf: preloads and caches PDFs.

If you want to create your own preloader, see [Preloader API](/docs/plugins/overview#preloader).

### [input] {#input}

#### `cursor_blink` {#input.cursor_blink}

Control the cursor blinking.

- `true`: Blink.
- `false`: Do not blink.

You can customize the title and position of each input. The following inputs are available: `cd`, `create`, `rename`, `filter`, `find`, `search` and `shell`. To change their configuration, use an underscore between the name and the option, like `cd_origin`.

As for position, it consists of two parts: [Origin](#input.origin) and [Offset](#input.offset).
The origin is the top-left corner of the input, and the offset is the increment from this origin. Together, they determine the area of the input on the screen.

#### Origin {#input.origin}

See [`Origin`](/docs/plugins/aliases#origin) for available values.

#### Offset {#input.offset}

As for the offset, it's a 4-element tuple: `(x, y, width, height)`.

#### Placeholder {#input.placeholder}

Some inputs have special placeholders that will be replaced with actual content on display:

- cd_title: String

  Title of the [`cd --interactive`](/docs/configuration/keymap/#mgr.cd) input used to enter the target path.

- create_title: [String, String]

  It's a tuple of 2-element: first for [`create`](/docs/configuration/keymap/#mgr.create) input title, second for `create --dir` action.

- rename_title: String

  Title of the [`rename`](/docs/configuration/keymap/#mgr.rename) input used to enter the new name.

- filter_title: String

  Title of the [`filter`](/docs/configuration/keymap/#mgr.filter) input used to enter the keyword.

- find_title: [String, String]

  It's a tuple of 2-element: first for [`find`](/docs/configuration/keymap/#mgr.find), second for `find --previous`.

- search_title: String

  - `{n}`: Name of the current [`search`](/docs/configuration/keymap/#mgr.search) engine.

- shell_title: [String, String]

  It's a tuple of 2-element: first for [`shell --interactive`](/docs/configuration/keymap/#mgr.shell), second for `shell --interactive --block`.

### [confirm] {#confirm}

Same as the [`[input]`](#input) section. There are a few available: `trash`, `delete`, `overwrite` and `quit`.

### [pick] {#pick}

Same as the [`[input]`](#input) section. Available selectors: `open`.

### [which] {#which}

#### `sort_by` {#which.sort_by}

Candidate sorting method.

- `"none"`: Don't sort.
- `"key"`: Sort by key.
- `"desc`: Sort by description.

#### `sort_sensitive` {#which.sort_sensitive}

Sort case-sensitively.

- `true`: Case-sensitive
- `false`: Case-insensitive

#### `sort_reverse` {#which.sort_reverse}

Display candidates in reverse order.

- `true`: Reverse order
- `false`: Normal order

#### `sort_translit` {#which.sort_translit}

Transliterate filenames for sorting, i.e. replace `Â` with `A`, `Æ` with `AE`, etc.

This is useful for files that contain Hungarian characters.

- `true`: Enabled
- `false`: Disabled

---

## keymap.toml

:::info
If you want to fine-tune the default settings, the first step is to [create your own configuration file](/docs/configuration/overview).
:::

You can change Yazi's keybindings in your `keymap.toml` file, which consists of the following 8 layers:

- [\[mgr\]](#mgr) - File list.
- [\[tasks\]](#tasks) - Task manager.
- [\[spot\]](#spot) - File information spotter.
- [\[pick\]](#pick) - Pick component. e.g. "open with" for files.
- [\[input\]](#input) - Input component. e.g. create, rename, etc.
- [\[confirm\]](#confirm) - Confirmation dialog. e.g. remove, overwrite, etc.
- [\[cmp\]](#cmp) - Completion component. e.g. "cd" URL completion.
- [\[help\]](#help) - Help menu.

In each layer, there are two attributes: `prepend_keymap` and `append_keymap`.
Prepend inserts before [the default keybindings](https://github.com/sxyazi/yazi/blob/shipped/yazi-config/preset/keymap-default.toml), while append inserts after them.

Since Yazi selects the first matching key to run, prepend always has a higher priority than default, and append always has a lower priority than default:

```toml
[mgr]
prepend_keymap = [
	{ on = "<C-a>", run = "act1", desc = "Single action with `Ctrl + a`" },
]
append_keymap = [
	{ on = [ "g", "b" ], run = "act2",             desc = "Single action with `g ⇒ b`" },
	{ on = "c",          run = [ "act1", "act2" ], desc = "Multiple actions with `c`" }
]
```

Or in another different style:

```toml
[[mgr.prepend_keymap]]
on   = "<C-a>"
run  = "act1"
desc = "Single action with `Ctrl + a`"

[[mgr.append_keymap]]
on  = [ "g", "b" ]
run = "act2"
desc = "Single action with `g ⇒ b`"

[[mgr.append_keymap]]
on  = "c"
run = [ "act1", "act2" ]
desc = "Multiple actions with `c`"
```

But keep in mind that you can only choose one of them, and it cannot be a combination of the two, as TOML language does not allow this:

```toml
[mgr]
prepend_keymap = [
	{ on = "<C-a>", run = "act1" },
]

[[mgr.append_keymap]]
on  = [ "g", "b" ]
run = "act2"
```

When you don't need any default and want to fully customize your keybindings, use `keymap`, for example:

```toml
[mgr]
keymap = [
	# This will override all default keybindings, and just keep the two below.
	{ on = "<C-a>",      run = "act1" },
	{ on = [ "g", "b" ], run = "act2" },
]
```

### Key notation {#notation}

You can specify one or more keys in the `on` of each keybinding rule, and each key can be represented with the following notations:

| Notation         | Description       | Notation      | Description       |
| ---------------- | ----------------- | ------------- | ----------------- |
| `a` - `z`        | Lowercase letters | `A` - `Z`     | Uppercase letters |
| `<Space>`        | Space key         | `<Backspace>` | Backspace key     |
| `<Enter>`        | Enter key         | -             | -                 |
| `<Left>`         | Left arrow key    | `<Right>`     | Right arrow key   |
| `<Up>`           | Up arrow key      | `<Down>`      | Down arrow key    |
| `<Home>`         | Home key          | `<End>`       | End key           |
| `<PageUp>`       | PageUp key        | `<PageDown>`  | PageDown key      |
| `<Tab>`          | Tab key           | `<BackTab>`   | Shift + Tab key   |
| `<Delete>`       | Delete key        | `<Insert>`    | Insert key        |
| `<F1>` - `<F19>` | Function keys     | `<Esc>`       | Escape key        |

You can combine the following modifiers for the keys above:

| Modifier | Description                |
| -------- | -------------------------- |
| `<S-…>`  | Shift key.                 |
| `<C-…>`  | Ctrl key.                  |
| `<A-…>`  | Alt/Meta key.              |
| `<D-…>`  | Command/Windows/Super key. |

For example:

- `<C-a>` for <kbd>Ctrl</kbd> + <kbd>a</kbd>.
- `<C-S-b>` or `<C-B>` for <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>b</kbd>.

Note that:

1. Not all terminals support `<D-...>` - make sure your terminal supports and has [CSI u][CSI u] enabled if you want to use it.
2. macOS doesn't have an <kbd>Alt</kbd> key, so `<A-...>` won't work. Some terminals offer a setting to map the <kbd>Option</kbd> as the <kbd>Alt</kbd> key, make sure you have it enabled.
3. The [legacy terminal keyboard protocol][Control character] treats `<Tab>` and `<C-i>`, `<Enter>` and `<C-m>`, etc. as the same key. If you want to distinguish between them, make sure your terminal supports and has [CSI u][CSI u] enabled.

[CSI u]: https://sw.kovidgoyal.net/kitty/keyboard-protocol/
[Control character]: https://en.wikipedia.org/wiki/Control_character

### [mgr] {#mgr}

#### `escape` {#mgr.escape}

Cancel find, exit visual mode, clear selected, cancel filter, or cancel search.

| Argument/Option | Description       |
| --------------- | ----------------- |
| `--all`         | Do all the below. |
| `--find`        | Cancel find.      |
| `--visual`      | Exit visual mode. |
| `--select`      | Clear selected.   |
| `--filter`      | Cancel filter.    |
| `--search`      | Cancel search.    |

Automatically determine the operation by default, and it will only execute the selected operation after specifying the option; multiple options can be stacked.

#### `quit` {#mgr.quit}

Exit the process.

| Argument/Option | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| `--code=[n]`    | Exit code.                                                                     |
| `--no-cwd-file` | Don't output the current directory to the file specified by `yazi --cwd-file`. |

#### `close` {#mgr.close}

Close the current tab; if it's the last tab, exit the process instead.

| Argument/Option | Description                                                                            |
| --------------- | -------------------------------------------------------------------------------------- |
| `--code=[n]`    | Exit code used when exiting.                                                           |
| `--no-cwd-file` | Don't output the current directory to the file specified by `yazi --cwd-file` on exit. |

#### `suspend` {#mgr.suspend}

Pauses Yazi and returns to the parent shell to continue with other tasks.

Once those tasks are done, use the `fg` command of the shell to send a resume signal and return back to Yazi.

#### `arrow` {#mgr.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `leave` {#mgr.leave}

Go back to the parent directory of the hovered file, or the parent of the current working directory if no file is hovered on.

#### `enter` {#mgr.enter}

Enter the child directory.

#### `back` {#mgr.back}

Go back to the previous directory.

#### `forward` {#mgr.forward}

Go forward to the next directory.

#### `seek` {#mgr.seek}

Scroll the contents in the preview panel.

| Argument/Option | Description                                                      |
| --------------- | ---------------------------------------------------------------- |
| `[n]`           | Use negative values to seek up and positive values to seek down. |

#### `spot` {#mgr.spot}

Display file information with the preset or user-customized spotter.

#### `cd` {#mgr.cd}

Change the current directory.

| Argument/Option | Description                             |
| --------------- | --------------------------------------- |
| `[url]`         | The URL to change to.                   |
| `--interactive` | Use an interactive UI to input the URL. |

You can add your own `g` series keys to achieve a simple bookmark feature:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "d" ]
run  = "cd ~/Downloads"
desc = "Cd to ~/Downloads"

[[mgr.prepend_keymap]]
on   = [ "g", "p" ]
run  = "cd ~/Pictures"
desc = "Cd to ~/Pictures"
```

For Windows users, you can also switch drives using the `cd` action:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "d" ]
run  = "cd D:"
desc = "Switch to D drive"

[[mgr.prepend_keymap]]
on   = [ "g", "p" ]
run  = 'cd "E:\\Pictures"'  # We need to escape the backslash
desc = 'Cd to E:\Pictures'
```

Check out the [resources page](/docs/resources) for a more comprehensive bookmark plugin.

#### `follow` {#mgr.follow}

Follow the hovered file if it's a symbolic link.

#### `reveal` {#mgr.reveal}

Hover over the specified file.

If the file is not in the current directory, it will change the current directory to the file's parent.

| Argument/Option | Description        |
| --------------- | ------------------ |
| `[url]`         | The URL to reveal. |

#### `toggle` {#mgr.toggle}

Toggle the selection state of the hovered file.

| Argument/Option | Description            |
| --------------- | ---------------------- |
| N/A             | Reverse the selection. |
| `--state=on`    | Select the file.       |
| `--state=off`   | Deselect the file.     |

#### `toggle_all` {#mgr.toggle_all}

Toggle the selection state of all files in the current working directory.

| Argument/Option | Description             |
| --------------- | ----------------------- |
| N/A             | Reverse the selections. |
| `--state=on`    | Select the files.       |
| `--state=off`   | Deselect the files.     |

Note that `toggle_all --state=off` only deselect the files in CWD, if you have selected files across multiple directories, and want to deselect all of them, use [`escape --select`](#mgr.escape).

#### `visual_mode` {#mgr.visual_mode}

Enter visual mode.

| Argument/Option | Description     |
| --------------- | --------------- |
| N/A             | Selection mode. |
| `--unset`       | Unset mode.     |

#### `open` {#mgr.open}

Open the selected files using [the rules in `[open]`](/docs/configuration/yazi#open).

| Argument/Option | Description                                                                            |
| --------------- | -------------------------------------------------------------------------------------- |
| `--interactive` | Open the hovered/selected file(s) with an interactive UI to choose the opening method. |
| `--hovered`     | Always open the hovered file regardless of the selection state.                        |

#### `yank` {#mgr.yank}

Yank the selected files.

| Argument/Option | Description |
| --------------- | ----------- |
| N/A             | Copy mode.  |
| `--cut`         | Cut mode.   |

#### `unyank` {#mgr.unyank}

Cancel the yank status of files.

#### `paste` {#mgr.paste}

Paste the yanked files.

| Argument/Option | Description                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------ |
| `--force`       | Overwrite the destination file if it exists.                                                                 |
| `--follow`      | Copy the file pointed to by the symbolic link, rather than the link itself. Only can be used during copying. |

#### `link` {#mgr.link}

Create a symbolic link to the yanked files. (This is a privileged action on Windows and must be run as an administrator.)

| Argument/Option | Description                                  |
| --------------- | -------------------------------------------- |
| `--relative`    | Use a relative path for the symbolic link.   |
| `--force`       | Overwrite the destination file if it exists. |

#### `hardlink` {#mgr.hardlink}

Hardlink the yanked files.

| Argument/Option | Description                                                              |
| --------------- | ------------------------------------------------------------------------ |
| `--force`       | Overwrite the destination file if it exists.                             |
| `--follow`      | Hardlink the file pointed to by a symbolic link, not the symlink itself. |

#### `remove` {#mgr.remove}

Move the files to the trash/recycle bin on macOS/Windows. For Linux, it follows the [FreeDesktop.org Trash Specification](https://specifications.freedesktop.org/trash/latest/).

In the Android platform, you can only use it with the `--permanently` option, since there lacks the concept of a trash bin.

| Argument/Option | Description                                                          |
| --------------- | -------------------------------------------------------------------- |
| `--force`       | Don't show the confirmation dialog, and trash/delete files directly. |
| `--permanently` | Permanently delete the files.                                        |
| `--hovered`     | Always remove the hovered file regardless of the selection state.    |

#### `create` {#mgr.create}

Create a file or directory. Ends with `/` (Unix) or `\` (Windows) for directories.

| Argument/Option | Description                                                                                    |
| --------------- | ---------------------------------------------------------------------------------------------- |
| `--dir`         | Always create directories, regardless of whether end with `/` or `\`.                          |
| `--force`       | Overwrite the destination file directly if it exists, without showing the confirmation dialog. |

#### `rename` {#mgr.rename}

Rename a file or directory, or bulk rename if multiple files are selected (`$EDITOR` is used to edit the filenames by default, see [Specify a different editor for bulk renaming](/docs/tips#bulk-editor) for details).

- `--hovered`: Always rename the hovered file regardless of the selection state.
- `--force`: Overwrite the destination file directly if it exists, without showing the confirmation dialog.
- `--empty`: Empty a part of the filename.
  - `"stem"`: Empty the stem. e.g. `"foo.jpg"` -> `".jpg"`.
  - `"ext"`: Empty the extension. e.g. `"foo.jpg"` -> `"foo."`.
  - `"dot_ext"`: Empty the dot and extension. e.g. `"foo.jpg"` -> `"foo"`.
  - `"all"`: Empty the whole filename. e.g. `"foo.jpg"` -> `""`.
- `--cursor`: Specify the cursor position of the renaming input box.
  - `"end"`: The end of the filename.
  - `"start"`: The start of the filename.
  - `"before_ext"`: Before the extension of the filename.

You can also use `--cursor` with `--empty`, for example, `rename --empty=stem --cursor=start` will empty the file's stem, and move the cursor to the start.

Which causes the input box content for the filename `foo.jpg` to be `|.jpg`, where "|" represents the cursor position.

#### `copy` {#mgr.copy}

Copy the URL of files or directories that are selected or hovered on.

| Argument/Option | Description                                                     |
| --------------- | --------------------------------------------------------------- |
| `[what]`        | What to copy, see the table below.                              |
| `--separator`   | Path separator, see the table below.                            |
| `--hovered`     | Always copy the hovered file regardless of the selection state. |

`[what]` can be one of the following values:

| Value                | Description                             |
| -------------------- | --------------------------------------- |
| `"path"`             | URL of the file.                        |
| `"dirname"`          | URL of the parent directory.            |
| `"filename"`         | Name of the file.                       |
| `"name_without_ext"` | Name of the file without the extension. |

`--separator` can be one of the following values:

| Value    | Description                                                         |
| -------- | ------------------------------------------------------------------- |
| N/A      | Platform-specific separator, e.g. `\` for Windows and `/` for Unix. |
| `"unix"` | Use `/` for all platforms.                                          |

#### `shell` {#mgr.shell}

Run a shell command.

| Argument/Option | Description                                                                                                                                                                                                                              |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `[template]`    | Optional, command template to be run.                                                                                                                                                                                                    |
| `--block`       | Open in a blocking manner. After setting this, Yazi will hide into a secondary screen and display the program on the main screen until it exits. During this time, it can receive I/O signals, which is useful for interactive programs. |
| `--orphan`      | Keep the process running even if Yazi has exited, once specified, the process will be detached from the task scheduling system.                                                                                                          |
| `--interactive` | Request the user to input the command to be run interactively                                                                                                                                                                            |
| `--cursor`      | Set the initial position of the cursor in the interactive command input box. For example, `shell 'zip -r .zip %h' --cursor=7 --interactive` places the cursor before `.zip`.                                                             |

You can use the following formatting parameters in `[template]`:

- `%h`: Path of hovered file, or empty if under an empty directory where no file is hovered on
- `%s`: Paths of all selected files
- `%sN`: Path of the N-th selected file, e.g. `%s1`, `%s2`, etc.
- `%d`: Dirnames of all selected files
- `%dN`: Dirname of the N-th selected file, e.g. `%d1`, `%d2`, etc.
- `%%`: Escape form of the `%` character itself

And their URL versions:

- `%H`: URL of hovered file, or empty if under an empty directory where no file is hovered on
- `%S`: URLs of all selected files
- `%SN`: URL of the N-th selected file, e.g. `%S1`, `%S2`, etc.
- `%D`: Dirnames of all selected files, as URLs
- `%DN`: Dirname of the N-th selected file as URL, e.g. `%D1`, `%D2`, etc.

You can use an end-of-options marker (`--`) to avoid any escaping - everything following the `--` will be treated as a raw string:

```diff
[[mgr.prepend_keymap]]
on = "d"
- run = "shell \"trash-put %s\""
+ run = "shell -- trash-put %s"
desc = "Trash selected files"
```

For complex shell scripts, you can use TOML's basic strings (`'''` or `"""`) to write them in multiple lines, as demonstrated in [this tip](/docs/tips#email-selected-files).

#### `hidden` {#mgr.hidden}

Set the visibility of hidden files.

| Argument/Option | Description              |
| --------------- | ------------------------ |
| `"show"`        | Show hidden files.       |
| `"hide"`        | Hide hidden files.       |
| `"toggle"`      | Toggle the hidden state. |

#### `linemode` {#mgr.linemode}

Set the [line mode](/docs/configuration/yazi#mgr.linemode).

| Argument/Option | Description                                                                                                                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `"none"`        | No line mode.                                                                                                                                                                                       |
| `"size"`        | Display the size in bytes of the file. Note that currently directory sizes are only evaluated when [`sort_by = "size"`](/docs/configuration/yazi#mgr.sort_by), and this might change in the future. |
| `"btime"`       | Display the birth time of the file.                                                                                                                                                                 |
| `"mtime"`       | Display the last modified time of the file.                                                                                                                                                         |
| `"permissions"` | Display the permissions of the file, only available on Unix-like systems.                                                                                                                           |
| `"owner"`       | Display the owner of the file, only available on Unix-like systems.                                                                                                                                 |

#### `search` {#mgr.search}

| Argument/Option | Description                                                                                       |
| --------------- | ------------------------------------------------------------------------------------------------- |
| `--via`         | Search engine, available values: [`fd`][fd], [`rg`][rg], and [`rga`][rga]                         |
| `--args`        | Additional arguments passed to the specified engine, for example `search --via=fd --args='-e -H'` |

You can search with an empty keyword (`""`) via `fd` to achieve flat view.

<details>
  <summary>Demonstrate flat view</summary>
	<p>Original post: https://github.com/sxyazi/yazi/issues/676#issuecomment-1943494129</p>
	<video src="https://github.com/sxyazi/yazi/assets/17523360/d2c9df9b-b7ef-41ec-889f-26b2f1117cd0" width="100%" controls muted></video>
</details>

Or bind a key to the `search_do` action to quickly switch to the flat view:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "f" ]
run  = 'search_do --via=fd --args="-d 3"'
desc = "Switch to the flat view with a max depth of 3"
```

[fd]: https://github.com/sharkdp/fd
[rg]: https://github.com/BurntSushi/ripgrep
[rga]: https://github.com/phiresky/ripgrep-all

#### `find` {#mgr.find}

Find files in the current working directory interactively and incrementally.

| Argument/Option | Description                                                                                                              |
| --------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `--previous`    | Find for the previous occurrence.                                                                                        |
| `--smart`       | Use smart-case when finding, i.e. case-sensitive if the query contains uppercase characters, otherwise case-insensitive. |
| `--insensitive` | Use case-insensitive find.                                                                                               |

#### `find_arrow` {#mgr.find_arrow}

Move the cursor to the next or previous occurrence.

| Argument/Option | Description                      |
| --------------- | -------------------------------- |
| `--previous`    | Move to the previous occurrence. |

#### `filter` {#mgr.filter}

| Argument/Option | Description                                                                                                           |
| --------------- | --------------------------------------------------------------------------------------------------------------------- |
| `--smart`       | Filter with smart-case, i.e. case-sensitive if the keyword contains uppercase characters, otherwise case-insensitive. |
| `--insensitive` | Use case-insensitive filter.                                                                                          |

#### `sort` {#mgr.sort}

- `[by]`: Optional, if not provided, the sort method will be kept unchanged.
  - `"none"`: Don't sort.
  - `"mtime"`: Sort by last modified time.
  - `"btime"`: Sort by birth time.
  - `"extension"`: Sort by file extension.
  - `"alphabetical"`: Sort alphabetically, e.g. `1.md` < `10.md` < `2.md`
  - `"natural"`: Sort naturally, e.g. `1.md` < `2.md` < `10.md`
  - `"size"`: Sort by file size.
  - `"random"`: Sort randomly.
- `--reverse`: Display files in reverse order. `--reverse` or `--reverse=yes` to enable, `--reverse=no` to disable.
- `--dir-first`: Display directories first. `--dir-first` or `--dir-first=yes` to enable, `--dir-first=no` to disable.
- `--translit`: Transliterate filenames for sorting, see [sort_translit](/docs/configuration/yazi#mgr.sort_translit) for details. `--translit` or `--translit=yes` to enable, `--translit=no` to disable.

#### `tab_create` {#mgr.tab_create}

| Argument/Option | Description                                         |
| --------------- | --------------------------------------------------- |
| `[url]`         | Optional, create a new tab using the specified URL. |
| `--current`     | Optional, create a new tab using the current URL.   |

If neither `[url]` nor `--current` is specified, will use the startup directory to create the tab.

#### `tab_close` {#mgr.tab_close}

| Argument/Option | Description                                     |
| --------------- | ----------------------------------------------- |
| `[n]`           | Close the tab at position `n`, starting from 0. |

If you want to close the current tab, use the [`close`](/docs/configuration/keymap/#mgr.close) action instead.

#### `tab_switch` {#mgr.tab_switch}

| Argument/Option | Description                                                                                                              |
| --------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `[n]`           | Switch to the tab at position `n`, starting from 0.                                                                      |
| `--relative`    | Switch to the tab at a position relative to the current tab. The value of `n` can be negative when using this parameter. |

#### `tab_swap` {#mgr.tab_swap}

| Argument/Option | Description                                                                                                                          |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `[n]`           | Swap the current tab with the tab at position `n`, where negative values move the tab forward, and positive values move it backward. |

#### `help` {#mgr.help}

Open the help menu.

#### `plugin` {#mgr.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#mgr.noop}

If you want to disable certain preset keybindings without rewriting the entire `keymap`, you can use the virtual `noop` action.

For example, to disable the default keybinding of <kbd>g</kbd> ⇒ <kbd>c</kbd>, use:

```toml
[[mgr.prepend_keymap]]
on  = [ "g", "c" ]
run = "noop"
```

Or, if you prefer an array style:

```toml
[[mgr.prepend_keymap]]
on  = [ "g", "c" ]
run = [ "noop" ]  # The array can only have one element and must be "noop"
```

The disabled keys won't trigger any actions when pressed and won't show up in the `which` component.

### [tasks] {#tasks}

#### `show` {#tasks.show}

Show the task manager.

#### `close` {#tasks.close}

Hide the task manager.

#### `arrow` {#tasks.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `inspect` {#tasks.inspect}

Inspect the task log:

- I/O error for failed file operations
- Lua error for failed async plugin tasks
- Real-time stdout/stderr for background running or failed shell tasks

press `q` to exit the inspect view.

#### `cancel` {#tasks.cancel}

Cancel the task.

#### `help` {#tasks.help}

Open the help menu.

#### `plugin` {#tasks.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#tasks.noop}

See [`noop` action](#mgr.noop).

### [spot] {#spot}

#### `close` {#spot.close}

Hide the spotter.

#### `arrow` {#spot.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `swipe` {#spot.swipe}

| Argument/Option | Description                                                                                  |
| --------------- | -------------------------------------------------------------------------------------------- |
| `[n]`           | Swipe `n` files up or down in the file list. Negative value for up, positive value for down. |

#### `copy` {#spot.copy}

Copy the content from the spotter.

| Argument/Option | Description                  |
| --------------- | ---------------------------- |
| `"cell"`        | Copy the selected table cell |

#### `plugin` {#spot.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#spot.noop}

See [`noop` action](#mgr.noop).

#### `help` {#spot.help}

Open the help menu.

### [pick] {#pick}

#### `close` {#pick.close}

Cancel the picker.

| Argument/Option | Description        |
| --------------- | ------------------ |
| `--submit`      | Submit the picker. |

#### `arrow` {#pick.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `help` {#pick.help}

Open the help menu.

#### `plugin` {#pick.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#pick.noop}

See [`noop` action](#mgr.noop).

### [input] {#input}

#### `close` {#input.close}

Cancel input.

| Argument/Option | Description       |
| --------------- | ----------------- |
| `--submit`      | Submit the input. |

#### `escape` {#input.escape}

Go back the normal mode, or cancel input.

#### `move` {#input.move}

Move the cursor left or right.

| Argument/Option  | Description                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| `[n]`            | Move the cursor `n` characters left or right. Negative value for left, positive value for right. |
| `--in-operating` | Move the cursor only if it's currently waiting for an operation.                                 |

#### `backward` {#input.backward}

Move back to the start of the current or previous word.

#### `forward` {#input.forward}

Move forward to the start of the next word.

| Argument/Option | Description                                          |
| --------------- | ---------------------------------------------------- |
| `--end-of-word` | Move forward to the end of the current or next word. |

#### `insert` {#input.insert}

Enter insert mode. This action is only available in normal mode.

| Argument/Option | Description              |
| --------------- | ------------------------ |
| `--append`      | Insert after the cursor. |

#### `visual` {#input.visual}

Enter visual mode. This action is only available in normal mode.

#### `delete` {#input.delete}

Delete the selected characters. This action is only available in normal mode.

| Argument/Option | Description                                                                |
| --------------- | -------------------------------------------------------------------------- |
| `--cut`         | Cut the selected characters into clipboard, instead of only deleting them. |
| `--insert`      | Delete and enter insert mode.                                              |

#### `yank` {#input.yank}

Copy the selected characters. This action is only available in normal mode.

#### `paste` {#input.paste}

Paste the copied characters after the cursor. This action is only available in normal mode.

| Argument/Option | Description                                    |
| --------------- | ---------------------------------------------- |
| `--before`      | Paste the copied characters before the cursor. |

#### `undo` {#input.undo}

Undo the last operation. This action is only available in normal mode.

#### `redo` {#input.redo}

Redo the last operation. This action is only available in normal mode.

#### `help` {#input.help}

Open the help menu. This action is only available in normal mode.

#### `backspace` {#input.backspace}

Delete the character before the cursor. This action is only available in insert mode.

| Argument/Option | Description                            |
| --------------- | -------------------------------------- |
| `--under`       | Delete the character under the cursor. |

#### `kill` {#input.kill}

Kill the specified range of characters. This action is only available in insert mode.

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `"bol"`         | Kill backwards to the BOL.                       |
| `"eol"`         | Kill forwards to the EOL.                        |
| `"backward"`    | Kill backwards to the start of the current word. |
| `"forward"`     | Kill forwards to the end of the current word.    |

#### `plugin` {#input.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin). This action is only available in normal mode.

#### `noop` {#input.noop}

See [`noop` action](#mgr.noop).

### [confirm] {#confirm}

#### `close` {#confirm.close}

Cancel and close the confirmation dialog.

| Argument/Option | Description              |
| --------------- | ------------------------ |
| `--submit`      | Submit the confirmation. |

#### `arrow` {#confirm.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `help` {#confirm.help}

Open the help menu.

### [cmp] {#cmp}

#### `close` {#cmp.close}

Hide the completion menu.

| Argument/Option | Description            |
| --------------- | ---------------------- |
| `--submit`      | Submit the completion. |

#### `arrow` {#cmp.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `help` {#cmp.help}

Open the help menu.

#### `plugin` {#cmp.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#cmp.noop}

See [`noop` action](#mgr.noop).

### [help] {#help}

#### `close` {#help.close}

Hide the help menu.

#### `escape` {#help.escape}

Clear the filter, or hide the help menu.

#### `arrow` {#help.arrow}

| Argument/Option | Description                                      |
| --------------- | ------------------------------------------------ |
| `[steps]`       | The number of steps the cursor moves up or down. |

`[steps]` can be one of the following values:

| Value    | Description                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `n`      | Move the cursor `n` lines up or down, negative for up, positive for down.                 |
| `n%`     | Move the cursor `n%` of the screen height up or down, negative for up, positive for down. |
| `"top"`  | Move the cursor to the top (first item).                                                  |
| `"bot"`  | Move the cursor to the bottom (last item).                                                |
| `"prev"` | Go to the previous item, or the bottom if the cursor is at the top.                       |
| `"next"` | Go to the next item, or the top if the cursor is at the bottom.                           |

The `arrow prev`/`arrow next` actions are similar to `arrow -1`/`arrow 1`, except that the former supports wraparound scrolling.

#### `filter` {#help.filter}

Apply a filter for the help items.

#### `plugin` {#help.plugin}

See [Functional plugin](/docs/plugins/overview#functional-plugin).

#### `noop` {#help.noop}

See [`noop` action](#mgr.noop).

---

## theme.toml

:::tip
If you're looking for ready-made themes and don't want to create one yourself, check out the [yazi-rs/flavors](https://github.com/yazi-rs/flavors) repository.
:::

### Types {#types}

#### Color {#types.color}

A color. It can be in Hex format with RGB values, such as `"#484D66"`. Or can be one of the following 17 values:

- `"reset"`
- `"black"`
- `"white"`
- `"red"`
- `"lightred"`
- `"green"`
- `"lightgreen"`
- `"yellow"`
- `"lightyellow"`
- `"blue"`
- `"lightblue"`
- `"magenta"`
- `"lightmagenta"`
- `"cyan"`
- `"lightcyan"`
- `"gray"`
- `"darkgray"`

#### Style {#types.style}

Appears in a format similar to `{ fg = "#e4e4e4", bg = "black", ... }`, and supports the following properties:

- fg (Color): Foreground color
- bg (Color): Background color
- bold (Boolean): Bold
- dim (Boolean): Dim (not supported by all terminals)
- italic (Boolean): Italic
- underline (Boolean): Underline
- blink (Boolean): Blink
- blink_rapid (Boolean): Rapid blink
- reversed (Boolean): Reversed foreground and background colors
- hidden (Boolean): Hidden
- crossed (Boolean): Crossed out

### [flavor] {#flavor}

See [flavor documentation](/docs/flavors/overview) for more details.

#### `dark` {#flavor.dark}

Flavor name used in dark mode, e.g. `"dracula"`.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `light` {#flavor.light}

Flavor name used in light mode, e.g. `"gruvbox"`.

|      |          |
| ---- | -------- |
| Type | `string` |

### [app] {#app}

#### `overall` {#app.overall}

The app's overall style.

Only the `bg` property is available to set the terminal background color, which requires your terminal to support OSC 11, for example:

```toml
overall = { bg = "#1e1e2e" }
```

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [mgr] {#mgr}

#### `cwd` {#mgr.cwd}

CWD text style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `find_keyword` {#mgr.find_keyword}

Style of the highlighted portion in the filename.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `find_position` {#mgr.find_position}

Style of current file location in all found files to the right of the filename.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `symlink_target` {#mgr.symlink_target}

Style for the path that a symbolic link points to, e.g., the ` -> /path/to/target` part in `my_symbolic_file -> /path/to/target`.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `marker_copied` {#mgr.marker_copied}

Copied file marker style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `marker_cut` {#mgr.marker_cut}

Cut file marker style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `marker_marked` {#mgr.marker_marked}

Marker style of pre-selected file in visual mode.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `marker_selected` {#mgr.marker_selected}

Selected file marker style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `count_copied` {#mgr.count_copied}

Style of copied file number.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `count_cut` {#mgr.count_cut}

Style of cut file number.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `count_selected` {#mgr.count_selected}

Style of selected file number.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `border_symbol` {#mgr.border_symbol}

Border symbol, e.g. `"│"`.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `border_style` {#mgr.border_style}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `syntect_theme` {#mgr.syntect_theme}

Code preview highlighting themes, which are paths to `.tmTheme` files. You can find them on GitHub [using "tmTheme" as a keyword](https://github.com/search?q=tmTheme&type=repositories)

For example, `"~/Downloads/Dracula.tmTheme"`, not available after using a flavor, as flavors always use their own tmTheme files `tmtheme.xml`.

|      |          |
| ---- | -------- |
| Type | `string` |

### [indicator]

#### `parent` {#indicator.parent}

Indicator bar style, in the parent pane.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `current` {#indicator.current}

Indicator bar style, in the current pane.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `preview` {#indicator.preview}

Indicator bar style, in the preview pane.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `padding` {#indicator.padding}

Padding around indicator bar, e.g. `{ open = "▐", close = "▌" }`, which makes a square indicator.

|      |                                   |
| ---- | --------------------------------- |
| Type | `{ open: string, close: string }` |

### [tabs] {#tabs}

<details>
	<summary>Explanation of `active` and `inactive`</summary>
	<img src="/webp/tabs-active-explain.webp" loading="lazy" />
</details>

#### `active` {#tabs.active}

Active tab style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `inactive` {#tabs.inactive}

Inactive tab style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `sep_inner` {#tabs.sep_inner}

Inner separator symbol, e.g. `{ open = "[", close = "]" }`.

|      |                                   |
| ---- | --------------------------------- |
| Type | `{ open: string, close: string }` |

#### `sep_outer` {#tabs.sep_outer}

Outer separator symbol, e.g. `{ open = "", close = "" }`.

|      |                                   |
| ---- | --------------------------------- |
| Type | `{ open: string, close: string }` |

### [mode] {#mode}

#### `normal_main` {#mode.normal_main}

Normal mode main style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `normal_alt` {#mode.normal_alt}

Normal mode alternative style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `select_main` {#mode.select_main}

Select mode main style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `select_alt` {#mode.select_alt}

Select mode alternative style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `unset_main` {#mode.unset_main}

Unset mode main style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `unset_alt` {#mode.unset_alt}

Unset mode alternative style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [status] {#status}

<details>
	<summary>Explanation of `sep_left` and `sep_right`</summary>
	<img src="/webp/status-sep-explain.webp" loading="lazy" />
</details>

#### `overall` {#status.overall}

Overall status bar style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `sep_left` {#status.sep_left}

Left separator symbol, e.g. `{ open = "", close = "]" }`.

|      |                                   |
| ---- | --------------------------------- |
| Type | `{ open: string, close: string }` |

#### `sep_right` {#status.sep_right}

Right separator symbol, e.g. `{ open = "[", close = "" }`.

|      |                                   |
| ---- | --------------------------------- |
| Type | `{ open: string, close: string }` |

#### `perm_type` {#status.perm_type}

Style of the file type symbol, such as `d` for directory, `-` for file, `l` for symlink, etc.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `perm_read` {#status.perm_read}

Style of the read permission symbol (`r`).

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `perm_write` {#status.perm_write}

Style of the write permission symbol (`w`).

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `perm_exec` {#status.perm_exec}

Style of the execute permission symbol (`x`).

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `perm_sep` {#status.perm_sep}

Style of the permission separator symbol (`-`).

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `progress_label` {#status.progress_label}

Progress label style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `progress_normal` {#status.progress_normal}

Style of the progress bar when it is not in an error state.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `progress_error` {#status.progress_error}

Style of the progress bar when an error occurs.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [which] {#which}

#### `cols` {#which.cols}

Number of columns.

|      |                   |
| ---- | ----------------- |
| Type | `1` \| `2` \| `3` |

#### `mask` {#which.mask}

Mask style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `cand` {#which.cand}

Candidate key style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `rest` {#which.rest}

Rest key style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `desc` {#which.desc}

Description style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `separator` {#which.separator}

Separator symbol, e.g. `" -> "`.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `separator_style` {#which.separator_style}

Separator style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [confirm] {#confirm}

#### `border` {#confirm.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title` {#confirm.title}

Title style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `body` {#confirm.body}

Body style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `list` {#confirm.list}

List style, which is the style of the list of items below the content.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `btn_yes` {#confirm.btn_yes}

The style of the yes button.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `btn_no` {#confirm.btn_no}

The style of the no button.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `btn_labels` {#confirm.btn_labels}

Labels for the yes and no buttons.

The first string is the label for the yes button and the second is the label for the no button.

|      |                    |
| ---- | ------------------ |
| Type | `[string, string]` |

### [spot] {#spot}

<details>
	<summary>Explanation of `tbl_col` and `tbl_cell`</summary>
	<img src="/webp/spot-tbl-explain.webp" loading="lazy" />
</details>

#### `border` {#spot.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title` {#spot.title}

Title style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `tbl_col` {#spot.tbl_col}

The style of the selected column in the table.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `tbl_cell` {#spot.tbl_cell}

The style of the selected cell in the table.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [notify] {#notify}

#### `title_info` {#notify.title_info}

Style of the info title.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title_warn` {#notify.title_warn}

Style of the warning title.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title_error` {#notify.title_error}

Style of the error title.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [pick] {#pick}

#### `border` {#pick.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `active` {#pick.active}

Selected item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `inactive` {#pick.inactive}

Unselected item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [input] {#input}

#### `border` {#input.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title` {#input.title}

Title style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `value` {#input.value}

Value style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `selected` {#input.selected}

Selected value style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [cmp] {#cmp}

#### `border` {#cmp.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `active` {#cmp.active}

Selected item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `inactive` {#cmp.inactive}

Unselected item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `icon_file` {#cmp.icon_file}

File icon.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `icon_folder` {#cmp.icon_folder}

Folder icon.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `icon_command` {#cmp.icon_command}

Command icon.

|      |          |
| ---- | -------- |
| Type | `string` |

### [tasks] {#tasks}

#### `border` {#tasks.border}

Border style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `title` {#tasks.title}

Title style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `hovered` {#tasks.hovered}

Hovered item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

### [help] {#help}

#### `on` {#help.on}

Key column style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `run` {#help.run}

Action column style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `desc` {#help.desc}

Description column style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `hovered` {#help.hovered}

Hovered item style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `footer` {#help.footer}

Footer style.

|      |                         |
| ---- | ----------------------- |
| Type | [`Style`](#types.style) |

#### `icon_info` {#help.icon_info}

Info icon.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `icon_warn` {#help.icon_warn}

Warning icon.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `icon_error` {#help.icon_error}

Error icon.

|      |          |
| ---- | -------- |
| Type | `string` |

### [filetype] {#filetype}

Set file list item display styles for specific file types, supporting matching by name and mime-type:

```toml
[filetype]
rules = [
	# Image
	{ mime = "image/*", fg = "yellow" },
	# Video
	{ mime = "{audio,video}/*", fg = "magenta" },
	# Empty file
	{ mime = "inode/empty", fg = "cyan" },
	# Orphan symbolic links
	{ url = "*", is = "orphan", fg = "red" },
	# Fallback
	# { url = "*", fg = "white" },
	{ url = "*/", fg = "blue" }
]
```

Each rule supports complete [Style properties](#types.style). There are two special rule:

- `url = "*"` matches all files.
- `url = "*/"` matches all directories.

You can restrict the specific type of files through `is`, noting that it must be used with either `url` or `mime`. It accepts the following values:

- `block`: Block device
- `char`: Char device
- `exec`: Executable
- `fifo`: FIFO
- `link`: Symbolic link
- `orphan`: Orphan symbolic link
- `sock`: Socket
- `sticky`: File with sticky bit set

### [icon] {#icon}

Yazi has builtin support for [nvim-web-devicons](https://github.com/nvim-tree/nvim-web-devicons), a rich set of icons ready to use.
If you want to add your own rules to this set, you can use `prepend_*` and `append_*` to prepend or append rules to the default ones (see [Configuration Mixing](/docs/configuration/overview#mixing) for details):

```toml
[icon]
prepend_dirs = [
	{ name = "Desktop", text = "", fg = "#563d7c" },
	# ...
]
append_exts = [
	{ name = "mp3", text = "", fg = "#00afff" },
	# ...
]
## ...
```

If you want to completely override the default rules, you can do so with:

```toml
[icon]
dirs = [
	{ name = "Desktop", text = "", fg = "#563d7c" },
	# ...
]
exts = [
	{ name = "mp3", text = "", fg = "#00afff" },
	# ...
]
## ...
```

Each icon rule contains the following properties:

- `name` (globs, dirs, files, exts), or `if` (conds): the rule itself, which is a string
- `text`: icon text, which is a string
- `fg`: icon color, which is a [Color](/docs/configuration/theme#types.color)

Icons are matched according to the following priority:

1. globs: glob expressions, e.g., `{ url = "**/Downloads/*.zip", ... }`
2. dirs: directory names, e.g., `{ name = "Desktop", ... }`
3. files: file names, e.g., `{ name = ".bashrc", ... }`
4. exts: extensions, e.g., `{ name = "mp3", ... }`
5. conds: conditions, e.g., `{ if = "!dir", ... }`

`dirs`, `files`, and `exts` are compiled into a HashMap at startup, offering O(1) time complexity for very fast lookups, which should meet most needs.

For more complex and precise rules, such as matching a specific file in a specific directory, use `globs` - these are always executed first to check if any rules in the glob set are met.
However, they are much slower than `dirs`, `files`, and `exts`, so it's not recommended to use them excessively.

If none of the above rules match, it will fall back to `conds` to check if any specific conditions are met. `conds` are mostly used for rules related to file metadata, which includes the following conditional factors:

- `dir`: The file is a directory
- `hidden`: The file is hidden
- `link`: The file is a symbolic link
- `orphan`: The file is an orphan (broken symbolic link)
- `dummy`: The file is dummy (failed to load complete metadata, possibly the filesystem doesn't support it, such as FUSE)
- `block`: The file is a block device
- `char`: The file is a char device
- `fifo`: The file is a FIFO
- `sock`: The file is a socket
- `exec`: The file is executable
- `sticky`: The file has the sticky bit set

These conditions support basic `|` (or), `&` (and), `!` (not), and `()` for priority, so you can combine them as needed, for example:

```toml
[icon]
prepend_conds = [
	{ if = "hidden & dir",  text = "👻" },  # Hidden directories
	{ if = "dir",           text = "📁" },  # Directories
	{ if = "!(dir | link)", text = "📄" },  # Normal files (not directories or symlinks)
]
```

---

## vfs.toml

:::info
If you want to fine-tune the default settings, the first step is to [create your own configuration file](/docs/configuration/overview).
:::

You can register any supported VFS provider in your `vfs.toml` as a service, for example:

```toml
[services.my-server]
type = "sftp"
host = "1.2.3.4"
user = "root"
port = 22
```

The service here is `my-server`, you can use any other name you like in [kebab-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case), up to 20 characters.

Different names are considered as different virtual filesystems, even if they are configured with the same provider and exactly the same parameters.

### Usage

Once registered, you can access them by the combination of provider type and name, for example, to start Yazi with the SFTP service `my-server` as the working directory:

```sh
yazi sftp://my-server
```

You can also reference them from Yazi's [built-in actions](/docs/configuration/keymap) in `keymap.toml`, for example the [`cd`](/docs/configuration/keymap#mgr.cd) action:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "s" ]
run  = "cd sftp://my-server"
desc = "Go to my-server"
```

Or the [`reveal`](/docs/configuration/keymap#mgr.reveal) action:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "s" ]
run  = "reveal sftp://my-server//root/dog.jpg"
desc = "Reveal dog.jpg on my-server"
```

### SFTP Provider

Yazi has an SFTP VFS provider built-in, which means you can manage files on remote servers over SSH.

To register an SFTP VFS named `my-server`, add the following to your `vfs.toml`:

```toml
[services.my-server]
type = "sftp"
host = "1.2.3.4"
user = "root"
port = 22
```

This configures Yazi to log in to `1.2.3.4` on port `22` as the `root` user and authenticate via your SSH agent by connecting to the socket specified in the `$SSH_AUTH_SOCK` environment variable.

On Unix-like systems the SSH agent is provided by `ssh-agent`. You can list the keys the agent has loaded with `ssh-add -l`, or add keys with `ssh-add`, e.g. `ssh-add ~/.ssh/id_rsa`.

If you don't want to use an agent and prefer to specify a private key file, add the `key_file` and `key_passphrase` options, for example:

```toml
[services.my-server]
type     = "sftp"
host     = "1.2.3.4"
user     = "root"
port     = 22
key_file = "~/.ssh/id_rsa"
## If your private key is protected by a passphrase:
## key_passphrase = "my_passphrase"
```

You can also authenticate with a password using the `password` option:

```toml
[services.my-server]
type     = "sftp"
host     = "1.2.3.4"
user     = "root"
port     = 22
password = "my_password"
```

If you want to use an agent socket other than `$SSH_AUTH_SOCK`, for example, if you [manage SSH keys with 1Password](https://developer.1password.com/docs/ssh/manage-keys/), specify it with `identity_agent`:

```toml
[services.my-server]
type           = "sftp"
host           = "1.2.3.4"
user           = "root"
port           = 22
identity_agent = "~/Library/Group Containers/2BUA8C4S2C.com.1password/t/agent.sock"
```

---

## Image Preview

Yazi has done a lot of work to adapt to different terminals and multiplexers, aiming to provide an out-of-the-box experience for users.

This is by no means a simple task. To reduce maintenance costs, we only guarantee support in the **_latest versions_** of terminals and multiplexers (tmux, Zellij):

| Platform                                                                     | Protocol                               | Support                                  |
| ---------------------------------------------------------------------------- | -------------------------------------- | ---------------------------------------- |
| [kitty](https://github.com/kovidgoyal/kitty) (>= 0.28.0)                     | [Kitty unicode placeholders][kgp]      | ✅ Built-in                              |
| [iTerm2](https://iterm2.com)                                                 | [Inline images protocol][iip]          | ✅ Built-in                              |
| [WezTerm](https://github.com/wez/wezterm)                                    | [Inline images protocol][iip]          | ✅ Built-in                              |
| [Konsole](https://invent.kde.org/utilities/konsole)                          | [Kitty old protocol][kgp-old]          | ✅ Built-in                              |
| [foot](https://codeberg.org/dnkl/foot)                                       | [Sixel graphics format][sixel]         | ✅ Built-in                              |
| [Ghostty](https://github.com/ghostty-org/ghostty)                            | [Kitty unicode placeholders][kgp]      | ✅ Built-in                              |
| [Windows Terminal](https://github.com/microsoft/terminal) (>= v1.22.10352.0) | [Sixel graphics format][sixel]         | ✅ Built-in                              |
| [st with Sixel patch](https://github.com/bakkeby/st-flexipatch)              | [Sixel graphics format][sixel]         | ✅ Built-in                              |
| [Warp](https://www.warp.dev) (macOS/Linux only)                              | [Inline images protocol][iip]          | ✅ Built-in                              |
| [Tabby](https://github.com/Eugeny/tabby)                                     | [Inline images protocol][iip]          | ✅ Built-in                              |
| [VSCode](https://github.com/microsoft/vscode)                                | [Inline images protocol][iip]          | ✅ Built-in                              |
| [Rio](https://github.com/raphamorim/rio)                                     | [Inline images protocol][iip]          | ❌ Rio renders images at incorrect sizes |
| [Black Box](https://gitlab.gnome.org/raggesilver/blackbox)                   | [Sixel graphics format][sixel]         | ✅ Built-in                              |
| [Bobcat](https://github.com/ismail-yilmaz/Bobcat)                            | [Inline images protocol][iip]          | ✅ Built-in                              |
| X11 / Wayland                                                                | Window system protocol                 | ☑️ [Überzug++][ueberzug] required        |
| Fallback                                                                     | [ASCII art (Unicode block)][ascii-art] | ☑️ [Chafa][chafa] required (>= 1.16.0)   |

Yazi automatically selects the appropriate preview method for you, based on the priority from top to bottom.
That's relying on the `$TERM`, `$TERM_PROGRAM`, and `$XDG_SESSION_TYPE` variables, make sure you don't overwrite them by mistake!

For instance, if your terminal is Alacritty, which doesn't support displaying images itself, but you are running on an X11/Wayland environment,
it will automatically use the "Window system protocol" to display images - this requires you to have Überzug++ installed.

<!-- Protocols -->

[kgp]: https://sw.kovidgoyal.net/kitty/graphics-protocol/#unicode-placeholders
[kgp-old]: https://github.com/sxyazi/yazi/blob/main/yazi-adapter/src/drivers/kgp_old.rs
[iip]: https://iterm2.com/documentation-images.html
[sixel]: https://www.vt100.net/docs/vt3xx-gp/chapter14.html
[ascii-art]: https://en.wikipedia.org/wiki/ASCII_art

<!-- Dependencies -->

[ueberzug]: https://github.com/jstkdng/ueberzugpp
[chafa]: https://hpjansson.org/chafa/

### tmux users {#tmux}

To enable Yazi's image preview to work correctly in tmux, add the following 3 options to your `tmux.conf`:

```sh
set -g allow-passthrough on
set -ga update-environment TERM
set -ga update-environment TERM_PROGRAM
```

Then restart tmux (important):

```sh
tmux kill-server && tmux || tmux
```

Now you should be able to enjoy with the image preview.

Note that if [the protocol you are using](#protocol) is Sixel, make sure you passed `--enable-sixel` when building tmux, as it's disabled by default.
You can verify this through [tmux/tmux#4104](https://github.com/tmux/tmux/issues/4104#issuecomment-2326339395).

### Zellij users {#zellij}

Zellij currently only supports the Sixel graphics format, so you will need a terminal that also supports Sixel.

Note that, Zellij's Sixel implementation is quite buggy and has serious performance issues at the moment,
causing noticeable lagginess when quickly switching between images, and sometimes even [image tearing](https://github.com/zellij-org/zellij/issues/2576#issuecomment-1707107473) or [not working at all](https://github.com/zellij-org/zellij/issues/2814#issuecomment-2318473921).

This situation won't improve until Zellij enhances its Sixel implementation or [provides a passthrough mode](https://github.com/zellij-org/zellij/issues/775). If the image is a stronger need to you, consider running Yazi outside of Zellij or using Überzug++:

```sh
## Deceive Yazi into thinking you're running in kitty,
## forcing it fallback to Überzug++ or Chafa
TERM=xterm-kitty yazi
```

### Windows users {#windows}

Currently, only the following 3 terminals support displaying images on Windows:

- [WezTerm](https://wezterm.org/install/windows.html) (latest nightly)
- [Windows Terminal](https://github.com/microsoft/terminal/releases) (>= v1.22.10352.0)
- [Bobcat v0.9.0](https://github.com/ismail-yilmaz/Bobcat/releases/tag/0.9.0)

### Windows with WSL users {#wsl}

Limited by ConPTY, the Windows edition has had to implement many workarounds, which are not perfect.

However, if you run Yazi in WSL, you can experience perfect image previews through [`wezterm ssh`][wezterm-ssh].<br/>
[WezTerm][wezterm] is an excellent terminal that can bypass the limitations of ConPTY through its SSH feature, and it's currently the only terminal that allows this approach.

You need to install `sshd` in WSL and start it:

```sh
sudo apt install openssh-server
sudo service ssh restart
```

Then, on the _host_ machine, connect to WSL over SSH:

```sh
wezterm ssh 127.0.0.1
```

That's it! you can now get Yazi's image preview working properly.

[wezterm]: https://wezfurlong.org/wezterm/
[wezterm-ssh]: https://wezfurlong.org/wezterm/cli/ssh.html

### Neovim users {#neovim}

The builtin terminal emulator (`:term`) in Neovim [doesn't support any graphic protocols](https://github.com/neovim/neovim/issues/4349), so Yazi will try to fallback to X11/Wayland/Chafa in sequence.

Note that Überzug++ might display images in the wrong position; in that case, please adjust it manually using [`ueberzug_offset`](/docs/configuration/yazi/#preview.ueberzug_scale).

### Why won't my images adapt to terminal size? {#size}

The size of the image depends on two factors:

1. The [max_width](/docs/configuration/yazi#preview.max_width) and [max_height](/docs/configuration/yazi#preview.max_height) config options, which need to be adjusted by the user as needed.
2. The pixel size of the terminal.

Yazi will use the smaller of these two factors as the image preview size.

However, some terminals (such as VSCode, Tabby, and all Windows terminals) don't implement the `ioctl` system call, before [Add `CSI 14 t` sequence support](https://github.com/crossterm-rs/crossterm/pull/810) is merged, it's not possible to obtain the actual pixel width and height of the terminal.

Hence, only `max_width` and `max_height` will be used in this case.

### How can I know what image protocol Yazi uses? {#protocol}

Yazi provides a `yazi --debug` command that includes all your environment information, such as terminal emulator, image adapter, whether you're in SSH mode, etc.

Run it in the terminal where you want to preview images, and you'll see output like:

```sh
...
Adapter
    Adapter.matches: Kgp
...
```

which indicates the image protocol detected and used by Yazi:

| `Adapter.matches` | Protocol                               | Notes                                                                                                |
| ----------------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `Kgp`             | [Kitty unicode placeholders][kgp]      | Ensure your terminal is up-to-date to support it                                                     |
| `KgpOld`          | [Kitty old protocol][kgp-old]          | Doesn't work under `tmux` due to the limitations of the protocol itself                              |
| `Iip`             | [Inline images protocol][iip]          | -                                                                                                    |
| `Sixel`           | [Sixel graphics format][sixel]         | See [tmux](#tmux) and [Zellij](#zellij) section if you're using either of them                       |
| `X11`             | Window system protocol                 | [Überzug++][ueberzug] is required                                                                    |
| `Wayland`         | Window system protocol                 | [Überzug++][ueberzug] is required and [_only_ supports Sway, Hyprland, and Wayfire][uberzug-wayland] |
| `Chafa`           | [ASCII art (Unicode block)][ascii-art] | [Chafa][chafa] is required as the last fallback resort                                               |

[uberzug-wayland]: https://github.com/jstkdng/ueberzugpp/blob/eea57daece774e152aedba9ac82a8113056fbab4/README.md?plain=1#L12

### Why can't I preview images via Überzug++? {#debug-ueberzug}

This may be a problem with Überzug++ itself. Please [run Yazi in debug mode](/docs/plugins/overview#logging), then hover over the image that's causing the issue.

Then find the last Überzug++ command in your log file sorted by time, it is usually at the very end of the file and looks like:

```
ueberzugpp command: {"action":"add","identifier":"yazi","x":96,"y":1,"max_width":400,"max_height":150,"path":"/root/test.jpg"}
```

Finally, run `ueberzugpp layer` directly in the terminal without and outside Yazi, and paste the command:

```sh
{"action":"add","identifier":"yazi","x":96,"y":1,"max_width":400,"max_height":150,"path":"/root/test.jpg"}
```

into it, press `Enter`, and to see if any image is shown, without exiting the Überzug++.

If the image shows properly when using Überzug++ independently, but not when used with Yazi, please create a bug report with:

- The contents of your log file.
- The contents of `/tmp/ueberzugpp-$USER.log`.
- A GIF demonstration of the above steps.

---

## Plugins (BETA)

You can extend Yazi's functionality through Lua plugins, which need to be placed in the `plugins` subdirectory of Yazi's configuration directory, so either:

- `~/.config/yazi/plugins/` on Unix-like systems.
- `%AppData%\yazi\config\plugins\` on Windows.

```
~/.config/yazi/
├── init.lua
├── plugins/
│   ├── foo.yazi/
│   └── bar.yazi/
└── yazi.toml
```

Each plugin is a directory with a [kebab-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case) name, ending in `.yazi`, and containing at least the following files:

```
~/.config/yazi/plugins/bar.yazi/
├── main.lua
├── README.md
└── LICENSE
```

Where:

- `main.lua` is the entry point of this plugin.
- `README.md` is the documentation of this plugin.
- `LICENSE` is the license file for this plugin.

### Usage {#usage}

A plugin has two usages:

- [Functional plugin](#functional-plugin): Bind the `plugin` action to a key in `keymap.toml`, and activate it by pressing the key.
- [Custom previewers, preloaders](/docs/configuration/yazi#plugin): Configure them as previewers or preloaders under `[plugin]` of your `yazi.toml`.

#### Functional plugin {#functional-plugin}

You can bind a `plugin` action to a specific key in your `keymap.toml` with:

| Argument/Option | Description                                           |
| --------------- | ----------------------------------------------------- |
| `[name]`        | Required, the name of the plugin to run.              |
| `[args]`        | Optional, shell-style arguments passed to the plugin. |

For example, `plugin test -- foo --bar --baz=qux` will run the `test` plugin with the arguments `foo --bar --baz=qux` in an async context.

To access the arguments in the plugin, use `job.args`:

```lua
-- ~/.config/yazi/plugins/test.yazi/main.lua
return {
	entry = function(self, job)
		ya.dbg(job.args[1])  -- "foo"
		ya.dbg(job.args.bar) -- true
		ya.dbg(job.args.baz) -- "qux"
	end,
}
```

Note that currently Yazi only supports positional arguments (`foo`) and named arguments (`--bar`), it does not support shorthand arguments like `-a`.

Shorthands will be treated as positional arguments at the moment, but as Yazi adds support for it in the future, their behavior will change. So please avoid using them to prevent any potential conflicts.

### Sync vs Async {#sync-vs-async}

The plugin system is designed with an async-first philosophy. Therefore, unless specifically specified, such as the [`@sync` annotation](/docs/plugins/overview#@sync), all plugins run in an async context.

There is one exception: the user's `init.lua` is synchronous, since `init.lua` is often used to initialize plugin configurations:

```lua
-- ~/.config/yazi/init.lua
require("my-plugin"):setup {
	key1 = "value1",
	key2 = "value2",
	-- ...
}
```

```lua
-- ~/.config/yazi/plugins/my-plugin.yazi/main.lua
return {
	setup = function(state, opts)
		-- Save the user configuration to the plugin's state
		state.key1 = opts.key1
		state.key2 = opts.key2
	end,
}
```

#### Sync context {#sync-context}

The sync context accompanies the entire app lifecycle, which is active during UI rendering (UI plugins), and on executing [sync functional plugins](/docs/plugins/overview#@sync).

For better performance, the sync context is created only at the app's start and remains singular throughout. Thus, plugins running within this context share states,
prompting plugin developers to use plugin-specific state persistence for their plugins to prevent global space contamination:

```lua
--- @sync entry
-- ~/.config/yazi/test.yazi/main.lua
return {
  entry = function(state)
    state.i = state.i or 0
    ya.dbg("i = " .. state.i)

    state.i = state.i + 1
  end,
}
```

Yazi initializes the `state` for each _sync_ plugin before running, and it exists independently for them throughout the entire lifecycle.
Do the `plugin test` three times, and you will see the log output:

```sh
i = 0
i = 1
i = 2
```

#### Async context {#async-context}

When a plugin is executed asynchronously, an isolated async context is created for it automatically.

In this context, you can use all the async functions supported by Yazi, and it operates concurrently with the main thread, ensuring that the main thread is not blocked.

You can also obtain [a small amount](#sendable) of data from the sync context by calling a "sync block":

```lua
-- ~/.config/yazi/plugins/my-async-plugin.yazi/main.lua
local set_state = ya.sync(function(state, a)
	-- You can get/set the state of the plugin through `state` parameter
	-- in the `sync()` block
	state.a = a
end)

local get_state = ya.sync(function(state, b)
	-- You can access all states through the `cx`,
	-- within the `sync()` block, in an async plugin
	local h = cx.active.current.hovered
	return h and state.a .. tostring(h.url) or b
end)

return {
	entry = function()
		set_state("hello from a")
		local h = get_state("hello from b")
		-- Do some time-consuming work, such as reading file, network request, etc.
		-- It will execute concurrently with the main thread
	end,
}
```

Note that `ya.sync()` call must be at the top level:

```lua
-- Wrong !!!
local get_state
if some_condition then
	get_state = ya.sync(function(state)
		-- ...
	end)
end
```

Passing data into and returning data from a `ya.sync()` block involves cross-thread data exchange. If the data contains userdata, it causes [Ownership transfer](/docs/plugins/overview#ownership).

### Annotations {#annotations}

Each plugin can contain zero or more annotations that specify the behavior of the plugin during runtime.

Each annotation starts with `---`, followed by `@` and the annotation name, and ends with the annotation's value.

These annotations _must_ be at the very top of the file, with no content before them, and no non-annotation content should appear between annotations.

#### `@sync` {#@sync}

Specifies that a method in the plugin runs in a sync context instead of the default async context. Available values:

- `entry`: Run the `entry` method in a sync context.
- `peek`: Run the `peek` method in a sync context.

For example:

```lua
--- @sync entry
return {
	entry = function() end
}
```

#### `@since` {#@since}

Specifies the minimum Yazi version that the plugin supports.

If specified, and the user's Yazi version is lower than the specified one, an error will be triggered to prompt the user to upgrade their Yazi version, preventing the plugin from being executed accidentally:

```lua
--- @since 25.2.13
return {
	--- ...
}
```

### Interface {#interface}

#### Previewer {#previewer}

A previewer needs to return a table that implements the `peek` and `seek` methods. Both methods take a table parameter `job` and do not return any values:

```lua
local M = {}

function M:peek(job)
	-- ...
end

function M:seek(job)
	-- ...
end

return M
```

When the user presses <kbd>j</kbd> or <kbd>k</kbd> to switch between hovering files, `peek` is called, with:

| Key    | Description                                                                                                     |
| ------ | --------------------------------------------------------------------------------------------------------------- |
| `area` | [Rect](/docs/plugins/layout#rect) of the available preview area.                                                |
| `args` | Arguments passed to the previewer.                                                                              |
| `file` | [File](/docs/plugins/types#file) to be previewed.                                                               |
| `skip` | Number of units to skip. The units depend on your previewer, such as lines for code and percentages for videos. |

When the user presses <kbd>J</kbd> or <kbd>K</kbd> to scroll the preview of the file, `seek` is called, with:

| Key     | Description                                                      |
| ------- | ---------------------------------------------------------------- |
| `file`  | [File](/docs/plugins/types#file) being scrolled.                 |
| `area`  | [Rect](/docs/plugins/layout#rect) of the available preview area. |
| `units` | Number of units to scroll.                                       |

The task of `peek` is to draw in the preview area based on the values of `file` and `skip`. This process is asynchronous.

The task of `seek` is to change the value of `skip` based on user behavior and trigger `peek` again. It's synchronous, meaning you can access [the context](/docs/plugins/context).

There are some preset previewers and preloaders you can refer to: [Yazi Preset Plugins](https://github.com/sxyazi/yazi/tree/shipped/yazi-plugin/preset/plugins)

#### Preloader {#preloader}

You need to return a table that implements the `preload` method:

```lua
local M = {}

function M:preload(job)
	-- ...
	return false, Err("some error")
end

return M
```

It receives a `job` parameter, which is a table:

| Key    | Description                                                      |
| ------ | ---------------------------------------------------------------- |
| `area` | [Rect](/docs/plugins/layout#rect) of the available preview area. |
| `args` | Arguments passed to the preloader.                               |
| `file` | [File](/docs/plugins/types#file) to be preloaded.                |
| `skip` | Always `0`                                                       |

And returns a `(complete, err)`:

- `complete`: Required, whether the preloading is complete, which is a boolean.
  - `true`: Marks the task as complete, and the task will not be called again.
  - `false`: Marks the task as incomplete, and the task will be retried until it's complete (returns `true`).
- `err`: Optional, the error to be logged.

When `complete = false`, the preloader will be re-triggered at the next time point, such as when the user scrolls leading to a page switch. This is usually done for either:

- Retrying in case of file loading failure
- Refreshing the file status upon successful loading

Yazi will automatically invoke the `preload` concurrently for each file that matches the preload rules on the page.

### Sendable value {#sendable}

Yazi's plugin can run concurrently on multiple threads. For better performance, only the following types of combinations can be used for inter-thread data exchange:

- Nil
- Boolean
- Number
- String
- [Url](/docs/plugins/types#url)
- Table and nested tables, with the above types as values

### Ownership transfer {#ownership}

Yazi's plugin system inherits [Rust's ownership and lifetime](https://doc.rust-lang.org/nomicon/ownership.html) concepts.

All [userdata](https://www.lua.org/pil/28.1.html) are native Rust types that have their own ownership to ensure safe and efficient transfers across different threads, avoiding any memory reallocation overhead. Specifically:

- [Url](/docs/plugins/types#url)

Passing these userdata to a cross-thread function like [`ya.emit()`](/docs/plugins/utils#ya.emit) transfers ownership. After transfer, the original userdata is no longer available, for example:

```lua
local target = Url("/tmp")
ya.emit("cd", { target })  -- Ownership transferred

ya.dbg(tostring(url)) -- Error: userdata has been destructed
```

To keep the original, clone a new userdata and pass that instead, but this allocates extra memory - `Url()` constructor can accept a `Url` userdata and return a new clone of that `Url`:

```diff
- ya.emit("cd", { target })
+ ya.emit("cd", { Url(target) })
```

A smarter way is to reverse the order of execution, use the `target` before it's transferred, to avoid the need for cloning:

```lua
local target = Url("/tmp")
local target_str = tostring(target)

ya.emit("cd", { target })  -- Ownership transferred
ya.dbg(target_str) -- No error
```

### Debugging {#debugging}

Please ensure that your `~/.config/yazi/init.lua` contains valid Lua code with correct syntax; otherwise, Yazi will be unable to parse and execute `init.lua` to initialize.

We recommend installing a Lua plugin in your editor for syntax checking to avoid any syntax errors.
For example, install the [Lua plugin](https://marketplace.visualstudio.com/items?itemName=sumneko.lua) for VSCode, and for Neovim, use [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig) to configure your Lua LSP.

If you have no experience with Lua, you can quickly get started through https://learnxinyminutes.com/docs/lua/

#### Logging {#logging}

If you want to debug some runtime data, use [`ya.dbg()`](/docs/plugins/utils#ya.dbg) and [`ya.err()`](/docs/plugins/utils#ya.err) to print what you want to debug to either:

- `~/.local/state/yazi/yazi.log` on Unix-like systems.
- `%AppData%\yazi\state\yazi.log` on Windows.

Make sure to set the `YAZI_LOG` environment variable before starting Yazi:

<Tabs>
  <TabItem value="unix" label="Unix-like" default>

```sh
YAZI_LOG=debug yazi
```

  </TabItem>

  <TabItem value="powershell" label="PowerShell">

```powershell
$env:YAZI_LOG = "debug"; yazi
```

  </TabItem>
</Tabs>

otherwise, no logs will be recorded. Its value can be (in descending order of verbosity):

- `debug`
- `info`
- `warn`
- `error`

#### Debugging preset plugins

1. Clone the latest source code.
2. Go to the `yazi-plugin/preset` folder and find the plugin you want to debug, make changes, such as [logging certain runtime data](/docs/plugins/overview#logging).
3. [Build in debug mode](/docs/installation#debug) and run the `yazi` binary with an appropriate `YAZI_LOG`.

---

## Types

### Url {#url}

Create a URL:

```lua
-- regular file
local url = Url("/root/Downloads/logo.png")

-- `/root/dog.jpg` on `my-server` via SFTP
local url = Url("sftp://my-server//root/dog.jpg")
```

#### `path` {#url.path}

[`Path`](#path) portion of the URL.

For the URL `sftp://my-server//path/to/file`, the path is `/path/to/file`.

|      |        |
| ---- | ------ |
| Type | `Path` |

#### `name` {#url.name}

Filename of the URL.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `stem` {#url.stem}

Filename without the extension.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `ext` {#url.ext}

Extension of the file.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `parent` {#url.parent}

Parent directory.

|      |         |
| ---- | ------- |
| Type | `Self?` |

#### `domain` {#url.domain}

Domain of the URL.

For the URL `sftp://my-server//root/dog.jpg`, the domain is `my-server`.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `is_regular` {#url.is_regular}

Whether the file represented by the URL is a regular file.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_search`

Whether the file represented by the URL is from a search result.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_archive` {#url.is_archive}

Whether the file represented by the URL is from an archive.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_absolute`

Whether the path represented by the URL is absolute.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `has_root` {#url.has_root}

Whether the path represented by the URL has a root.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `join(self, other)` {#url.join}

Join with `other` to create a new URL.

| In/Out  | Type               |
| ------- | ------------------ |
| `self`  | `Self`             |
| `other` | `Self` \| `string` |
| Return  | `Self`             |

#### `starts_with(self, base)` {#url.starts_with}

Whether the URL starts with `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `boolean`          |

#### `ends_with(self, base)` {#url.ends_with}

Whether the URL ends with `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `boolean`          |

#### `strip_prefix(self, base)` {#url.strip_prefix}

Strips the prefix of `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `Path`             |

#### `__eq(self, other)` {#url.\_\_eq}

Whether the URL is equal to `other`.

| In/Out  | Type      |
| ------- | --------- |
| `self`  | `Self`    |
| `other` | `Self`    |
| Return  | `boolean` |

#### `__tostring(self)` {#url.\_\_tostring}

Convert the URL to string.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `string` |

#### `__concat(self, other)` {#url.\_\_concat}

Concatenate the URL with `other`.

| In/Out  | Type     |
| ------- | -------- |
| `self`  | `Self`   |
| `other` | `string` |
| Return  | `Self`   |

#### `__new(value)` {#url.\_\_new}

Make a new URL.

| In/Out  | Type               |
| ------- | ------------------ |
| `value` | `string` \| `Self` |
| Return  | `Self`             |

### Path {#path}

`Path` is the path portion of a [`Url`](#url).

For the URL `sftp://my-server//path/to/file`, the path is `/path/to/file`.

#### `name` {#path.name}

Filename of the path.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `stem` {#path.stem}

Filename without the extension.

|      |           |
| ---- | --------- |
| Type | `string?` |

#### `parent` {#path.parent}

Parent directory.

|      |         |
| ---- | ------- |
| Type | `Self?` |

#### `is_absolute`

Whether the path is absolute.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `has_root` {#path.has_root}

Whether the path has a root.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `join(self, other)` {#path.join}

Join with `other` to create a new path.

| In/Out  | Type               |
| ------- | ------------------ |
| `self`  | `Self`             |
| `other` | `Self` \| `string` |
| Return  | `Self`             |

#### `starts_with(self, base)` {#path.starts_with}

Whether the path starts with `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `boolean`          |

#### `ends_with(self, base)` {#path.ends_with}

Whether the path ends with `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `boolean`          |

#### `strip_prefix(self, base)` {#path.strip_prefix}

Strips the prefix of `base`.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `base` | `Self` \| `string` |
| Return | `Self`             |

#### `__eq(self, other)` {#path.\_\_eq}

Whether the path is equal to `other`.

| In/Out  | Type      |
| ------- | --------- |
| `self`  | `Self`    |
| `other` | `Self`    |
| Return  | `boolean` |

#### `__tostring(self)` {#path.\_\_tostring}

Convert the path to string.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `string` |

#### `__concat(self, other)` {#path.\_\_concat}

Concatenate the path with `other`.

| In/Out  | Type     |
| ------- | -------- |
| `self`  | `Self`   |
| `other` | `string` |
| Return  | `Self`   |

### Cha {#cha}

One file's characteristics.

#### `is_dir` {#cha.is_dir}

Whether the file is a directory.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_hidden` {#cha.is_hidden}

Whether the file is hidden.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_link` {#cha.is_link}

Whether the file is a symlink.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_orphan` {#cha.is_orphan}

Whether the file is a bad symlink, which points to a non-existent file.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_dummy` {#cha.is_dummy}

Whether the file is dummy, which fails to load complete metadata. It could be due to the file system not supporting it, such as FUSE.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_block` {#cha.is_block}

Whether the file is a block device.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_char` {#cha.is_char}

Whether the file is a character device.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_fifo` {#cha.is_fifo}

Whether the file is a FIFO.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_sock` {#cha.is_sock}

Whether the file is a socket.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_exec` {#cha.is_exec}

Whether the file is executable.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_sticky` {#cha.is_sticky}

Whether the file has the sticky bit set.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `len` {#cha.len}

Length of the file in bytes.

If you want to get the size of a directory, use [`size()`](/docs/plugins/context#fs-file.size) instead.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `atime` {#cha.atime}

Accessed time of the file in Unix timestamp.

|      |            |
| ---- | ---------- |
| Type | `integer?` |

#### `btime` {#cha.btime}

Birth time of the file in Unix timestamp.

|      |            |
| ---- | ---------- |
| Type | `integer?` |

#### `mtime` {#cha.mtime}

Modified time of the file in Unix timestamp.

|      |            |
| ---- | ---------- |
| Type | `integer?` |

#### `uid` {#cha.uid}

User id of the file.

|           |                        |
| --------- | ---------------------- |
| Type      | `integer?`             |
| Available | Unix-like systems only |

#### `gid` {#cha.gid}

Group id of the file.

|           |                        |
| --------- | ---------------------- |
| Type      | `integer?`             |
| Available | Unix-like systems only |

#### `nlink` {#cha.nlink}

Number of hard links to the file.

|           |                        |
| --------- | ---------------------- |
| Type      | `integer?`             |
| Available | Unix-like systems only |

#### `perm(self)` {#cha.perm}

Unix permission representation, such as `drwxr-xr-x`.

|           |                        |
| --------- | ---------------------- |
| Type      | `string?`              |
| Available | Unix-like systems only |

### File {#file}

A bare file without any context information. See also [`fs::File`](/docs/plugins/context#fs-file).

#### `url` {#file.url}

URL of the file.

|      |       |
| ---- | ----- |
| Type | `Url` |

#### `cha` {#file.cha}

[`Cha`](#cha) of the file.

|      |       |
| ---- | ----- |
| Type | `Cha` |

#### `link_to` {#file.link_to}

Path of the file points to, if it's a symlink.

|      |         |
| ---- | ------- |
| Type | `Path?` |

#### `name` {#file.name}

Name of the file.

|      |          |
| ---- | -------- |
| Type | `string` |

### Icon {#icon}

An icon.

#### `text` {#icon.text}

Text of the icon.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `style` {#icon.style}

[Style](/docs/plugins/layout#style) of the icon.

|      |         |
| ---- | ------- |
| Type | `Style` |

### Error {#error}

An error.

#### `code` {#error.code}

Raw error code.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `__tostring(self)` {#error.\_\_tostring}

Convert the error to string.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `string` |

#### `__concat(self, other)` {#error.\_\_concat}

Concatenate the error with `other`.

| In/Out  | Type     |
| ------- | -------- |
| `self`  | `Self`   |
| `other` | `string` |
| Return  | `Error`  |

### Window {#window}

#### `rows` {#window.rows}

Number of rows.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `cols` {#window.cols}

Number of columns.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `width` {#window.width}

Width in pixels.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `height` {#window.height}

Height in pixels.

|      |           |
| ---- | --------- |
| Type | `integer` |

---

## Layout

Line, Text, List, Bar, Border, and Gauge are renderable elements; others need to be placed within any of them.

### Rect {#rect}

A Rect is represented an area within the terminal by four attributes:

```lua
ui.Rect {
	x = 10, -- x position
	y = 10, -- y position
	w = 20, -- width
	h = 30, -- height
}

ui.Rect.default  -- Equal to `ui.Rect { x = 0, y = 0, w = 0, h = 0 }`
```

You can get a pre-computed `Rect` through [`ui.Layout()`](#layout).
Note that if you intend to create a `Rect` yourself, ensure these values are calculated accurately; otherwise, it may cause Yazi to crash!

#### `x` {#rect.x}

X position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `y` {#rect.y}

Y position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `w` {#rect.w}

Width of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `h` {#rect.h}

Height of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `left` {#rect.left}

Left position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `right` {#rect.right}

Right position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `top` {#rect.top}

Top position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `bottom` {#rect.bottom}

Bottom position of the rect.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `pad(self, padding)` {#rect.pad}

Apply a `padding` to the rect.

| In/Out    | Type          |
| --------- | ------------- |
| `self`    | `Self`        |
| `padding` | [`Pad`](#pad) |
| Return    | `self`        |

#### `__new(value)` {#rect.\_\_new}

Make a new rect.

| In/Out  | Type                                                     |
| ------- | -------------------------------------------------------- |
| `value` | `{ x: integer?, y: integer?, w: integer?, h: integer? }` |
| Return  | `Self`                                                   |

### Pad {#pad}

`Pad` represents a padding, and all of its parameters are integers:

```lua
ui.Pad(top, right, bottom, left)
```

#### `top` {#pad.top}

Top padding.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `right` {#pad.right}

Right padding.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `bottom` {#pad.bottom}

Bottom padding.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `left` {#pad.left}

Left padding.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `top(top)` {#pad.Top}

Create a padding with only top value, which is equal to `ui.Pad(top, 0, 0, 0)`.

| In/Out | Type      |
| ------ | --------- |
| `top`  | `integer` |
| Return | `Self`    |

#### `right(right)` {#pad.Right}

Create a padding with only right value, which is equal to `ui.Pad(0, right, 0, 0)`.

| In/Out  | Type      |
| ------- | --------- |
| `right` | `integer` |
| Return  | `Self`    |

#### `bottom(bottom)` {#pad.Bottom}

Create a padding with only bottom value, which is equal to `ui.Pad(0, 0, bottom, 0)`.

| In/Out   | Type      |
| -------- | --------- |
| `bottom` | `integer` |
| Return   | `Self`    |

#### `left(left)` {#pad.Left}

Create a padding with only left value, which is equal to `ui.Pad(0, 0, 0, left)`.

| In/Out | Type      |
| ------ | --------- |
| `left` | `integer` |
| Return | `Self`    |

#### `x(x)` {#pad.X}

Create a padding on both x-axis, which is equal to `ui.Pad(0, x, 0, x)`.

| In/Out | Type      |
| ------ | --------- |
| `x`    | `integer` |
| Return | `Self`    |

#### `y(y)` {#pad.Y}

Create a padding on both y-axis, which is equal to `ui.Pad(y, 0, y, 0)`.

| In/Out | Type      |
| ------ | --------- |
| `y`    | `integer` |
| Return | `Self`    |

#### `xy(x, y)` {#pad.XY}

Create a padding on both x and y-axis, which is equal to `ui.Pad(y, x, y, x)`.

| In/Out | Type      |
| ------ | --------- |
| `x`    | `integer` |
| `y`    | `integer` |
| Return | `Self`    |

#### `__new(top, right, bottom, left)` {#pad.\_\_new}

Make a new padding.

| In/Out   | Type      |
| -------- | --------- |
| `top`    | `integer` |
| `right`  | `integer` |
| `bottom` | `integer` |
| `left`   | `integer` |
| Return   | `Self`    |

### Pos {#pos}

`Pos` represents a position, which is composed of an origin and an offset relative to that origin:

```lua
ui.Pos { "center", x = 5, y = 3, w = 20, h = 10 }
```

Its only parameter is a table containing the following keys:

- `[1]`: [Origin](/docs/plugins/aliases#origin) of the position.
- `x`: X-offset relative to the origin, default is 0.
- `y`: Y-offset relative to the origin, default is 0.
- `w`: Width, default is 0.
- `h`: Height, default is 0.

#### `[1]` {#pos.[1]}

Origin of the position.

|      |                                          |
| ---- | ---------------------------------------- |
| Type | [`Origin`](/docs/plugins/aliases#origin) |

#### `x` {#pos.x}

X-offset relative to the origin.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `y` {#pos.y}

Y-offset relative to the origin.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `w` {#pos.w}

Width of the position.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `h` {#pos.h}

Height of the position.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `__new(value)` {#pos.\_\_new}

Make a new position.

| In/Out  | Type                                                                  |
| ------- | --------------------------------------------------------------------- |
| `value` | `{ [1]: Origin, x?: integer, y?: integer, w?: integer, h?: integer }` |
| Return  | `Self`                                                                |

### Style {#style}

Create a style:

```lua
ui.Style()
```

#### `fg(self, color)` {#style.fg}

Apply a foreground color.

| In/Out  | Type                                        |
| ------- | ------------------------------------------- |
| `self`  | `Self`                                      |
| `color` | [`AsColor`](/docs/plugins/aliases#as-color) |
| Return  | `Self`                                      |

#### `bg(self, color)` {#style.bg}

Apply a background color.

| In/Out  | Type                                        |
| ------- | ------------------------------------------- |
| `self`  | `Self`                                      |
| `color` | [`AsColor`](/docs/plugins/aliases#as-color) |
| Return  | `Self`                                      |

#### `bold(self)` {#style.bold}

Apply a bold style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `dim(self)` {#style.dim}

Apply a dim style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `italic(self)` {#style.italic}

Apply an italic style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `underline(self)` {#style.underline}

Apply an underline style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `blink(self)` {#style.blink}

Apply a blink style.

Note that this style may not be supported by all terminals.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `blink_rapid(self)` {#style.blink_rapid}

Apply a rapid blink style. Not all terminals support this.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `reverse(self)` {#style.reverse}

Apply a reverse style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `hidden(self)` {#style.hidden}

Apply a hidden style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `crossed(self)` {#style.crossed}

Apply a crossed style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `reset(self)` {#style.reset}

Apply a reset style.

| In/Out | Type   |
| ------ | ------ |
| `self` | `Self` |
| Return | `Self` |

#### `patch(self, another)` {#style.patch}

Patch the style with `other`.

| In/Out  | Type                            |
| ------- | ------------------------------- |
| `self`  | `Self`                          |
| `other` | `Self`                          |
| Return  | `Self`                          |
| Private | This method can't be inherited. |

#### `__new()` {#style.\_\_new}

Make a new style.

| In/Out | Type   |
| ------ | ------ |
| Return | `Self` |

### Span {#span}

`ui.Span` is the smallest unit of text, yet a component of `ui.Line`. Create a span:

```lua
ui.Span("foo")
```

For convenience, `ui.Span` can also accept another `ui.Span` as an argument:

```lua
ui.Span(ui.Span("bar"))
```

|         |                   |                                                  |
| ------- | ----------------- | ------------------------------------------------ |
| Inherit | [`Style`](#style) | To call [`Style`](#style) methods on it directly |

#### `visible(self)` {#span.visible}

Whether the span is visible, i.e. includes any printable characters.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `boolean` |

#### `style(self, style)` {#span.style}

Set the style of the span.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

Span inherits from `Style`, besides applying a whole `Style`, you can also call those methods of `Style` directly on it, which means:

```lua
local style = ui.Style():fg("white"):bg("black"):bold()
ui.Span("Hello world"):style(style)
```

can be also written as:

```lua
ui.Span("Hello world"):fg("white"):bg("black"):bold()
```

#### `__new(value)` {#span.\_\_new}

Make a new span.

| In/Out  | Type                                      |
| ------- | ----------------------------------------- |
| `value` | [`AsSpan`](/docs/plugins/aliases#as-span) |
| Return  | `Self`                                    |

### Line {#line}

`ui.Line` represents a line, consisting of multiple `ui.Span`s, and it accepts a table of them:

```lua
ui.Line { ui.Span("foo"), ui.Span("bar") }
```

For convenience, the following types are also supported:

```lua
-- string
ui.Line("foo")

-- ui.Span
ui.Line(ui.Span("bar"))

-- ui.Line itself
ui.Line(ui.Line("baz"))

-- Mixed table of string, ui.Span, ui.Line
ui.Line { "foo", ui.Span("bar"), ui.Line("baz") }
```

|         |                   |                                                  |
| ------- | ----------------- | ------------------------------------------------ |
| Inherit | [`Style`](#style) | To call [`Style`](#style) methods on it directly |

#### `area(self, rect)` {#line.area}

Set the area of the line.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `width(self)` {#line.width}

Calculate the width of the line.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `align(self, align)` {#line.align}

Set the alignment of the line.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `align` | [`Align`](#align) |
| Return  | `self`            |

#### `visible(self)` {#line.visible}

Whether the line is visible, i.e. includes any printable characters.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `boolean` |

#### `style(self, style)` {#line.style}

Set the style of the line.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

Like with [`Span`](#span), you can also call the [`Style`](#style) methods on it directly:

```lua
ui.Line("Hello world"):fg("white"):bg("black"):bold()
```

#### `__new(value)` {#line.\_\_new}

Make a new line.

| In/Out  | Type                                      |
| ------- | ----------------------------------------- |
| `value` | [`AsLine`](/docs/plugins/aliases#as-line) |
| Return  | `Self`                                    |

### Text {#text}

`ui.Text` is used to represent multi-line text, it takes a table of `ui.Line`:

```lua
ui.Text { ui.Line("foo"), ui.Line("bar") }
```

For convenience, the following types are also supported:

```lua
-- string
ui.Text("foo\nbar")

-- ui.Line
ui.Text(ui.Line("foo"))

-- ui.Span
ui.Text(ui.Span("bar"))

-- Mixed table of string, ui.Line, ui.Span
ui.Text { "foo", ui.Line("bar"), ui.Span("baz") }
```

You can also use `ui.Text.parse(code)` to parse an [ANSI escape sequence](https://en.wikipedia.org/wiki/ANSI_escape_code) string into a text.

|         |                   |                                                  |
| ------- | ----------------- | ------------------------------------------------ |
| Inherit | [`Style`](#style) | To call [`Style`](#style) methods on it directly |

#### `area(self, rect)` {#text.area}

Set the area of the text.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `align(self, align)` {#text.align}

Set the alignment of the text.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `align` | [`Align`](#align) |
| Return  | `self`            |

#### `wrap(self, wrap)` {#text.wrap}

Set the wrap of the text.

| In/Out | Type            |
| ------ | --------------- |
| `self` | `Self`          |
| `wrap` | [`Wrap`](#wrap) |
| Return | `self`          |

#### `max_width(self)` {#text.max_width}

Calculate the maximum width of the text across all lines.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `style(self, style)` {#text.style}

Set the style of the text.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

Like with [`Span`](#span), you can also call the [`Style`](#style) methods on it directly:

```lua
ui.Text("Hello world"):fg("white"):bg("black"):bold()
```

#### `__new(value)` {#text.\_\_new}

Make a new text.

| In/Out  | Type                                      |
| ------- | ----------------------------------------- |
| `value` | [`AsText`](/docs/plugins/aliases#as-text) |
| Return  | `Self`                                    |

### Layout {#layout}

Create a layout:

```lua
local areas = ui.Layout()
	:direction(ui.Layout.HORIZONTAL)
	:constraints({ ui.Constraint.Percentage(50), ui.Constraint.Percentage(50) })
	:split(area)

local left = areas[1] -- The first rect
local right = areas[2] -- The second rect
```

#### `direction(self, direction)` {#layout.direction}

Set the direction of the layout.

| In/Out      | Type        |
| ----------- | ----------- |
| `self`      | `Self`      |
| `direction` | `Direction` |
| Return      | `self`      |

The `direction` accepts the following constants:

- `ui.Layout.HORIZONTAL`
- `ui.Layout.VERTICAL`

#### `margin(self, margin)` {#layout.margin}

Set the margin of the layout.

| In/Out   | Type      | Note             |
| -------- | --------- | ---------------- |
| `self`   | `Self`    | -                |
| `margin` | `integer` | Positive integer |
| Return   | `self`    | -                |

#### `margin_h(self, margin)` {#layout.margin_h}

Set the horizontal margin of the layout.

| In/Out   | Type      | Note             |
| -------- | --------- | ---------------- |
| `self`   | `Self`    | -                |
| `margin` | `integer` | Positive integer |
| Return   | `self`    | -                |

#### `margin_v(self, margin)` {#layout.margin_v}

Set the vertical margin of the layout.

| In/Out   | Type      | Note             |
| -------- | --------- | ---------------- |
| `self`   | `Self`    | -                |
| `margin` | `integer` | Positive integer |
| Return   | `self`    | -                |

#### `constraints(self, constraints)` {#layout.constraints}

Set the constraints of the layout.

| In/Out        | Type                          |
| ------------- | ----------------------------- |
| `self`        | `Self`                        |
| `constraints` | [`Constraint[]`](#constraint) |
| Return        | `self`                        |

#### `split(self, rect)` {#layout.split}

Split the layout into multiple [Rect](#rect)s according to the constraints.

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| `rect` | [`Rect`](#rect)   |
| Return | [`Rect[]`](#rect) |

#### `__new()` {#layout.\_\_new}

Make a new layout.

| In/Out | Type   |
| ------ | ------ |
| Return | `Self` |

### Constraint {#constraint}

A constraint that defines the size of a layout element.

Constraints can be used to specify a fixed size, a percentage of the available space, a ratio of
the available space, a minimum or maximum size or a fill proportional value for a layout
element.

Relative constraints (percentage, ratio) are calculated relative to the entire space being
divided, rather than the space available after applying more fixed constraints (min, max,
length).

Constraints are prioritized in the following order:

1. `ui.Constraint.Min(min)`
2. `ui.Constraint.Max(max)`
3. `ui.Constraint.Length(len)`
4. `ui.Constraint.Percentage(p)`
5. `ui.Constraint.Ratio(num, den)`
6. `ui.Constraint.Fill(scale)`

#### `Min(min)` {#constraint.Min}

Applies a minimum size constraint to the element.

| In/Out | Type      |
| ------ | --------- |
| `min`  | `integer` |
| Return | `Self`    |

The element size is set to at least the specified amount.

```lua
-- { Percentage(100), Min(20) }
-- ┌────────────────────────────┐┌──────────────────┐
-- │            30 px           ││       20 px      │
-- └────────────────────────────┘└──────────────────┘

-- { Percentage(100), Min(10) }
-- ┌──────────────────────────────────────┐┌────────┐
-- │                 40 px                ││  10 px │
-- └──────────────────────────────────────┘└────────┘
```

#### `Max(max)` {#constraint.Max}

Applies a maximum size constraint to the element.

| In/Out | Type      |
| ------ | --------- |
| `max`  | `integer` |
| Return | `Self`    |

The element size is set to at most the specified amount.

```lua
-- { Percentage(0), Max(20) }
-- ┌────────────────────────────┐┌──────────────────┐
-- │            30 px           ││       20 px      │
-- └────────────────────────────┘└──────────────────┘

-- { Percentage(0), Max(10) }
-- ┌──────────────────────────────────────┐┌────────┐
-- │                 40 px                ││  10 px │
-- └──────────────────────────────────────┘└────────┘

```

#### `Length(len)` {#constraint.Length}

Applies a length constraint to the element.

| In/Out | Type      |
| ------ | --------- |
| `len`  | `integer` |
| Return | `Self`    |

The element size is set to the specified amount:

```lua
-- { Length(20), Length(20) }
-- ┌──────────────────┐┌──────────────────┐
-- │       20 px      ││       20 px      │
-- └──────────────────┘└──────────────────┘

-- { Length(20), Length(30) }
-- ┌──────────────────┐┌────────────────────────────┐
-- │       20 px      ││            30 px           │
-- └──────────────────┘└────────────────────────────┘
```

#### `Percentage(p)` {#constraint.Percentage}

Applies a percentage of the available space to the element.

| In/Out | Type      |
| ------ | --------- |
| `p`    | `integer` |
| Return | `Self`    |

Converts the given percentage to a floating-point value and multiplies that with area.
This value is rounded back to an integer as part of the layout split calculation.

```lua
-- { Percentage(75), Fill(1) }
-- ┌────────────────────────────────────┐┌──────────┐
-- │                38 px               ││   12 px  │
-- └────────────────────────────────────┘└──────────┘

-- { Percentage(50), Fill(1) }
-- ┌───────────────────────┐┌───────────────────────┐
-- │         25 px         ││         25 px         │
-- └───────────────────────┘└───────────────────────┘
```

#### `Ratio(num, den)` {#constraint.Ratio}

Applies a ratio of the available space to the element.

| In/Out | Type      |
| ------ | --------- |
| `num`  | `integer` |
| `den`  | `integer` |
| Return | `Self`    |

Converts the given ratio to a floating-point value and multiplies that with area.
This value is rounded back to an integer as part of the layout split calculation.

```lua
-- { Ratio(1, 2), Ratio(1, 2) }
-- ┌───────────────────────┐┌───────────────────────┐
-- │         25 px         ││         25 px         │
-- └───────────────────────┘└───────────────────────┘

-- { Ratio(1, 4), Ratio(1, 4), Ratio(1, 4), Ratio(1, 4) }
-- ┌───────────┐┌──────────┐┌───────────┐┌──────────┐
-- │   13 px   ││   12 px  ││   13 px   ││   12 px  │
-- └───────────┘└──────────┘└───────────┘└──────────┘
```

#### `Fill(scale)` {#constraint.Fill}

Applies the scaling factor proportional to all other `Fill` elements
to fill excess space.

| In/Out  | Type      |
| ------- | --------- |
| `scale` | `integer` |
| Return  | `Self`    |

The element will only expand or fill into excess available space, proportionally matching
other `Fill` elements while satisfying all other constraints.

```lua
-- { Fill(1), Fill(2), Fill(3) }
-- ┌──────┐┌───────────────┐┌───────────────────────┐
-- │ 8 px ││     17 px     ││         25 px         │
-- └──────┘└───────────────┘└───────────────────────┘

-- { Fill(1), Percentage(50), Fill(1) }
-- ┌───────────┐┌───────────────────────┐┌──────────┐
-- │   13 px   ││         25 px         ││   12 px  │
-- └───────────┘└───────────────────────┘└──────────┘
```

See https://docs.rs/ratatui/latest/ratatui/layout/enum.Constraint.html for more information.

### List {#list}

Create a `List` that takes a table of `ui.Text`:

```lua
ui.List { ui.Text("foo"), ui.Text("bar") }
```

For convenience, the following types are also supported:

```lua
-- Table of string
ui.List { "foo", "bar" }

-- Table of ui.Line
ui.List { ui.Line("foo"), ui.Line("bar") }

-- Table of ui.Span
ui.List { ui.Span("foo"), ui.Span("bar") }

-- Mixed table of string, ui.Line, ui.Span
ui.List { "foo", ui.Line("bar"), ui.Span("baz") }
```

#### `area(self, rect)` {#list.area}

Set the area of the list.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `style(self, style)` {#list.style}

Set the style of the list.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

#### `__new(value)` {#list.\_\_new}

Make a new list.

| In/Out  | Type                                                                     |
| ------- | ------------------------------------------------------------------------ |
| `value` | `string` \| `Span` \| `Line` \| `Text` \| `(string\|Span\|Line\|Text)[]` |
| Return  | `Self`                                                                   |

### Bar {#bar}

Create a bar:

```lua
ui.Bar(edge)
```

The first attribute denotes the direction of the bar and accepts an [`Edge`](#edge) constant.

#### `area(self, rect)` {#bar.area}

Set the area of the bar.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `symbol(self, symbol)` {#bar.symbol}

Set the symbol of the bar.

| In/Out   | Type     |
| -------- | -------- |
| `self`   | `Self`   |
| `symbol` | `string` |
| Return   | `self`   |

#### `style(self, style)` {#bar.style}

Set the style of the bar.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

#### `__new(edge)` {#bar.\_\_new}

Make a new bar.

| In/Out | Type            |
| ------ | --------------- |
| `edge` | [`Edge`](#edge) |
| Return | `Self`          |

### Border {#border}

Create a border:

```lua
ui.Border(edge)
```

The first attribute denotes the edge of the border and accepts an [`Edge`](#edge) constant.

#### `area(self, rect)` {#border.area}

Set the area of the border.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `type(self, type)` {#border.type}

Set the type of the border.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| `type` | `integer` |
| Return | `self`    |

The `type` accepts the following constants:

- `ui.Border.PLAIN`
- `ui.Border.ROUNDED`
- `ui.Border.DOUBLE`
- `ui.Border.THICK`
- `ui.Border.QUADRANT_INSIDE`
- `ui.Border.QUADRANT_OUTSIDE`

#### `style(self, style)` {#border.style}

Set the style of the border.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

#### `__new(edge)` {#border.\_\_new}

Make a new border.

| In/Out | Type            |
| ------ | --------------- |
| `edge` | [`Edge`](#edge) |
| Return | `Self`          |

### Gauge {#gauge}

Create a gauge:

```lua
ui.Gauge()
```

#### `area(self, rect)` {#gauge.area}

Set the area of the gauge.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `percent(self, percent)` {#gauge.percent}

Set the percentage of the gauge.

| In/Out    | Type      |
| --------- | --------- |
| `self`    | `Self`    |
| `percent` | `integer` |
| Return    | `self`    |

#### `ratio(self, ratio)` {#gauge.ratio}

Set the ratio of the gauge.

| In/Out  | Type     | Note            |
| ------- | -------- | --------------- |
| `self`  | `Self`   | -               |
| `ratio` | `number` | Between 0 and 1 |
| Return  | `self`   | -               |

#### `label(self, label)` {#gauge.label}

Set the label of the gauge.

| In/Out  | Type     |
| ------- | -------- |
| `self`  | `Self`   |
| `label` | `string` |
| Return  | `self`   |

#### `style(self, style)` {#gauge.style}

Set the style of everything except the gauge itself.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

#### `gauge_style(self, style)` {#gauge.gauge_style}

Set the style of the gauge itself.

| In/Out  | Type              |
| ------- | ----------------- |
| `self`  | `Self`            |
| `style` | [`Style`](#style) |
| Return  | `self`            |

#### `__new()` {#gauge.\_\_new}

Make a new gauge.

| In/Out | Type   |
| ------ | ------ |
| Return | `Self` |

### Clear {#clear}

Clear the content of a specific area, which is a [Rect](#rect). Place it followed by the component that you want to clear:

```lua
local components = {
	ui.Text("..."):area(rect),
	-- ...

	ui.Clear(rect),
}
```

#### `area(self, rect)` {#clear.area}

Set the area of the clear.

| In/Out | Type                      |
| ------ | ------------------------- |
| `self` | `Self`                    |
| `rect` | [`Rect?`](#rect)          |
| Return | `self` \| [`Rect`](#rect) |

If `rect` is not specified, it returns the current area.

#### `__new(rect)` {#clear.\_\_new}

Make a new clear.

| In/Out | Type            |
| ------ | --------------- |
| `rect` | [`Rect`](#rect) |
| Return | `Self`          |

### Align {#align}

Alignment of an element such as [`Text`](#text) or [`Line`](#line).

#### `LEFT` {#align.LEFT}

Align to the left.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `CENTER` {#align.CENTER}

Align to the center.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `RIGHT` {#align.RIGHT}

Align to the right.

|      |        |
| ---- | ------ |
| Type | `Self` |

### Wrap {#wrap}

Wrapping behavior of a [`Text`](#text).

#### `NO` {#wrap.NO}

Disables wrapping.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `YES` {#wrap.YES}

Enables wrapping.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `TRIM` {#wrap.TRIM}

Enables wrapping and trims the leading whitespace.

|      |        |
| ---- | ------ |
| Type | `Self` |

### Edge {#edge}

Which edges of elements such as [`Bar`](#bar) or [`Border`](#border) should be applied.

#### `NONE` {#edge.NONE}

No edge is applied.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `TOP` {#edge.TOP}

Applies the top edge.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `RIGHT` {#edge.RIGHT}

Applies the right edge.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `BOTTOM` {#edge.BOTTOM}

Applies the bottom edge.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `LEFT` {#edge.LEFT}

Applies the left edge.

|      |        |
| ---- | ------ |
| Type | `Self` |

#### `ALL` {#edge.ALL}

Applies all edges.

|      |        |
| ---- | ------ |
| Type | `Self` |

---

## Context

### cx {#cx}

You can access all states within [sync context](/docs/plugins/overview#sync-context) through `cx`.

#### `active` {#cx.active}

The active tab.

|      |                        |
| ---- | ---------------------- |
| Type | [`tab::Tab`](#tab-tab) |

#### `tabs` {#cx.tabs}

All of tabs.

|      |                          |
| ---- | ------------------------ |
| Type | [`mgr::Tabs`](#mgr-tabs) |

#### `tasks` {#cx.tasks}

All of tasks.

|      |                                |
| ---- | ------------------------------ |
| Type | [`tasks::Tasks`](#tasks-tasks) |

#### `yanked` {#cx.yanked}

Yanked files.

|      |                              |
| ---- | ---------------------------- |
| Type | [`mgr::Yanked`](#mgr-yanked) |

### tab::Mode {#tab-mode}

Visual mode status.

#### `is_select` {#tab-mode.is_select}

Whether in select mode.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_unset` {#tab-mode.is_unset}

Whether in unset mode.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `is_visual` {#tab-mode.is_visual}

Whether in select mode, or unset mode.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `__tostring(self)` {#tab-mode.\_\_tostring}

Converts the mode to string.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `string` |

### tab::Pref {#tab-pref}

Tab-specific user preferences.

#### `sort_by` {#tab-pref.sort_by}

File sorting method. See [`sort_by`](/docs/configuration/yazi#mgr.sort_by) for details.

|      |                                                                                                                  |
| ---- | ---------------------------------------------------------------------------------------------------------------- |
| Type | `"none"` \| `"mtime"` \| `"btime"` \| `"extension"` \| `"alphabetical"` \| `"natural"` \| `"size"` \| `"random"` |

#### `sort_sensitive` {#tab-pref.sort_sensitive}

Sort case-sensitively. See [`sort_sensitive`](/docs/configuration/yazi#mgr.sort_sensitive) for details.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `sort_reverse` {#tab-pref.sort_reverse}

Display files in reverse order. See [`sort_reverse`](/docs/configuration/yazi#mgr.sort_reverse) for details.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `sort_dir_first` {#tab-pref.sort_dir_first}

Display directories first. See [`sort_dir_first`](/docs/configuration/yazi#mgr.sort_dir_first) for details.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `sort_translit` {#tab-pref.sort_translit}

Transliterate filenames for sorting. See [`sort_translit`](/docs/configuration/yazi#mgr.sort_translit) for details.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `linemode` {#tab-pref.linemode}

Line mode. See [`linemode`](/docs/configuration/yazi#mgr.linemode) for details.

|      |                                                                                            |
| ---- | ------------------------------------------------------------------------------------------ |
| Type | `string` \| `"none"` \| `"size"` \| `"btime"` \| `"mtime"` \| `"permissions"` \| `"owner"` |

#### `show_hidden` {#tab-pref.show_hidden}

Show hidden files. See [`show_hidden`](/docs/configuration/yazi#mgr.show_hidden) for details.

|      |           |
| ---- | --------- |
| Type | `boolean` |

### tab::Selected {#tab-selected}

[Url](#url)s of the selected files.

#### `__len(self)` {#tab-selected.\_\_len}

Returns the number of selected [Url](#url)s.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `__pairs(self)` {#tab-selected.\_\_pairs}

Iterate over the selected [Url](#url)s.

| In/Out | Type                                 |
| ------ | ------------------------------------ |
| `self` | `Self`                               |
| Return | `fun(t: self, k: any): integer, Url` |

### tab::Preview {#tab-preview}

State of the preview pane.

#### `skip` {#tab-preview.skip}

Number of units to skip. The units largely depend on your previewer, such as lines for code and percentages for videos.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `folder` {#tab-preview.folder}

The folder being previewed, or `nil` if this preview is not for a folder.

|      |                               |
| ---- | ----------------------------- |
| Type | [`tab::Folder?`](#tab-folder) |

### tab::Folder {#tab-folder}

A folder.

#### `cwd` {#tab-folder.cwd}

Current working directory.

|      |               |
| ---- | ------------- |
| Type | [`Url`](#url) |

#### `offset` {#tab-folder.offset}

Offset of the folder.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `cursor` {#tab-folder.cursor}

Cursor position.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `window` {#tab-folder.window}

Files within the visible area.

|      |                          |
| ---- | ------------------------ |
| Type | [`fs::Files`](#fs-files) |

#### `files` {#tab-folder.files}

All of the files in the folder.

|      |                          |
| ---- | ------------------------ |
| Type | [`fs::Files`](#fs-files) |

#### `hovered` {#tab-folder.hovered}

Hovered file, or `nil` if no file is hovered.

|      |                         |
| ---- | ----------------------- |
| Type | [`fs::File?`](#fs-file) |

### fs::Files {#fs-files}

Files in a [`tab::Folder`](#tab-folder).

#### `__len(self)` {#fs-files.\_\_len}

Returns the number of files in this folder.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `__index(self, idx)` {#fs-files.\_\_index}

Access each file by index.

| In/Out | Type                    |
| ------ | ----------------------- |
| `self` | `Self`                  |
| `idx`  | `integer`               |
| Return | [`fs::File?`](#fs-file) |

### fs::File {#fs-file}

A file lives in the current context, which inherits from [`File`](/docs/plugins/types#file) but has many more context-specific properties and methods.

|         |                                    |                                  |
| ------- | ---------------------------------- | -------------------------------- |
| Inherit | [`File`](/docs/plugins/types#file) | To access basic file attributes. |

#### `is_hovered` {#fs-file.is_hovered}

Whether the file is hovered.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `size(self)` {#fs-file.size}

Size of the file in bytes, or `nil` if it's a directory yet not been evaluated.

| In/Out | Type       |
| ------ | ---------- |
| `self` | `Self`     |
| Return | `integer?` |

#### `mime(self)` {#fs-file.mime}

Mimetype of the file, or `nil` if it's a directory or hasn't been lazily calculated.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `string?` |

#### `prefix(self)` {#fs-file.prefix}

Prefix of the file relative to `CWD`, which used in the flat view during search.

For instance, if `CWD` is `/foo`, and the file is `/foo/bar/baz`, then the prefix is `bar/`.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `string?` |

#### `icon(self)` {#fs-file.icon}

Icon of the file, or `nil` if no [`[icon]`](/docs/configuration/theme#icon) rules match.

| In/Out | Type    |
| ------ | ------- |
| `self` | `Self`  |
| Return | `Icon?` |

#### `style(self)` {#fs-file.style}

Style of the file, or `nil` if no [`[filetype]`](/docs/configuration/theme#filetype) rules match.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `Style?` |

#### `is_yanked(self)` {#fs-file.is_yanked}

Whether the file is yanked.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `boolean` |

#### `is_selected(self)` {#fs-file.is_selected}

Whether the file is selected.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `boolean` |

#### `found(self)` {#fs-file.found}

File find status:

- `nil` if if the user not in [`find`](/docs/configuration/keymap#mgr.find) mode.
- `nil` if current file is not related to the keyword entered by the user.
- `integer, integer` if current file is one of the files found, where first is its index among the results and second is the total count of files found.

| In/Out | Type                 |
| ------ | -------------------- |
| `self` | `Self`               |
| Return | `integer?, integer?` |

### mgr::Tabs {#mgr-tabs}

All of tabs.

#### `idx` {#mgr-tabs.idx}

Index of the active tab.

|      |           |
| ---- | --------- |
| Type | `integer` |

#### `__len(self)` {#mgr-tabs.\_\_len}

Returns the number of tabs.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `__index(self, idx)` {#mgr-tabs.\_\_index}

Access each tab by index.

| In/Out | Type                    |
| ------ | ----------------------- |
| `self` | `Self`                  |
| `idx`  | `integer`               |
| Return | [`tab::Tab?`](#tab-tab) |

### tab::Tab {#tab-tab}

A tab.

#### `name` {#tab-tab.name}

Name of the tab.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `mode` {#tab-tab.mode}

Mode of the tab.

|      |                          |
| ---- | ------------------------ |
| Type | [`tab::Mode`](#tab-mode) |

#### `pref` {#tab-tab.pref}

Preference of the tab.

|      |                          |
| ---- | ------------------------ |
| Type | [`tab::Pref`](#tab-pref) |

#### `current` {#tab-tab.current}

Current working folder.

|      |                              |
| ---- | ---------------------------- |
| Type | [`tab::Folder`](#tab-folder) |

#### `parent` {#tab-tab.parent}

Parent folder of the `CWD`, or `nil` if no parent folder exists.

|      |                               |
| ---- | ----------------------------- |
| Type | [`tab::Folder?`](#tab-folder) |

#### `selected` {#tab-tab.selected}

Selected files within the tab.

|      |                                  |
| ---- | -------------------------------- |
| Type | [`tab::Selected`](#tab-selected) |

#### `preview` {#tab-tab.preview}

Preview of the tab.

|      |                                |
| ---- | ------------------------------ |
| Type | [`tab::Preview`](#tab-preview) |

### tasks::Tasks {#tasks-tasks}

#### `progress` {#tasks-tasks.progress}

Progress of all tasks:

```lua
{
	-- Number of tasks
	total = 0,
	succ  = 0,
	fail  = 0,

	-- Workload of tasks
	found     = 0,
	processed = 0,
}
```

|      |                                                                                        |
| ---- | -------------------------------------------------------------------------------------- |
| Type | `{ total: integer, succ: integer, fail: integer, found: integer, processed: integer }` |

### mgr::Yanked {#mgr-yanked}

Yanked files.

#### `is_cut` {#mgr-yanked.is_cut}

Whether in cut mode.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `__len(self)` {#mgr-yanked.\_\_len}

Returns the number of yanked files.

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| Return | `integer` |

#### `__pairs(self)` {#mgr-yanked.\_\_pairs}

Iterate over the url of yanked files.

| In/Out | Type                                 |
| ------ | ------------------------------------ |
| `self` | `Self`                               |
| Return | `fun(t: self, k: any): integer, Url` |

---

## Runtime

### rt {#rt}

You can access Yazi's runtime through `rt` to obtain startup parameters, terminal properties, [user preferences](/docs/configuration/yazi), etc.

#### `args` {#rt.args}

Command-line arguments passed by the user when launching Yazi.

|      |                        |
| ---- | ---------------------- |
| Type | [`rt::Args`](#rt-args) |

#### `term` {#rt.term}

User's terminal emulator properties.

|      |                        |
| ---- | ---------------------- |
| Type | [`rt::Term`](#rt-term) |

#### `mgr` {#rt.mgr}

User preferences under [\[mgr\]](/docs/configuration/yazi#mgr).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `plugin` {#rt.plugin}

User preferences under [\[plugin\]](/docs/configuration/yazi#plugin).

|      |                            |
| ---- | -------------------------- |
| Type | [`rt::Plugin`](#rt-plugin) |

#### `preview` {#rt.preview}

User preferences under [\[preview\]](/docs/configuration/yazi#preview).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `tasks` {#rt.tasks}

User preferences under [\[tasks\]](/docs/configuration/yazi#tasks).

|      |         |
| ---- | ------- |
| Type | `table` |

### th {#th}

You can access the user's theme and flavor configuration through `th`.

#### `mgr` {#th.mgr}

See [\[mgr\]](/docs/configuration/theme#mgr).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `tabs` {#th.tabs}

See [\[tabs\]](/docs/configuration/theme#tabs).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `mode` {#th.mode}

See [\[mode\]](/docs/configuration/theme#mode).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `status` {#th.status}

See [\[status\]](/docs/configuration/theme#status).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `which` {#th.which}

See [\[which\]](/docs/configuration/theme#which).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `confirm` {#th.confirm}

See [\[confirm\]](/docs/configuration/theme#confirm).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `spot` {#th.spot}

See [\[spot\]](/docs/configuration/theme#spot).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `notify` {#th.notify}

See [\[notify\]](/docs/configuration/theme#notify).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `pick` {#th.pick}

See [\[pick\]](/docs/configuration/theme#pick).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `input` {#th.input}

See [\[input\]](/docs/configuration/theme#input).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `cmp` {#th.cmp}

See [\[cmp\]](/docs/configuration/theme#cmp).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `tasks` {#th.tasks}

See [\[tasks\]](/docs/configuration/theme#tasks).

|      |         |
| ---- | ------- |
| Type | `table` |

#### `help` {#th.help}

See [\[help\]](/docs/configuration/theme#help).

|      |         |
| ---- | ------- |
| Type | `table` |

### rt::Args {#rt-args}

#### `entries` {#rt-args.entries}

TODO

#### `cwd_file` {#rt-args.cwd_file}

TODO

#### `chooser_file` {#rt-args.chooser_file}

TODO

### rt::Term {#rt-term}

User's terminal emulator properties.

#### `light` {#rt-term.light}

Whether the terminal is in light mode.

|      |           |
| ---- | --------- |
| Type | `boolean` |

### rt::Plugin {#rt-plugin}

TODO

---

## Utils

### ya {#ya}

#### `file_cache(opts)` {#ya.file_cache}

Calculate the cached [Url](/docs/plugins/types#url) corresponding to the given file.

```lua
ya.file_cache {
	-- File to be cached.
	file = file,
	-- Number of units to skip. Its units largely depend on your previewer,
	-- such as lines for code, and percentages for videos.
	skip = 1,
}
```

If the file is not allowed to be cached, such as it's ignored in the user config, or the file itself is a cache, returns `nil`.

| In/Out | Type                            |
| ------ | ------------------------------- |
| `opts` | `{ file: File, skip: integer }` |
| Return | `Url?`                          |

#### `emit(action, args)` {#ya.emit}

Send an action to the [`[mgr]`](/docs/configuration/keymap#mgr) without waiting for the executor to execute:

```lua
ya.emit("action", { "hello", 123, foo = true, bar_baz = "world" })

-- Equivalent to:
-- action "hello" "123" --foo --bar-baz="world"
```

| In/Out   | Type                              | Note                                                                                    |
| -------- | --------------------------------- | --------------------------------------------------------------------------------------- |
| `action` | `string`                          | -                                                                                       |
| `args`   | `{ [integer\|string]: Sendable }` | Table values are [Sendable][sendable] that follow [Ownership transfer rules][ownership] |
| Return   | `unknown`                         | -                                                                                       |

#### `image_show(url, rect)` {#ya.image_show}

Display the image of `url` within the `rect`, and the image will downscale to fit the area automatically:

| In/Out    | Type               |
| --------- | ------------------ |
| `url`     | `Url`              |
| `rect`    | `Rect`             |
| Return    | `unknown`          |
| Available | Async context only |

#### `image_precache(src, dist)` {#ya.image_precache}

Pre-cache the image of `src` as `dist` based on user-configured [`max_width` and `max_height`](/docs/configuration/yazi#preview).

| In/Out    | Type               |
| --------- | ------------------ |
| `src`     | `Url`              |
| `dist`    | `Url`              |
| Return    | `unknown`          |
| Available | Async context only |

#### `which(opts)` {#ya.which}

Prompt users with a set of available keys:

```lua
local cand = ya.which {
	-- Key candidates, contains the following fields:
	--   `on`: Key to be prompted, which is a string or a table of strings if multiple.
	--   `desc`: Description of the key.
	cands = {
		{ on = "a" },
		{ on = "b", desc = "optional description" },
		{ on = "<C-c>", desc = "key combination" },
		{ on = { "d", "e" }, desc = "multiple keys" },
	},
	-- Whether to show the UI of key indicator
	silent = false,
}
```

When the user clicks a valid candidate, `ya.which` returns the 1-based index of that `cand`;
otherwise, it returns `nil`, indicating that the user has canceled the key operation.

| In/Out    | Type                                                                     |
| --------- | ------------------------------------------------------------------------ |
| `opts`    | `{ cands: { on: string\|string[], desc: string? }[], silent: boolean? }` |
| Return    | `number?`                                                                |
| Available | Async context only                                                       |

#### `input(opts)` {#ya.input}

Request user input:

```lua
local value, event = ya.input {
	-- Position
	pos = { "top-center", y = 3, w = 40 },
	-- Title
	title = "Archive name:",
	-- Default value
	value = "",
	-- Whether to obscure the input.
	obscure = false,
	-- Whether to report user input in real time.
	realtime = false,
	-- Number of seconds to wait for the user to stop typing, available if `realtime = true`.
	debounce = 0.3,
}
```

Returns `(value, event)`:

- `value`: The user input value carried by this event, which is a string if the `event` is non-zero; otherwise, `nil`.
- `event`: The event type, which is an integer:
  - 0: Unknown error.
  - 1: The user has confirmed the input.
  - 2: The user has canceled the input.
  - 3: The user has changed the input (only if `realtime` is true).

When `realtime = true` specified, `ya.input()` returns a receiver, which has a `recv()` method that can be called multiple times to receive events:

```lua
local input = ya.input {
	pos = { "center", w = 50 },
	title = "Input in realtime:",
	realtime = true,
}

while true do
	local value, event = input:recv()
	if not value then
		break
	end

	ya.dbg(value)
end
```

| In/Out    | Type                                                                                                      |
| --------- | --------------------------------------------------------------------------------------------------------- |
| `opts`    | `{ pos: AsPos, title: string, value: string?, obscure: boolean?, realtime: boolean?, debounce: number? }` |
| Return    | `(string?, integer)` \| `Recv`                                                                            |
| Available | Async context only                                                                                        |

#### `notify(opts)` {#ya.notify}

Send a foreground notification to the user:

```lua
ya.notify {
	-- Title.
	title = "Hello, World!",
	-- Content.
	content = "This is a notification from Lua!",
	-- Timeout.
	timeout = 6.5,
	-- Level, available values: "info", "warn", and "error", default is "info".
	level = "info",
}
```

| In/Out | Type                                                                                       |
| ------ | ------------------------------------------------------------------------------------------ |
| `opts` | `{ title: string, content: string, timeout: number, level: "info"\|"warn"\|"error"\|nil }` |
| Return | `unknown`                                                                                  |

#### `confirm(opts)` {#ya.confirm}

Request user confirmation:

```lua
local answer = ya.confirm {
	-- Position
  pos = { "center", w = 40, h = 10 },
	-- Title
  title = "Test",
	-- Body
  body = "Hello, World!",
}
```

| In/Out    | Type                                          |
| --------- | --------------------------------------------- |
| `opts`    | `{ pos: AsPos, title: AsLine, body: AsText }` |
| Return    | `boolean`                                     |
| Available | Async context only                            |

#### `dbg(msg, ...)` {#ya.dbg}

Append messages to [the log file](/docs/plugins/overview#logging) at the debug level:

```lua
ya.dbg("Hello", "World!")                       -- Multiple arguments are supported
ya.dbg({ foo = "bar", baz = 123, qux = true })  -- Any type of data is supported
```

| In/Out | Type      |
| ------ | --------- |
| `msg`  | `any`     |
| `...`  | `any`     |
| Return | `unknown` |

#### `err(msg, ...)` {#ya.err}

Append messages to [the log file](/docs/plugins/overview#logging) at the error level:

```lua
ya.err("Hello", "World!")                       -- Multiple arguments are supported
ya.err({ foo = "bar", baz = 123, qux = true })  -- Any type of data is supported
```

| In/Out | Type      |
| ------ | --------- |
| `msg`  | `any`     |
| `...`  | `any`     |
| Return | `unknown` |

#### `preview_code(opts)` {#ya.preview_code}

Preview the file as code into the specified area:

```lua
ya.preview_code {
	-- Available preview area
  area = area,
	-- File to be previewed.
  file = file,
	-- Mimetype of the file.
  mime = "text/plain",
	-- Number of units to skip. The units depend on your previewer,
	-- such as lines for code and percentages for videos.
  skip = 1,
}
```

Returns `(err, upper_bound)`:

- `err`: Error string if the preview fails; otherwise, `nil`.
- `upper_bound`: If the preview fails and it's because exceeds the maximum upper bound, return this bound; otherwise, `nil`.

| In/Out    | Type                                                      |
| --------- | --------------------------------------------------------- |
| `opts`    | `{ area: Rect, file: File, mime: string, skip: integer }` |
| Return    | `Error?, integer?`                                        |
| Available | Async context only                                        |

#### `preview_widget(opts, widget)` {#ya.preview_widget}

```lua
local opts = {
	-- Available preview area.
	area = area,
	-- File to be previewed.
	file = file,
	-- Mimetype of the file.
	mime = "text/plain",
	-- Number of units to skip. The units depend on your previewer,
	-- such as lines for code and percentages for videos.
	skip = 1,
}

-- Preview a widget in the specified area.
ya.preview_widget(opts, ui.Line("Hello world"):area(area))

-- Preview multiple widgets in the specified area.
ya.preview_widget(opts, {
	ui.Line("Hello"):area(area1),
	ui.Line("world"):area(area2),
})
```

| In/Out    | Type                                                      |
| --------- | --------------------------------------------------------- |
| `opts`    | `{ area: Rect, file: File, mime: string, skip: integer }` |
| `widget`  | `Renderable` \| `Renderable[]`                            |
| Return    | `unknown`                                                 |
| Available | Async context only                                        |

#### `sync(fn)` {#ya.sync}

Make a function synchronous.

See [Async context](/docs/plugins/overview#async-context).

| In/Out | Type                 |
| ------ | -------------------- |
| `fn`   | `fun(...: any): any` |
| Return | `fun(...: any): any` |

#### `async(fn)` {#ya.async}

:::warning
This API is highly experimental at the moment, and its behavior may change in the future.
:::

Run a function asynchronously on the main thread.

`fn` should contain only async I/O operations, i.g., calls to other async APIs, and should not include any sync I/O, or blocking tasks, such as Lua's `io.open()`, `os.system()`.

`fn` runs in an asynchronous context but can access any [Sendable values](/docs/plugins/overview#sendable) from the outer synchronous context, for example:

```lua
--- @sync entry
local function entry()
	local cwd = cx.active.current.cwd
	ya.async(function ()
		ya.dbg(cwd)    -- `cwd` is a Url and is sendable
	end)
end

return { entry }
```

See [Async context](/docs/plugins/overview#async-context).

| In/Out | Type                 |
| ------ | -------------------- |
| `fn`   | `fun(...: any): any` |
| Return | `any`                |

#### `target_os()` {#ya.target_os}

Returns a string describing the specific operating system in use.

| In/Out | Type                                                                                                                                                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Return | `string` \| `"linux"` \| `"macos"` \| `"ios"` \| `"freebsd"` \| `"dragonfly"` \| `"netbsd"` \| `"openbsd"` \| `"solaris"` \| `"android"` \| `"windows"` |

#### `target_family()` {#ya.target_family}

Returns the family of the operating system.

| In/Out | Type                                            |
| ------ | ----------------------------------------------- |
| Return | `string` \| `"unix"` \| `"windows"` \| `"wasm"` |

#### `hash(str)` {#ya.hash}

Returns the hash of `str`:

```lua
ya.hash("Hello, World!")
```

It is designed to work with algorithm-independent tasks, such as generating file cache names.

The current implementation uses MD5, but it will be replaced with a faster hash algorithm, like [xxHash](https://github.com/Cyan4973/xxHash), in the future. So, don't rely on this implementation detail.

| In/Out    | Type               |
| --------- | ------------------ |
| `str`     | `string`           |
| Return    | `string`           |
| Available | Async context only |

#### `quote(str)` {#ya.quote}

Quote characters in `str` that may have special meaning in a shell:

```lua
local handle = io.popen("ls " .. ya.quote(filename))
```

| In/Out | Type     |
| ------ | -------- |
| `str`  | `string` |
| Return | `string` |

#### `clipboard(text)` {#ya.clipboard}

Get or set the content of the system clipboard:

```lua
-- Get contents from the clipboard if no argument is provided
local content = ya.clipboard()

-- Set contents to the clipboard
ya.clipboard("new content")
```

| In/Out    | Type               |
| --------- | ------------------ |
| `text`    | `string?`          |
| Return    | `string?`          |
| Available | Async context only |

#### `time()` {#ya.time}

Returns the current timestamp, which is a float, the integer part represents the seconds, and the decimal part represents the milliseconds.

| In/Out | Type     |
| ------ | -------- |
| Return | `number` |

#### `sleep(secs)` {#ya.sleep}

Waits until `secs` has elapsed:

```lua
ya.sleep(0.5)  -- Sleep for 500 milliseconds
```

| In/Out    | Type               |
| --------- | ------------------ |
| `secs`    | `number`           |
| Return    | `unknown`          |
| Available | Async context only |

#### `uid()` {#ya.uid}

Returns the id of the current user.

| In/Out    | Type                   |
| --------- | ---------------------- |
| Return    | `integer`              |
| Available | Unix-like systems only |

#### `gid()` {#ya.gid}

Returns the group id of the current user.

| In/Out    | Type                   |
| --------- | ---------------------- |
| Return    | `integer`              |
| Available | Unix-like systems only |

#### `user_name(uid)` {#ya.user_name}

Get the username by `uid`:

```lua
-- Get the current user's name if no argument is provided
ya.user_name()

-- Get the name of user with id 1000
ya.user_name(1000)
```

| In/Out    | Type                   |
| --------- | ---------------------- |
| `uid`     | `integer?`             |
| Return    | `string?`              |
| Available | Unix-like systems only |

#### `group_name(gid)` {#ya.group_name}

Get the group name by `gid`:

```lua
-- Get the current user's group name if no argument is provided
ya.group_name()

-- Get the name of group with id 1000
ya.group_name(1000)
```

| In/Out    | Type                   |
| --------- | ---------------------- |
| `gid`     | `integer?`             |
| Return    | `string?`              |
| Available | Unix-like systems only |

#### `host_name()` {#ya.host_name}

Returns the hostname of the current machine.

| In/Out    | Type                   |
| --------- | ---------------------- |
| Return    | `string?`              |
| Available | Unix-like systems only |

### fs {#fs}

The following functions can only be used within an async context.

#### `cwd()` {#fs.cwd}

Get the current working directory (CWD) of the process.

This API was added to compensate for the lack of a [`getcwd`][getcwd] in Lua; it is used to retrieve the directory of the last [`chdir`][chdir] call:

```lua
local url, err = fs.cwd()
```

You probably will never need it, and more likely, you'll need [`cx.active.current.cwd`][folder-cwd], which is the current directory where the user is working.

Specifically, when the user changes the directory, `cx.active.current.cwd` gets updated immediately, while synchronizing this update with the file system via `chdir` involves I/O operations, such as checking if the directory is valid.

So, there may be some delay, which is particularly noticeable on slow devices. For example, when an HDD wakes up from sleep, it typically takes 3~4 seconds.

It is useful if you just need a valid directory as the CWD of a process to start some work that doesn't depend on the CWD.

| In/Out    | Type               |
| --------- | ------------------ |
| Return    | `Url?, Error?`     |
| Available | Async context only |

[getcwd]: https://man7.org/linux/man-pages/man3/getcwd.3.html
[chdir]: https://man7.org/linux/man-pages/man2/chdir.2.html
[folder-cwd]: /docs/plugins/context#tab-folder.cwd

#### `cha(url, follow)` {#fs.cha}

Get the [Cha][cha] of the specified `url`:

```lua
-- Not following symbolic links
local cha, err = fs.cha(url)

-- Follow symbolic links
local cha, err = fs.cha(url, true)
```

Returns `(cha, err)`:

- `cha`: The [Cha][cha] of the specified `url` if the operation succeeds.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type               |
| --------- | ------------------ |
| `url`     | `Url`              |
| `follow`  | `boolean?`         |
| Return    | `Cha?, Error?`     |
| Available | Async context only |

#### `write(url, data)` {#fs.write}

Write `data` to the specified `url`:

```lua
local ok, err = fs.write(url, "hello world")
```

| In/Out    | Type               |
| --------- | ------------------ |
| `url`     | `Url`              |
| `data`    | `string`           |
| Return    | `boolean, Error?`  |
| Available | Async context only |

#### `access()` {#fs.access}

Create an [`Access`](#access) with which to access the filesystem.

```lua
local access = fs.access()
```

| In/Out    | Type               |
| --------- | ------------------ |
| Return    | `Access`           |
| Available | Async context only |

#### `create(type, url)` {#fs.create}

Create directories at the given filesystem `url`:

```lua
local ok, err = fs.create("dir_all", Url("/tmp/test/nest/nested"))
```

Where `type` can be one of the following:

- `"dir"`: Creates a new, empty directory.
- `"dir_all"`: Recursively create a directory and all of its parents if they are missing.

Returns `(ok, err)`:

- `ok`: Whether the operation succeeds, which is a `boolean`.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type                               |
| --------- | ---------------------------------- |
| `type`    | `string` \| `"dir"` \| `"dir_all"` |
| `url`     | `Url`                              |
| Return    | `boolean, Error?`                  |
| Available | Async context only                 |

#### `remove(type, url)` {#fs.remove}

Remove file(s) at the `url` of the file system:

```lua
local ok, err = fs.remove("file", Url("/tmp/test.txt"))
```

Where `type` can be one of the following:

- `"file"`: Removes a file from the file system.
- `"dir"`: Removes an existing, empty directory.
- `"dir_all"`: Removes a directory at this url, after removing all its contents. Use carefully!
- `"dir_clean"`: Remove all empty directories under it, and if the directory itself is empty afterward, remove it as well.

Returns `(ok, err)`:

- `ok`: Whether the operation succeeds, which is a `boolean`.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type                                                            |
| --------- | --------------------------------------------------------------- |
| `type`    | `string` \| `"file"` \| `"dir"` \| `"dir_all"` \| `"dir_clean"` |
| `url`     | `Url`                                                           |
| Return    | `boolean, Error?`                                               |
| Available | Async context only                                              |

#### `read_dir(url, options)` {#fs.read_dir}

Reads the directory contents of `url`:

```lua
local files, err = fs.read_dir(url, {
	-- Glob pattern to filter files out if provided.
	glob = nil,
	-- Maximum number of files to read, defaults to unlimited.
	limit = 10,
	-- Whether to resolve symbolic links, defaults to `false`.
	resolve = false,
})
```

| In/Out    | Type                                                    |
| --------- | ------------------------------------------------------- |
| `url`     | `Url`                                                   |
| `options` | `{ glob: string?, limit: integer?, resolve: boolean? }` |
| Return    | `File[]?, Error?`                                       |
| Available | Async context only                                      |

#### `copy(from, to)` {#fs.copy}

Copy a file from the source `from`, to the destination `to`:

```lua
local len, err = fs.copy(Url("/tmp/src.txt"), Url("/tmp/dest.txt"))
```

Returns `(len, err)`:

- `len`: Length of the copied content, which is an `integer`, or `nil` if the operation fails.
- `err`: [`Error`][error] of the failure.

Note that:

- This function will overwrite the destination file.
- This function follows symbolic links for both `from` and `to`.
- If `from` and `to` are the same file, the file will likely be truncated by this operation.

| In/Out    | Type               |
| --------- | ------------------ |
| `from`    | `Url`              |
| `to`      | `Url`              |
| Return    | `integer?, Error?` |
| Available | Async context only |

#### `rename(from, to)` {#fs.rename}

Rename a file from the source `from`, to the destination `to`.

```lua
local ok, err = fs.rename(Url("/tmp/old.txt"), Url("/tmp/new.txt"))
```

Returns `(ok, err)`:

- `ok`: Whether the operation succeeds, which is a `boolean`.
- `err`: [`Error`][error] of the failure.

Note that:

- This function will overwrite the destination file.
- This function does not work if `from` and `to` are on different file systems.

To move files across file systems, use a combination of [`fs.copy()`](#fs.copy) and [`fs.remove()`](#fs.remove):

```lua
local from = Url("/mnt/dev1/a")
local to = Url("/mnt/dev2/b")

local ok, err = fs.rename(from, to)
if not ok and err.kind == "CrossesDevices" then
	local len, err = fs.copy(from, to)
	if len and not err then
		fs.remove("file", from)
	end
end
```

| In/Out    | Type               |
| --------- | ------------------ |
| `from`    | `Url`              |
| `to`      | `Url`              |
| Return    | `boolean, Error?`  |
| Available | Async context only |

#### `unique(type, url)` {#fs.unique}

Create a file or a directory with the unique name from the given `url` to ensure it's unique in the file system:

```lua
local url, err = fs.unique("file", Url("/tmp/test.txt"))
```

Where `type` can be one of the following:

- `"file"`: Creates a file with the unique name.
- `"dir"`: Creates a directory with the unique name.

If the file already exists, it will append `_n` to the filename, where `n` is a number, and keep incrementing until the first available name is found.

Returns `(url, err)`:

- `url`: The [`Url`][url] with the unique filename.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type                |
| --------- | ------------------- |
| `type`    | `"file"` \| `"dir"` |
| `url`     | `Url`               |
| Return    | `Url?, Error?`      |
| Available | Async context only  |

### ui {#ui}

APIs related to the user interface.

#### `hide()` {#ui.hide}

Hide Yazi to the secondary screen by returning to the terminal, completely controlled by the requested plugin.

```lua
local permit = ui.hide()
```

This method returns a `permit` for this resource. When it's necessary to restore the TUI display, call its `drop()` method:

```lua
permit:drop()
```

Note that since there's always only one available terminal control resource, `ui.hide()` cannot be called again before the previous `permit` is dropped, otherwise an error will be thrown, effectively avoiding deadlocks.

| In/Out    | Type               |
| --------- | ------------------ |
| Return    | `Permit`           |
| Available | Async context only |

#### `render()` {#ui.render}

Re-render the UI:

```lua
local update_state = ya.sync(function(self, new_state)
	self.state = new_state
	ui.render()
end)
```

| In/Out    | Type              |
| --------- | ----------------- |
| Return    | `unknown`         |
| Available | Sync context only |

#### `truncate(text, opts)` {#ui.truncate}

Truncate the `text` to the specified width and return the truncated result:

```lua
ui.truncate("Hello, World!", {
	-- Maximum width of the text.
	max = 5,
	-- Whether to truncate the text from right-to-left.
	rtl = false
})
```

| In/Out | Type                              |
| ------ | --------------------------------- |
| `text` | `string`                          |
| `opts` | `{ max: integer, rtl: boolean? }` |
| Return | `string`                          |

### ps {#ps}

Yazi's DDS (Data Distribution Service) uses a Lua-based publish-subscribe model as its carrier. That is, you can achieve cross-instance communication and state persistence through the `ps` API. See [DDS](/docs/dds) for details.

The following functions can only be used within a sync context.

#### `pub(kind, value)` {#ps.pub}

Publish a message to the current instance, and all plugins subscribed through `sub()` for this `kind` will receive it, achieving internal communication within the instance:

```lua
ps.pub("greeting", "Hello, World!")
```

Since the `kind` is used globally, to add the plugin name as the prefix is a best practice.
For example, the combination of the plugin `my-plugin` and the kind `event1` would be `my-plugin-event1`.

| In/Out  | Type       | Note                                                                            |
| ------- | ---------- | ------------------------------------------------------------------------------- |
| `kind`  | `string`   | Alphanumeric with dashes, cannot be [built-in kinds](/docs/dds#kinds)           |
| `value` | `Sendable` | A [Sendable value][sendable] that follows [Ownership transfer rules][ownership] |
| Return  | `unknown`  | -                                                                               |

#### `pub_to(receiver, kind, value)` {#ps.pub_to}

Publish a message to a specific instance with `receiver` as the ID:

```lua
ps.pub_to(1711957283332834, "greeting", "Hello, World!")
```

Where:

- Local - `receiver` is the current instance, and is subscribed to this `kind` via `sub()`, it will receive the message.
- Remote - `receiver` isn't the current instance, and is subscribed to this `kind` via `sub_remote()`, it will receive the message.
- Broadcast - `receiver` is `0`, all remote instances subscribed to this `kind` via `sub_remote()` will receive the message.

| In/Out     | Type       | Note                                                                            |
| ---------- | ---------- | ------------------------------------------------------------------------------- |
| `receiver` | `integer`  | -                                                                               |
| `kind`     | `string`   | Alphanumeric with dashes, cannot be [built-in kinds](/docs/dds#kinds)           |
| `value`    | `Sendable` | A [Sendable value][sendable] that follows [Ownership transfer rules][ownership] |
| Return     | `unknown`  | -                                                                               |

#### `sub(kind, callback)` {#ps.sub}

Subscribe to local messages of `kind` and call the `callback` handler for it:

```lua
-- The same `kind` from the same plugin can only be subscribed once,
-- re-subscribing (`sub()`) before unsubscribing (`unsub()`) will throw an error.
ps.sub("cd", function(body)
	ya.dbg("New cwd", cx.active.current.cwd)
end)
```

It runs in a sync context, so you can access all states via `cx` for the data of interest.

| In/Out     | Type                  | Note                                                                  |
| ---------- | --------------------- | --------------------------------------------------------------------- |
| `kind`     | `string`              | Alphanumeric with dashes, cannot be [built-in kinds](/docs/dds#kinds) |
| `callback` | `fun(body: Sendable)` | No time-consuming work should be done in the callback                 |
| Return     | `unknown`             | -                                                                     |

#### `sub_remote(kind, callback)` {#ps.sub_remote}

Same as `sub()`, except it subscribes to remote messages of this `kind` instead of local.

| In/Out     | Type                  | Note            |
| ---------- | --------------------- | --------------- |
| `kind`     | `string`              | Same as `sub()` |
| `callback` | `fun(body: Sendable)` | Same as `sub()` |
| Return     | `unknown`             | -               |

#### `unsub(kind)` {#ps.unsub}

Unsubscribe from local messages of this `kind`:

```lua
ps.unsub("my-message")
```

| In/Out | Type      | Note                                                                  |
| ------ | --------- | --------------------------------------------------------------------- |
| `kind` | `string`  | Alphanumeric with dashes, cannot be [built-in kinds](/docs/dds#kinds) |
| Return | `unknown` | -                                                                     |

#### `unsub_remote(kind)` {#ps.unsub_remote}

Unsubscribe from remote messages of this `kind`:

```lua
ps.unsub_remote("my-message")
```

| In/Out | Type      | Note              |
| ------ | --------- | ----------------- |
| `kind` | `string`  | Same as `unsub()` |
| Return | `unknown` | -                 |

### Access {#access}

This object is created by [`fs.access()`](#fs.access) and represents the options for interacting with a file.

#### `read(self, read)` {#Access.read}

Sets the operation for read access.

```lua
local access = fs.access():read(true)
```

| In/Out | Type      |
| ------ | --------- |
| `self` | `Self`    |
| `read` | `boolean` |
| Return | `self`    |

#### `write(self, write)` {#Access.write}

Sets the operation for write access.

```lua
local access = fs.access():write(true)
```

| In/Out  | Type      |
| ------- | --------- |
| `self`  | `Self`    |
| `write` | `boolean` |
| Return  | `self`    |

#### `append(self, append)` {#Access.append}

Sets the operation for the append mode.

```lua
local access = fs.access():append(true)
```

| In/Out   | Type      |
| -------- | --------- |
| `self`   | `Self`    |
| `append` | `boolean` |
| Return   | `self`    |

#### `truncate(self, truncate)` {#Access.truncate}

Sets the operation for truncating a previous file.

```lua
local access = fs.access():truncate(true)
```

| In/Out     | Type      |
| ---------- | --------- |
| `self`     | `Self`    |
| `truncate` | `boolean` |
| Return     | `self`    |

#### `create(self, create)` {#Access.create}

Sets the operation to create a new file, or open it if it already exists.

```lua
local access = fs.access():create(true)
```

| In/Out   | Type      |
| -------- | --------- |
| `self`   | `Self`    |
| `create` | `boolean` |
| Return   | `self`    |

#### `create_new(self, create_new)` {#Access.create_new}

Sets the operation to create a new file, failing if it already exists.

```lua
local access = fs.access():create_new(true)
```

| In/Out       | Type      |
| ------------ | --------- |
| `self`       | `Self`    |
| `create_new` | `boolean` |
| Return       | `self`    |

#### `open(self, url)` {#Access.open}

Opens a file at `url` with the mode specified.

```lua
local url = Url("/tmp/test.txt")
local fd, err = fs.access():read(true):open(url)
```

Returns `(fd, err)`:

- `fd`: [Fd](#fd) (file descriptor) if the operation succeeds; otherwise, `nil`.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type               |
| --------- | ------------------ |
| `self`    | `Self`             |
| `url`     | `Url`              |
| Return    | `Fd?, Error?`      |
| Available | Async context only |

### Fd {#fd}

This object is created by [`Access:open()`](#access.open) and contains the methods for working with the opened file.

#### `write_all(self, bytes)` {#Fd.write_all}

Writes all `bytes` to the file descriptor.

```lua
local url = Url("/tmp/test.txt")

local fd, err = fs.access():write(true):open(url)
assert(fd, err)

local ok, err = fd:write_all("Hello, World!")
assert(ok, err)
```

Returns `(ok, err)`:

- `ok`: Whether the operation succeeds, which is a `boolean`.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type               |
| --------- | ------------------ |
| `self`    | `Self`             |
| `bytes`   | `string`           |
| Return    | `boolean, Error?`  |
| Available | Async context only |

#### `flush(self)` {#Fd.flush}

Flushes the file descriptor, making sure all data gets written to the underlying storage.

```lua
local url = Url("/tmp/test.txt")

local fd, err = fs.access():write(true):open(url)
assert(fd, err)

local ok, err = fd:flush()
assert(ok, err)
```

Returns `(ok, err)`:

- `ok`: Whether the operation succeeds, which is a `boolean`.
- `err`: [`Error`][error] of the failure.

| In/Out    | Type               |
| --------- | ------------------ |
| `self`    | `Self`             |
| Return    | `boolean, Error?`  |
| Available | Async context only |

### Command {#command}

You can invoke external programs through:

```lua
local child, err = Command("ls")
	:arg { "-a", "-l" }
	:stdout(Command.PIPED)
	:spawn()
```

Compared to Lua's `os.execute`, it provides many comprehensive and convenient methods, and the entire process is async.

It takes better advantage of the benefits of concurrent scheduling. However, it can only be used in async contexts, such as preloaders, previewers, and async functional plugins.

#### `NULL` {#Command.NULL}

A `Stdio` indicating that the stream will be ignored, which is the equivalent of attaching the stream to `/dev/null`.

|      |         |
| ---- | ------- |
| Type | `Stdio` |

#### `PIPED` {#Command.PIPED}

A `Stdio` indicating that a new pipe should be arranged to connect the parent and child processes.

|      |         |
| ---- | ------- |
| Type | `Stdio` |

#### `INHERIT` {#Command.INHERIT}

A `Stdio` indicating that the child inherits from the corresponding parent descriptor.

|      |         |
| ---- | ------- |
| Type | `Stdio` |

#### `arg(self, arg)` {#Command.arg}

Append one or more arguments to the command:

```lua
local cmd = Command("ls"):arg("-a"):arg("-l")
-- Equivalent to:
local cmd = Command("ls"):arg { "-a", "-l" }
```

| In/Out | Type                   |
| ------ | ---------------------- |
| `self` | `Self`                 |
| `arg`  | `string` \| `string[]` |
| Return | `self`                 |

#### `cwd(self, dir)` {#Command.cwd}

Set the current working directory of the command:

```lua
local cmd = Command("ls"):cwd("/root")
```

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| `dir`  | `string` |
| Return | `self`   |

#### `env(self, key, value)` {#Command.env}

Append an environment variable to the command:

```lua
local cmd = Command("ls"):env("PATH", "/bin"):env("HOME", "/home")
```

| In/Out  | Type     |
| ------- | -------- |
| `self`  | `Self`   |
| `key`   | `string` |
| `value` | `string` |
| Return  | `self`   |

#### `stdin(self, stdio)` {#Command.stdin}

Set the stdin of the command:

```lua
local cmd = Command("ls"):stdin(Command.PIPED)
```

Where `stdio` can be one of the following:

- `Command.PIPED`: Pipe the stdin.
- `Command.NULL`: Discard the stdin (default).
- `Command.INHERIT`: Inherit the stdin.

| In/Out  | Type    |
| ------- | ------- |
| `self`  | `Self`  |
| `stdio` | `Stdio` |
| Return  | `self`  |

#### `stdout(self, stdio)` {#Command.stdout}

Set the stdout of the command:

```lua
local cmd = Command("ls"):stdout(Command.PIPED)
```

Where `stdio` can be one of the following:

- `Command.PIPED`: Pipe the stdout.
- `Command.NULL`: Discard the stdout (default).
- `Command.INHERIT`: Inherit the stdout.

| In/Out  | Type    |
| ------- | ------- |
| `self`  | `Self`  |
| `stdio` | `Stdio` |
| Return  | `self`  |

#### `stderr(self, stdio)` {#Command.stderr}

Set the stderr of the command:

```lua
local cmd = Command("ls"):stderr(Command.PIPED)
```

Where `stdio` can be one of the following:

- `Command.PIPED`: Pipe the stderr.
- `Command.NULL`: Discard the stderr (default).
- `Command.INHERIT`: Inherit the stderr.

| In/Out  | Type    |
| ------- | ------- |
| `self`  | `Self`  |
| `stdio` | `Stdio` |
| Return  | `self`  |

#### `spawn(self)` {#Command.spawn}

Spawn the command:

```lua
local child, err = Command("ls"):spawn()
```

| In/Out | Type             |
| ------ | ---------------- |
| `self` | `Self`           |
| Return | `Child?, Error?` |

#### `output(self)` {#Command.output}

Executes the command as a child process, waiting for it to finish and collecting all of its output:

```lua
local output, err = Command("ls"):output()
```

This method sets both stdout and stderr to `Command.PIPED` and closes the stdin stream.

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| Return | `Output?, Error?` |

#### `status(self)` {#Command.status}

Executes the command as a child process, waiting for it to finish and collecting its exit status:

```lua
local status, err = Command("ls"):status()
```

This method closes the stdin, stdout, and stderr streams if they were set to `Command.PIPED`.

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| Return | `Status?, Error?` |

#### `__new(value)` {#command.\_\_new}

Make a new command.

| In/Out  | Type     |
| ------- | -------- |
| `value` | `string` |
| Return  | `Self`   |

### Child {#child}

This object is created by [`Command:spawn()`](#Command.spawn) and represents a running child process.

You can access the runtime data of this process through its proprietary methods.

#### `read(self, len)` {#Child.read}

Reads data from the available data source alternately:

```lua
local data, event = child:read(1024)
```

"available data source" refers to `stdout` or `stderr` that has `Command.PIPED` set, or them both, the `event` indicates where the data comes from:

- Data comes from stdout, if event is 0.
- Data comes from stderr, if event is 1.
- No data to read from both stdout and stderr, if event is 2.

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| `len`  | `integer`          |
| Return | `string?, integer` |

#### `read_line(self)` {#Child.read_line}

Same as [`read()`](#Child.read), except it reads data line by line:

```lua
local line, event = child:read_line()
```

| In/Out | Type               |
| ------ | ------------------ |
| `self` | `Self`             |
| Return | `string?, integer` |

#### `read_line_with(self, opts)` {#Child.read_line_with}

Same as [`read_line()`](#Child.read_line), except it accepts a table of options:

```lua
local line, event = child:read_line_with {
	-- Timeout to read
	timeout = 500,
}
```

It has an extra event:

- Timeout, if `event` is 3.

| In/Out | Type                   |
| ------ | ---------------------- |
| `self` | `Self`                 |
| `opts` | `{ timeout: integer }` |
| Return | `string?, integer`     |

#### `write_all(self, src)` {#Child.write_all}

Writes all `src` to the stdin of the child process:

```lua
local ok, err = child:write_all(src)
```

Ensure that the child's stdin is available when calling this method, specifically:

1. [`stdin(Command.PIPED)`](/docs/plugins/utils#Command.stdin) is set.
2. [`take_stdin()`](/docs/plugins/utils#Child.take_stdin) has never been called.

Otherwise, an error will be thrown.

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| `src`  | `string`          |
| Return | `boolean, Error?` |

#### `flush(self)` {#Child.flush}

Flushes any buffered data to the stdin of the child process:

```lua
local ok, err = child:flush()
```

Ensure that the child's stdin is available when calling this method, specifically:

1. [`stdin(Command.PIPED)`](/docs/plugins/utils#Command.stdin) is set.
2. [`take_stdin()`](/docs/plugins/utils#Child.take_stdin) has never been called.

Otherwise, an error will be thrown.

| In/Out   | Type              |
| -------- | ----------------- |
| `self`   | `Self`            |
| `Return` | `boolean, Error?` |

#### `wait(self)` {#Child.wait}

Wait for the child process to finish:

```lua
local status, err = child:wait()
```

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| Return | `Status?, Error?` |

#### `wait_with_output(self)` {#Child.wait_with_output}

Wait for the child process to finish and get the output:

```lua
local output, err = child:wait_with_output()
```

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| Return | `Output?, Error?` |

#### `start_kill(self)` {#Child.start_kill}

Send a SIGTERM signal to the child process:

```lua
local ok, err = child:start_kill()
```

| In/Out | Type              |
| ------ | ----------------- |
| `self` | `Self`            |
| Return | `boolean, Error?` |

#### `take_stdin(self)` {#Child.take_stdin}

Take and return the stdin stream of the child process:

```lua
local stdin = child:take_stdin()
```

This method can only be called once and is only applicable to processes with [`stdin(Command.PIPED)`](/docs/plugins/utils#Command.stdin) set;
otherwise, it returns `nil`.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `Stdio?` |

#### `take_stdout(self)` {#Child.take_stdout}

Take and return the stdout stream of the child process:

```lua
local stderr = child:take_stdout()
```

which is useful when redirecting stdout to another process's stdin:

```lua
local echo = Command("echo"):arg("Hello"):stdout(Command.PIPED):spawn()

local rev = Command("rev"):stdin(echo:take_stdout()):stdout(Command.PIPED):output()

ya.dbg(rev.stdout) -- "olleH\n"
```

This method can only be called once and is only applicable to processes with [`stdout(Command.PIPED)`](/docs/plugins/utils#Command.stdin) set;
otherwise, it returns `nil`.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `Stdio?` |

#### `take_stderr(self)` {#Child.take_stderr}

Take and return the stderr stream of the child process:

```lua
local stderr = child:take_stderr()
```

See [`take_stdout()`](/docs/plugins/utils#Child.take_stdout) for an example.

This method can only be called once and is only applicable to processes with [`stderr(Command.PIPED)`](/docs/plugins/utils#Command.stdin) set;
otherwise, it returns `nil`.

| In/Out | Type     |
| ------ | -------- |
| `self` | `Self`   |
| Return | `Stdio?` |

### Output {#output}

#### `status` {#output.status}

Status of the child process.

|      |                     |
| ---- | ------------------- |
| Type | [`Status`](#status) |

#### `stdout` {#output.stdout}

Stdout of the child process.

|      |          |
| ---- | -------- |
| Type | `string` |

#### `stderr` {#output.stderr}

Stderr of the child process.

|      |          |
| ---- | -------- |
| Type | `string` |

### Status {#status}

This object represents the exit status of a child process, and it is created by [`wait()`](#Child.wait), or [`output()`](#Command.output).

#### `success` {#status.success}

Whether the child process exited successfully.

|      |           |
| ---- | --------- |
| Type | `boolean` |

#### `code` {#status.code}

Exit code of the child process.

|      |            |
| ---- | ---------- |
| Type | `integer?` |

<!-- Links -->

[sendable]: /docs/plugins/overview#sendable
[ownership]: /docs/plugins/overview#ownership
[url]: /docs/plugins/types#url
[cha]: /docs/plugins/types#cha
[error]: /docs/plugins/types#error

---

## Builtins

Yazi comes with useful built-in plugins to help enhance your workflow without extra setup. This page introduces these built-in plugins and their available configuration options.

### `fzf.lua` {#fzf}

Integrate the power of [`fzf`](https://github.com/junegunn/fzf) into Yazi, allowing you to swiftly search and navigate through files and directories with fuzzy matching.

Source code: https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/fzf.lua

#### Usage

How to invoke fzf:

- Press <kbd>z</kbd> for quick file subtree navigation within CWD.
- Or, press <kbd>z</kbd> for quick navigation among selected items, if you are in selection mode.

If you exit fzf with a single-selected file:

- [`reveal`](/docs/configuration/keymap#mgr.reveal) the file.
- Or, [`cd`](/docs/configuration/keymap#mgr.cd) to it if it's a directory.

If you exit fzf with multiple-selected files:

- Select the files chosen by fzf in Yazi.
- Or, deselect the files chosen by fzf in Yazi, if you are in selection mode.

### `zoxide.lua` {#zoxide}

Enhance your experience of historical directories navigation with external shell, through [`zoxide`](https://github.com/ajeetdsouza/zoxide), a smarter `cd`.

Source code: https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/zoxide.lua

#### Usage

Click <kbd>Z</kbd> to launch the interactive zoxide UI. Please ensure that:

1. You have installed the latest version of zoxide.
2. You have installed the latest version of [fzf](https://github.com/junegunn/fzf), which is a dependency of zoxide.
3. You have correctly configured zoxide for your shell according to [its documentation](https://github.com/ajeetdsouza/zoxide?tab=readme-ov-file#installation).

#### Options

| Option             | Description                                              |
| ------------------ | -------------------------------------------------------- |
| `update_db` (bool) | Add the path to zoxide database whenever you change CWD. |

You can _optionally_ change certain options in your `init.lua` like this:

```lua
-- ~/.config/yazi/init.lua
require("zoxide"):setup {
	update_db = true,
}
```

---

## Aliases

### Origin {#origin}

A set of constants representing the origin of a position.

|       |                                                                                                                                          |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Alias | `"top-left"` \| `"top-center"` \| `"top-right"` \| `"bottom-left"` \| `"bottom-center"` \| `"bottom-right"` \| `"center"` \| `"hovered"` |

### Sendable {#sendable}

A value that can be sent across threads. See [Sendable value](/docs/plugins/overview#sendable) for more details.

|       |                                                                                   |
| ----- | --------------------------------------------------------------------------------- |
| Alias | `nil` \| `boolean` \| `number` \| `string` \| `Url` \| `{ [Sendable]: Sendable }` |

### Renderable {#renderable}

An element that can be rendered.

|       |                                                                       |
| ----- | --------------------------------------------------------------------- |
| Alias | `Bar` \| `Border` \| `Clear` \| `Gauge` \| `Line` \| `List` \| `Text` |

### AsPos {#as-pos}

A value that can be covariantly treated as a [`Pos`](/docs/plugins/layout#pos).

|       |                                                                                |
| ----- | ------------------------------------------------------------------------------ |
| Alias | `Pos` \| `{ [1]: Origin, x: integer?, y: integer?, w: integer?, h: integer? }` |

### AsSpan {#as-span}

A value that can be covariantly treated as a [`Span`](/docs/plugins/layout#span).

|       |                    |
| ----- | ------------------ |
| Alias | `string` \| `Span` |

### AsLine {#as-line}

A value that can be covariantly treated as a [`Line`](/docs/plugins/layout#line).

|       |                                                          |
| ----- | -------------------------------------------------------- |
| Alias | `string` \| `Span` \| `Line` \| `(string\|Span\|Line)[]` |

### AsText {#as-text}

A value that can be covariantly treated as a [`Text`](/docs/plugins/layout#text).

|       |                                                          |
| ----- | -------------------------------------------------------- |
| Alias | `string` \| `Span` \| `Line` \| `(string\|Span\|Line)[]` |

### AsColor {#as-color}

A set of constants representing colors.

|       |                                                                                                                                                                                                                                                                     |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Alias | `"black"` \| `"white"` \| `"red"` \| `"lightred"` \| `"green"` \| `"lightgreen"` \| `"yellow"` \| `"lightyellow"` \| `"blue"` \| `"lightblue"` \| `"magenta"` \| `"lightmagenta"` \| `"cyan"` \| `"lightcyan"` \| `"gray"` \| `"darkgray"` \| `"reset"` \| `string` |

---

## Flavors (BETA)

The "flavor" is a pre-made Yazi theme, while what we typically refer to as a "theme" is the user's own theme, i.e. `~/.config/yazi/theme.toml` file.

The purpose of separating them is to allow users to customize their preferences more conveniently on top of an existing flavor, without having to modify those flavor files.
This makes it easier to update, as there won't be conflicts when pulling from Git.

Behind the scenes, Yazi merges the user's `theme.toml` with the flavor's `flavor.toml` automatically, and the user's always takes precedence over the flavor.

### Directory structure {#structure}

These flavors are placed in the `flavors` subdirectory of the Yazi configuration directory, so either:

- `~/.config/yazi/flavors/` on Unix-like systems.
- `%AppData%\yazi\config\flavors\` on Windows.

```
~/.config/yazi/
├── flavors/
│   ├── foo.yazi/
│   └── bar.yazi/
└── theme.toml
```

Each flavor is a directory with a [kebab-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case) name, ending in `.yazi`, and containing at least the following files:

```
~/.config/yazi/flavors/bar.yazi/
├── flavor.toml
├── tmtheme.xml
├── README.md
├── preview.png
├── LICENSE
└── LICENSE-tmtheme
```

Where:

- `flavor.toml` is this flavor's configuration file, in the format consistent with the [user's `theme.toml`](/docs/configuration/theme).
- `tmtheme.xml` is a [tmTheme file](https://www.sublimetext.com/docs/color_schemes_tmtheme.html) that matches the colors of this flavor for code highlighting.
- `README.md` and `preview.png` are the description and the preview image of this flavor, respectively.
- `LICENSE` and `LICENSE-tmtheme` are the licenses for the flavor and the `tmtheme.xml` file, respectively.

### Usage {#usage}

For example, if you want to use the `bar.yazi` flavor in _dark_ mode, set the content of your `theme.toml` to:

```toml
[flavor]
dark = "bar"
```

or use it in _light_ mode:

```toml
[flavor]
light = "bar"
```

If you want to use the `bar.yazi` flavor in both _dark_ and _light_ modes:

```toml
[flavor]
dark  = "bar"
light = "bar"
```

Make sure your `theme.toml` doesn't contain anything other than `[flavor]`, unless you want to override certain styles of the `bar.yazi` flavor.

### Why flavors over themes? {#why-flavor}

We recommend using the new flavor format instead of the old theme, because flavors:

- More powerful - auto dark/light mode switching with the terminal
- Easier to update - can be managed with the [`ya pkg` package manager](/docs/cli#pm)
- Offers configuration merging - override some styles from `flavor.toml` in your own `theme.toml`

### Why is my flavor/theme not working? {#why-not-working}

This is usually because the flavor or theme contains outdated color configurations. Please ensure that your flavor or theme is compatible with your Yazi version:

1. **No invalid fields**

   You can use a TOML linter like [taplo](https://taplo.tamasfe.dev) to check if your `theme.toml` or `flavor.toml` contains any invalid fields:

   ```sh
   taplo check --schema https://yazi-rs.github.io/schemas/theme.json flavor.toml
   ```

2. **Includes fields for components you want to stylize**

   A Yazi theme or flavor can optionally stylize only certain components, i.e., it doesn't necessarily style everything. For components without a specified style, the [preset configuration](https://github.com/sxyazi/yazi/tree/shipped/yazi-config/preset) will be applied.

   See [theme.toml](/docs/configuration/theme) for a complete list of available fields, and make sure your `theme.toml` or `flavor.toml` includes them.

### Cooking a flavor {#cooking}

Please use our [flavor-template](https://github.com/yazi-rs/flavor-template) repository as a starting point to create your own flavor.

---

## CLI

Yazi provides a command-line tool called `ya`, which is used to assist with tasks like plugin management, flavor management, DDS message publishing and subscribing, among other features.

It is an essential component of Yazi. Most distributions include it by default when installing Yazi, but if yours doesn't, you'll need to [build it from source](/docs/installation#source). Just be sure that the versions of both `ya` and `yazi` are exactly the same.

### Package Manager {#pm}

You can manage your plugins and flavors using the `ya pkg` subcommand. For example, to install the plugin from https://github.com/owner/my-plugin.yazi, run:

```sh
ya pkg add owner/my-plugin
```

`ya pkg` also supports installing a subdirectory from a monorepo as a package. For example, to install the package from https://github.com/yazi-rs/plugins/tree/main/git.yazi, run:

```sh
ya pkg add yazi-rs/plugins:git
```

and it will automatically clone them from GitHub, copy them to your plugins directory, and update the `package.toml` to lock their versions:

```toml
## ~/.config/yazi/package.toml
[[plugin.deps]]
use  = "owner/my-plugin"
rev  = "0573024"
hash = "d81b64a39432fcd6224cd75d296e7510"

[[plugin.deps]]
use  = "yazi-rs/plugins:git"
rev  = "9a1129c"
hash = "a8e15d3c21c02a5af41d46ed04778a02"
```

To delete a plugin:

```sh
ya pkg delete yazi-rs/plugins:git
```

To list all the plugins managed by `ya pkg`:

```sh
ya pkg list
```

To install all the plugins with locked versions from `package.toml` on a new system:

```sh
ya pkg install
```

To upgrade all the plugins to the latest version:

```sh
ya pkg upgrade
```

If you want to pin a plugin to a specific version so that it doesn't get upgraded when running `ya pkg upgrade`, add an `=` qualifier before the hash in `rev`:

```diff
[[plugin.deps]]
use = "owner/my-plugin"
- rev = "9a1129c"
+ rev = "=9a1129c"
```

For `add` and `delete`, they can accept multiple arguments, which means you can operate on multiple packages at once:

```sh
ya pkg add owner/my-plugin yazi-rs/plugins:git
ya pkg delete owner/my-plugin yazi-rs/plugins:git
```

### Data Distribution Service {#dds}

You can use `ya` as a user interface to interact with the data distribution service.

See the [DDS section](/docs/dds) for more information.

---

## DDS

DDS (Data Distribution Service) is designed to achieve communication and state synchronization between multiple Yazi instances, as well as state persistence. It is built on a client-server architecture but does not require running additional server processes.

It deeply integrates with a publish-subscribe model based on the Lua API.

### Concept {#concept}

- Local: the current instance, that is, the current Yazi process.
- Remote: instances other than the current instance.
- Static message: A message with a kind that starts with `@` will be persistently stored and automatically restored when a new instance starts. To un-persist, send `nil` to that kind.

### Usage {#usage}

The DDS has three usage:

- [Plugin API](/docs/plugins/utils#ps): Using Lua-based publish-subscribe model as the message carrier.
- [`ya pub` and `ya pub-to`](#ya-pub): Using [`ya` CLI tool](/docs/cli) as the message carrier.
- [`ya emit` and `ya emit-to`](#ya-emit): Using [`ya` CLI tool](/docs/cli) as the action carrier.
- [Real-time `stdout` reporting](#stdout-reporting): Using `stdout` as the carrier.

#### `ya pub` and `ya pub-to` {#ya-pub}

If you're in a Yazi subshell where the `$YAZI_ID` environment variable is set, you can send a message to the current instance using `ya pub`.
It requires a `kind` argument, which is consistent with [`ps.pub()`](/docs/plugins/utils#ps.pub):

```sh
ya pub <kind> --str "string body"
ya pub <kind> --list "a" "b" "c"
ya pub <kind> --json '{"key":"json body"}'

## For example, request the current instance to extract `a.zip` and `b.7z`
ya pub extract --list "/root/a.zip" "/root/b.7z"
```

You can also send a message to a specified remote instance(s) using `ya pub-to`, with the required `receiver` and `kind` arguments, consistent with [`ps.pub_to()`](/docs/plugins/utils#ps.pub_to):

```sh
ya pub-to <receiver> <kind> --str "string body"
ya pub-to <receiver> <kind> --list "a" "b" "c"
ya pub-to <receiver> <kind> --json '{"key":"json body"}'

## If you're in a Yazi subshell,
## you can obtain the ID of the current instance through `$YAZI_ID`.
ya pub-to "$YAZI_ID" my-event --str "Hello world!"

## If you are not in a Yazi subshell, i.e., communicating with Yazi externally,
## you can start with `yazi --client-id <globally-unique-id>`, and pass that ID to `ya pub-to`.
MY_UNIQUE_ID="$(date +%s)$RANDOM"
yazi --client-id "$MY_UNIQUE_ID"
ya pub-to "$MY_UNIQUE_ID" my-event --str "Hello world!"
```

For greater convenience in integrating within the command-line environment, they support two body formats:

- String: a straightforward format, suitable for most scenarios, without the need for additional tools for encoding
- List: An array of strings, it is useful for carrying a file list to the message
- JSON: for advanced needs, support for types and more complex data can be represented through the JSON format

#### `ya emit` and `ya emit-to` {#ya-emit}

If you're in a Yazi subshell where the `$YAZI_ID` environment variable is set, you can use `ya emit` to send an action to the current instance for execution.

The action format is the same as what you'd write in the [`keymap.toml`](/docs/configuration/keymap):

```sh
ya emit <action> <args>
```

For example:

```sh
ya emit cd /tmp
ya emit reveal /tmp/foo
```

You can also send actions to a specific remote instance using `ya emit-to`:

```sh
ya emit-to <receiver> <action> <args>
```

For example:

```sh
ya emit-to "$YAZI_ID" cd /tmp
```

#### Real-time `stdout` reporting {#stdout-reporting}

You can specify the `--local-events` and `--remote-events` options when starting Yazi:

```sh
## Local events
yazi --local-events=kind1,kind2
## Remote events
yazi --remote-events=kind1,kind2
## Both local and remote events
yazi --local-events=kind1,kind2 --remote-events=kind1,kind2
```

When an event of the specified kind is received, it will be output to `stdout`:

```sh
hover,0,200,{"tab":0,"url":"/root/Downloads"}
cd,0,100,{"tab":0,"url":"/root/Downloads"}
```

One payload per line, each payload contains the following fields separated by commas:

| Field    | Description                                                                                       |
| -------- | ------------------------------------------------------------------------------------------------- |
| kind     | The kind of the message                                                                           |
| receiver | The remote instance ID that receives the message; if it's `0`, broadcasts to all remote instances |
| sender   | The sender of the message                                                                         |
| body     | The body of the message, which is a JSON string                                                   |

This provides the ability to report Yazi's internal events in real-time, which is useful for external tool integration (such as Neovim), as they will be able to subscribe to the events triggered by the user behavior.

### Builtin kinds {#kinds}

#### `cd` - change directory {#cd}

`sub()` callback body:

```lua
{
	tab = 0
}
```

`sub_remote()` callback body:

```lua
{
	tab = 0,
	url = Url("/root/Downloads")
}
```

`--local-events` stdout payload:

```sh
cd,1711957542289249,1711957542289249,{"tab":0,"url":"/root/Downloads"}
```

`--remote-events` stdout payload:

```sh
cd,0,100,{"tab":0,"url":"/root/Downloads"}
```

#### `hover` - hover over a file {#hover}

`sub()` callback body:

```lua
{
	tab = 0
}
```

`sub_remote()` callback body:

```lua
{
	tab = 0,
	url = Url("/root/foo.txt")
}
```

`--local-events` stdout payload:

```sh
hover,1711957283332834,1711957283332834,{"tab":0,"url":"/root/foo.txt"}
```

`--remote-events` stdout payload:

```sh
hover,0,200,{"tab":0,"url":"/root/foo.txt"}
```

#### `rename` - rename a file {#rename}

`sub()` / `sub_remote()` callback body:

```lua
{
  tab = 0,
  from = Url("/root/foo.txt"),
  to = Url("/root/bar.txt"),
}
```

`--local-events` stdout payload:

```sh
rename,1711957878076791,1711957878076791,{"tab":0,"from":"/root/foo.txt","to":"/root/bar.txt"}
```

`--remote-events` stdout payload:

```sh
rename,0,1711957878076791,{"tab":0,"from":"/root/foo.txt","to":"/root/bar.txt"}
```

#### `bulk` - bulk rename files {#bulk}

`sub()` / `sub_remote()` callback body:

```lua
-- Since `Iterator` implementing `__pairs()`,
-- you can iterate over all URL pairs using `pairs(body)`
Iterator {
	__len = function(self)
		-- Returns the number of files changed
	end,
	__pairs = function(self)
		-- Returns (Url("/path/from.txt"), Url("/path/to.txt"))
	end
}
```

`--local-events` stdout payload:

```sh
bulk,1711957542289249,1711957542289249,{"changes":{"/path/from.txt":"/path/to.txt"}}
```

`--remote-events` stdout payload:

```sh
bulk,0,1711957542289249,{"changes":{"/path/from.txt":"/path/to.txt"}}
```

#### `@yank` - yank files {#@yank}

`sub()` callback body:

```lua
{}
```

`sub_remote()` callback body:

```lua
-- The `Iterator` implements `__pairs()`, so you can iterate over all URLs with `pairs()`
Iterator {
	cut = false,
	__len = function(self)
		-- Returns the number of URLs yanked
	end,
	__pairs = function(self)
		-- Returns next URL
	end
}
```

`--local-events` stdout payload:

```sh
@yank,1711960311454247,1711960311454247,{"cut":false,"urls":["/root/foo.txt","/root/bar.txt"]}
```

`--remote-events` stdout payload:

```sh
@yank,0,300,{"cut":false,"urls":["/root/foo.txt","/root/bar.txt"]}
```

#### `move` - move files {#move}

`sub()` callback body:

```lua
{
	items = {
		{ from = Url("/root/foo.txt"), to = Url("/root/bar.txt") },
		-- ...
	}
}
```

`sub_remote()` callback body:

```lua
{
	items = {
		{ from = Url("/root/foo.txt"), to = Url("/root/bar.txt") },
		-- ...
	}
}
```

`--local-events` stdout payload:

```sh
move,1711957542289249,1711957542289249,{"items":[{"from":"/root/foo.txt","to":"/root/bar.txt"}]}
```

`--remote-events` stdout payload:

```sh
move,0,1711957542289249,{"items":[{"from":"/root/foo.txt","to":"/root/bar.txt"}]}
```

#### `trash` - trash files {#trash}

`sub()` callback body:

```lua
{
	urls = {
		Url("/root/foo.txt"),
		-- ...
	}
}
```

`sub_remote()` callback body:

```lua
{
	urls = {
		Url("/root/foo.txt"),
		-- ...
	}
}
```

`--local-events` stdout payload:

```sh
trash,1711957542289249,1711957542289249,{"urls":["/root/foo.txt"]}
```

`--remote-events` stdout payload:

```sh
trash,0,1711957542289249,{"urls":["/root/foo.txt"]}
```

#### `delete` - delete files {#delete}

`sub()` callback body:

```lua
{
	urls = {
		Url("/root/foo.txt"),
		-- ...
	}
}
```

`sub_remote()` callback body:

```lua
{
	urls = {
		Url("/root/foo.txt"),
		-- ...
	}
}
```

`--local-events` stdout payload:

```sh
delete,1711957542289249,1711957542289249,{"urls":["/root/foo.txt"]}
```

`--remote-events` stdout payload:

```sh
delete,0,1711957542289249,{"urls":["/root/foo.txt"]}
```

#### `hi` - client handshake {#hi}

System reserves kind.

#### `hey` - server handshake {#hey}

System reserves kind.

#### `bye`

System reserves kind.

### Builtin plugins {#plugins}

#### `dds.lua` {#dds.lua}

This plugin provides a `dds-emit` event kind, which is used for the implementation of the `ya emit` subcommand — `ya emit` is a shorthand for `ya pub`, and the emitted action will be converted into an equivalent `ya pub` event message.

With `ya emit`, you can implement many interesting features, such as synchronizing the CWD of the current Yazi instance when exiting from a subshell:

<Tabs>
  <TabItem value="Zsh" label="Zsh" default>

```sh
## Change Yazi's CWD to PWD on subshell exit
if [[ -n "$YAZI_ID" ]]; then
	function _yazi_cd() {
		ya emit cd "$PWD"
	}
	add-zsh-hook zshexit _yazi_cd
fi
```

  </TabItem>
  <TabItem value="fish" label="Fish">

```sh
## Change Yazi's CWD to PWD on subshell exit
if [ -n "$YAZI_ID" ]
	trap 'ya emit cd "$PWD"' EXIT
end
```

  </TabItem>
  <TabItem value="nushell" label="Nushell">

```sh
## Please raise a PR if you have a nushell version
```

  </TabItem>
</Tabs>

Source code: https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/dds.lua

#### `session.lua` {#session.lua}

This plugin provides cross-instance yank ability, which means you can yank files in one instance, and then paste them in another instance.

To enable it, add these lines to your `init.lua`, then restart _all_ Yazi instances to apply the changes:

```lua
require("session"):setup {
	sync_yanked = true,
}
```

Source code: https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/session.lua

#### `extract.lua` {#extract.lua}

This plugin provides an `extract` event kind for archive extraction, which accepts an array of file URL. You can bind it as [the opener](/docs/configuration/yazi#opener) for archives:

```toml
## ~/.config/yazi/yazi.toml
[opener]
extract = [
	{ run = "ya pub extract --list %s", desc = "Extract here" },
]
```

Source code: https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/extract.lua

---

## Tips

These tips require prior knowledge of the Yazi configuration file.

If you are using Yazi for the first time, please read our [configuration](/docs/configuration/overview) and [plugins](/docs/plugins/overview) documentation first.

### Full border {#full-border}

<img src={useBaseUrl("/webp/full-border.webp")} width="600" />

Moved to: https://github.com/yazi-rs/plugins/tree/main/full-border.yazi

### Dropping to the shell {#dropping-to-shell}

Add this keybinding to your `keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on   = "!"
for  = "unix"
run  = 'shell "$SHELL" --block'
desc = "Open $SHELL here"

## If you also using Yazi on Windows:
[[mgr.prepend_keymap]]
on   = "!"
for  = "windows"
run  = 'shell "powershell.exe" --block'
desc = "Open PowerShell here"
```

### Close input by once <kbd>Esc</kbd> press {#close-input-by-esc}

You can change the <kbd>Esc</kbd> of input component from the default `escape` to `close` action, in your `keymap.toml`:

```toml
[[input.prepend_keymap]]
on   = "<Esc>"
run  = "close"
desc = "Cancel input"
```

to exiting input directly, without entering Vi mode, making it behave like a regular input box.

### Smart enter: `open` files or `enter` directories all in one key {#smart-enter}

Moved to: https://github.com/yazi-rs/plugins/tree/main/smart-enter.yazi

### Smart paste: `paste` files without entering the directory {#smart-paste}

Moved to: https://github.com/yazi-rs/plugins/tree/main/smart-paste.yazi

### Smart tab: create a tab and enter the hovered directory {#smart-tab}

Save these lines as `~/.config/yazi/plugins/smart-tab.yazi/main.lua`:

```lua
--- @sync entry
return {
	entry = function()
		local h = cx.active.current.hovered
		ya.emit("tab_create", h and h.cha.is_dir and { h.url } or { current = true })
	end,
}
```

Then bind it to the <kbd>t</kbd> key, in your `keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on   = [ "t", "t" ]
run  = "plugin smart-tab"
desc = "Create a tab and enter the hovered directory"
```

### Smart switch: create tab if the tab being switched to does not exist {#smart-switch}

Save these lines as `~/.config/yazi/plugins/smart-switch.yazi/main.lua`:

```lua
--- @sync entry
local function entry(_, job)
	local cur = cx.active.current
	for _ = #cx.tabs, job.args[1] do
		ya.emit("tab_create", { cur.cwd })
		if cur.hovered then
			ya.emit("reveal", { cur.hovered.url })
		end
	end
	ya.emit("tab_switch", { job.args[1] })
end

return { entry = entry }
```

Then bind it to the <kbd>2</kbd> key, in your `keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on   = "2"
run  = "plugin smart-switch 1"
desc = "Switch or create tab 2"
```

### Folder-specific rules {#folder-rules}

You can subscribe to directory change events through the [`cd` event provided by DDS](/docs/dds#cd), and then do any action you want, such as setting different sorting methods for specific directories.

The following code demonstrates making the `Downloads` directory to sort by modification time, while others are sorted alphabetically. Save these lines as `~/.config/yazi/plugins/folder-rules.yazi/main.lua`:

```lua
local function setup()
	ps.sub("ind-sort", function(opt)
		local cwd = cx.active.current.cwd
		if cwd:ends_with("Downloads") then
			opt.by, opt.reverse, opt.dir_first = "mtime", true, false
		else
			opt.by, opt.reverse, opt.dir_first = "natural", false, true
		end
		return opt
	end)
end

return { setup = setup }
```

Then enable it in your `~/.config/yazi/init.lua`:

```lua
require("folder-rules"):setup()
```

Thanks to @tianze0926 for [sharing it](https://github.com/sxyazi/yazi/issues/623#issuecomment-2096270843).

### Folder-specific previewer and preloader {#folder-previewer}

In addition to the `mime` rules, Yazi also has `url` rules for pre\{viewer,loader}, which accept a URL pattern.
This allows for flexible creation of different pre\{viewer,loader} rules for various directories.

For example, you can use the `noop` builtin preloader for a remote mount point like `/remote`, disabling preloads in that directory:

```toml
## yazi.toml
[[plugin.prepend_preloaders]]
url = "/remote/**"
run = "noop"
```

If you want to disable all the preset previewers, preloaders:

```toml
## yazi.toml
[plugin]
preloaders = []
previewers = []
```

### Drag and drop via [`dragon`](https://github.com/mwh/dragon) {#drag-and-drop}

Original post: https://github.com/sxyazi/yazi/discussions/327

```toml
[[mgr.prepend_keymap]]
on  = "<C-n>"
run = "shell -- dragon -x -i -T %h"
```

### Set a wallpaper

To set a wallpaper with the "Open with" menu (<kbd>O</kbd> key by default), add a `set-wallpaper` opener in your `yazi.toml` by choosing the appropriate command for your desktop environment:

```toml
## Linux: Hyprland + Hyprpaper
[[opener.set-wallpaper]]
run  = "hyprctl hyprpaper reload ,%s1"
for  = "linux"
desc = "Set as wallpaper"

## Linux: Swaybg
[[opener.set-wallpaper]]
run  = "killall swaybg; swaybg -m fill -i %s1"
for  = "linux"
desc = "Set as wallpaper"
orphan = true

## macOS
[[opener.set-wallpaper]]
run = '''
	osascript -e 'on run {img}' -e 'tell application "System Events" to set picture of every desktop to img' -e 'end run' %s1
'''
for  = "macos"
desc = "Set as wallpaper"
```

Then apply the `set-wallpaper` opener to the image files:

```toml
## yazi.toml
[[open.prepend_rules]]
mime = "image/*"
use  = [ "set-wallpaper", "open" ]
```

Alternatively, you can also change the wallpaper with a keybinding, for example <kbd>Ctrl</kbd> + <kbd>w</kbd>:

```toml
## keymap.toml
[[mgr.prepend_keymap]]
on   = "<C-w>"
for  = "linux"
run  = "shell -- hyprctl hyprpaper reload ,%h"
desc = "Set hovered file as wallpaper"
```

The above example is for Hyprland + Hyprpaper, adapt to the command of your respective DE as needed.

### Linux: Copy selected files to the system clipboard while yanking {#selected-files-to-clipboard}

Yazi allows multiple actions to be bound to a single key, so you can set <kbd>y</kbd> to not only do the `yank` but also run a shell script:

```toml
[[mgr.prepend_keymap]]
on  = "y"
run = [ "shell -- echo %s | xclip -i -selection clipboard -t text/uri-list", "yank" ]
```

The above is available on X11, there is also a Wayland version (Thanks to @hurutparittya for [sharing it](https://discord.com/channels/1136203602898194542/1136203604076802092/1188498323867455619) in the Discord server):

```toml
[[mgr.prepend_keymap]]
on  = "y"
run = [ 'shell -- for path in %s; do echo "file://$path"; done | wl-copy -t text/uri-list', "yank" ]
```

### `cd` back to the root of the current Git repository {#cd-to-git-root}

```toml
[[mgr.prepend_keymap]]
on = [ "g", "r" ]
run = 'shell -- ya emit cd "$(git rev-parse --show-toplevel)"'
```

Thanks to @aidanzhai for [sharing it](https://t.me/yazi_rs/3325/15373) in the Telegram group.

### Unix: Add subtitle to the running MPV {#mpv-subtitle}

Add these lines to your `~/.config/yazi/yazi.toml`:

```toml
[[opener.add-sub]]
run  = ''' printf "sub-add '%%s'\n" %s1 | socat - /tmp/mpv.sock '''
desc = "Add sub to MPV"

[[open.prepend_rules]]
url = "*.{ass,srt,ssa,sty,sup,vtt}"
use = [ "add-sub", "edit" ]
```

To make it work, make sure you've:

1. Installed `socat` and can be found in your `$PATH`
2. Enabled and configured the ipc socket to `/tmp/mpv.sock`, that is, include:
   ```
   input-ipc-server=/tmp/mpv.sock
   ```
   in your `~/.config/mpv/mpv.conf`. See [the documentation of `--input-ipc-server`](https://mpv.io/manual/stable/#options-input-ipc-server) for more info.

### Linux: Grid view with Rofi {#grid-view}

This tip lets you preview thumbnails in the current directory using [Rofi](https://github.com/davatorium/rofi/), selecting an item reveals it in Yazi:

```toml
## ~/.config/yazi/keymap.toml
[[mgr.prepend_keymap]]
on   = "<C-g>"
run  = 'shell -- rofi -theme fullscreen-preview -show filebrowser -filebrowser-command "ya emit reveal" -filebrowser-directory "$(pwd)"'
desc = "Grid view"
```

Rofi themes: https://davatorium.github.io/rofi/themes/themes

<details>
  <summary>Demonstrate grid view</summary>
	<p>Original post on the Discord server: https://discord.com/channels/1136203602898194542/1136203604076802092/1312811541300772934</p>
	<video src="https://github.com/user-attachments/assets/a79b13d3-612e-43a5-9ffb-9ddf1549766c" width="100%" controls muted></video>
</details>

### Maximize preview pane {#max-preview}

Moved to: https://github.com/yazi-rs/plugins/tree/main/toggle-pane.yazi

### Hide preview pane {#hide-preview}

Moved to: https://github.com/yazi-rs/plugins/tree/main/toggle-pane.yazi

### Navigation in the parent directory without leaving the CWD {#parent-arrow}

Save these lines as `~/.config/yazi/plugins/parent-arrow.yazi/main.lua`:

<Tabs>
  <TabItem value="classic" label="Classic" default>

```lua
--- @sync entry
local function entry(_, job)
	local parent = cx.active.parent
	if not parent then return end

	local target = parent.files[parent.cursor + 1 + job.args[1]]
	if target and target.cha.is_dir then
		ya.emit("cd", { target.url })
	end
end

return { entry = entry }
```

  </TabItem>
  <TabItem value="skip-files" label="Skip files">

```lua
--- @sync entry
local function entry(_, job)
	local parent = cx.active.parent
	if not parent then return end

	local offset = tonumber(job.args[1])
	if not offset then return ya.err(job.args[1], 'is not a number') end

	local start = parent.cursor + 1 + offset
	local end_ = offset < 0 and 1 or #parent.files
	local step = offset < 0 and -1 or 1
	for i = start, end_, step do
		local target = parent.files[i]
		if target and target.cha.is_dir then
			return ya.emit("cd", { target.url })
		end
	end
end

return { entry = entry }
```

  </TabItem>
</Tabs>

Then bind it for <kbd>K</kbd> and <kbd>J</kbd> key, in your `keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on  = "K"
run = "plugin parent-arrow -1"

[[mgr.prepend_keymap]]
on  = "J"
run = "plugin parent-arrow 1"
```

### Confirm before quitting if multiple tabs are open {#confirm-quit}

Save these lines as `~/.config/yazi/plugins/confirm-quit.yazi/main.lua`:

```lua
local count = ya.sync(function() return #cx.tabs end)

local function entry()
	if count() < 2 then
		return ya.emit("quit", {})
	end

	local yes = ya.confirm {
		pos = { "center", w = 62, h = 10 },
		title = "Quit?",
		body = ui.Text("There are multiple tabs open. Are you sure you want to quit?"):wrap(ui.Wrap.YES),
	}
	if yes then
		ya.emit("quit", {})
	end
end

return { entry = entry }
```

Next, bind it to the <kbd>q</kbd> key in your `keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on  = "q"
run = "plugin confirm-quit"
```

Thanks to @lpnh for [sharing it](https://github.com/sxyazi/yazi/issues/2267#issuecomment-2624805134).

### No status bar {#no-status-bar}

<img src={useBaseUrl("/webp/no-status-bar.webp")} width="600" />

Moved to: https://github.com/yazi-rs/plugins/tree/main/no-status.yazi

### Show symlink in status bar {#symlink-in-status}

<img src={useBaseUrl("/webp/symlink-in-status.webp")} width="600" />

Add the following code to your `~/.config/yazi/init.lua`:

```lua
Status:children_add(function(self)
	local h = self._current.hovered
	if h and h.link_to then
		return " -> " .. tostring(h.link_to)
	else
		return ""
	end
end, 3300, Status.LEFT)
```

### Show user/group of files in status bar {#user-group-in-status}

<img src={useBaseUrl("/webp/owner.webp")} width="600" />

Add the following code to your `~/.config/yazi/init.lua`:

```lua
Status:children_add(function()
	local h = cx.active.current.hovered
	if not h or ya.target_family() ~= "unix" then
		return ""
	end

	return ui.Line {
		ui.Span(ya.user_name(h.cha.uid) or tostring(h.cha.uid)):fg("magenta"),
		":",
		ui.Span(ya.group_name(h.cha.gid) or tostring(h.cha.gid)):fg("magenta"),
		" ",
	}
end, 500, Status.RIGHT)
```

### Show username and hostname in header {#username-hostname-in-header}

<img src={useBaseUrl("/webp/hostname-in-header.webp")} width="600" />

Add the following code to your `~/.config/yazi/init.lua`:

```lua
Header:children_add(function()
	if ya.target_family() ~= "unix" then
		return ""
	end
	return ui.Span(ya.user_name() .. "@" .. ya.host_name() .. ":"):fg("blue")
end, 500, Header.LEFT)
```

### macOS: Preview files with the system Quick Look {#macos-quick-look}

```toml
[[mgr.prepend_keymap]]
on = "<C-p>"
run = "shell -- qlmanage -p %s"
```

Thanks to @UncleGravity for [sharing it](https://discord.com/channels/1136203602898194542/1146658361740369960/1293471643959558156) in the Discord server.

### Specify a different editor for bulk renaming {#bulk-editor}

For bulk renaming, Yazi finds the first matching opener in your [`[open]`](/docs/configuration/yazi#open) rules with:

|         | Value               |
| ------- | ------------------- |
| `block` | `true`              |
| `url`   | `"bulk-rename.txt"` |
| `mime`  | `"text/plain"`      |

to use as the editor for editing the file list, and wait for the command to finish to know editing is finished.

By default, this matches your editor used for opening normal text files, if you want to use an editor different from that:

```toml
## ~/.config/yazi/yazi.toml
[[opener.bulk-rename]]
run   = "code --wait %s"
block = true

[[open.prepend_rules]]
url = "bulk-rename.txt"
use = "bulk-rename"
```

### Linux: Yazi as your system file chooser {#system-chooser}

The `xdg-desktop-portal-termfilechooser` backend lets you replace the default file picker with Yazi, providing seamless integration with applications, such as Firefox.

For installation steps, refer to the [installation guide](https://github.com/hunkyburrito/xdg-desktop-portal-termfilechooser?tab=readme-ov-file#installation) and additional instructions available there.

### File tree picker in Helix {#helix}

Yazi can be used as a file picker to browse and open file(s) in Helix with a keybind, e.g. <kbd>Ctrl</kbd> + <kbd>y</kbd>:

```toml
## ~/.config/helix/config.toml
[keys.normal]
C-y = [
	':sh rm -f /tmp/unique-ca1ea106',
	':insert-output yazi "%{buffer_name}" --chooser-file=/tmp/unique-ca1ea106',
	':sh printf "\x1b[?1049h\x1b[?2004h" > /dev/tty',
	':open %sh{cat /tmp/unique-ca1ea106}',
	':redraw',
	':set mouse false',
  ':set mouse true',
]
```

Original post: https://github.com/sxyazi/yazi/pull/2461

<details>
  <summary>Demonstrate Helix+Yazi workflow</summary>
	<video src="https://github.com/user-attachments/assets/17a370d5-ee50-4cfa-8292-ed3159058ac6" width="100%" controls muted></video>
</details>

### Email selected files

To send selected files using [Thunderbird](https://www.thunderbird.net), with a keybinding <kbd>Ctrl</kbd> + <kbd>m</kbd>:

```toml
## ~/.config/yazi/keymap.toml
[[mgr.prepend_keymap]]
on  = "<C-m>"
run = '''shell --
	paths=$(for p in %s; do echo "$p"; done | paste -s -d,)
	thunderbird -compose "attachment='$paths'"
'''
```

Or, use the [NeoMutt](https://neomutt.org) command-line mail client:

```toml
## ~/.config/yazi/keymap.toml
[[mgr.prepend_keymap]]
on  = "<C-m>"
run = "shell --block -- neomutt -a %s"
```

### Make Yazi even faster than fast {#make-yazi-even-faster}

While Yazi is already fast, there is still plenty of room for optimization for specific users or under certain conditions:

- For users who don't need image previews at all, disabling the default `image` previewer and preloader will make Yazi faster by reducing the I/O read file and CPU decode image consumption.
- For users managing network files, it's recommended to [disable all previewers and preloaders](/docs/tips#folder-previewer) since previewing and preloading these files means they need to be downloaded locally.
- For low-spec devices like Raspberry Pi, [reducing the concurrency](/docs/configuration/yazi#tasks) will make Yazi faster since the default configuration is optimized for PCs, and high concurrency on these low-spec devices may have the opposite effect.
- For users who don't need accurate mime-type, [`mime-ext.yazi`](https://github.com/yazi-rs/plugins/tree/main/mime-ext.yazi) may be useful, as it simply returns mime-type based on file extensions, while Yazi defaults to obtaining mime-type based on file content for accuracy. Mime-type is used for matching opening, previewing, rendering rules. Encourage users to choose an appropriate `mime` plugin based on their needs, which is why we decided to open it up to plugin developers.
- For high-performance terminal emulators, lowering the [`image_delay` option](/docs/configuration/yazi/#preview.image_delay) or setting it to 0 can reduce image preview latency.

---

## Resources

:::warning
The plugin system is still in the early stage, and most of the plugins below only guarantee compatibility with the latest code of Yazi!

Please make sure that both your Yazi and plugins are on the `HEAD` to ensure proper functionality!
:::

### 🖼️ Previewers {#previewers}

General:

- [piper.yazi](https://github.com/yazi-rs/plugins/tree/main/piper.yazi) - Pipe any shell command as a previewer.
- [mux.yazi](https://github.com/peterfication/mux.yazi) - Plugin multiplexer. Define and cycle through previewers for the same file.

Media:

- [exifaudio.yazi](https://github.com/Sonico98/exifaudio.yazi) - Preview audio metadata and cover using [exiftool](https://exiftool.org/).
- [mediainfo.yazi](https://github.com/boydaihungst/mediainfo.yazi) - Preview image, audio, video, subtitle and many media files using `ffmpeg` and `mediainfo`.

Archives:

- [ouch.yazi](https://github.com/ndtoan96/ouch.yazi) - An [ouch](https://github.com/ouch-org/ouch) plugin for Yazi, supporting preview and compression.
- [zless-preview.yazi](https://github.com/vmikk/zless-preview.yazi) - Preview compressed text files using `zless`.
- [comicthumb.yazi](https://github.com/navysky12/comicthumb.yazi) - Preview for comicbook archive files using p7zip on Linux.

Binaries:

- [exiftool.yazi](https://github.com/AleMenon/exiftool.yazi) - Preview metadata from executable files using `exiftool`.

Documents:

- [djvu-view.yazi](https://github.com/Shallow-Seek/djvu-view.yazi) - Preview Djvu using `ddjvu` from [djvulibre](https://github.com/DjvuNet/DjVuLibre)

Data Files:

- [duckdb.yazi](https://github.com/wylie102/duckdb.yazi) - Preview CSV/TSV, JSON, and Parquet files using [duckdb](https://github.com/duckdb/duckdb). View the raw data, or a summarized view with data-types, min, max, avg etc. for all columns.

BitTorrent:

- [torrent-preview.yazi](https://github.com/kirasok/torrent-preview.yazi) - Preview "\*.torrent" files using [transmission-cli](https://github.com/transmission/transmission).

Jupyter notebooks:

- [nbpreview.yazi](https://github.com/AnirudhG07/nbpreview.yazi) - Preview jupyter notebooks(\*.ipynb) files using [nbpreview](https://github.com/paw-lu/nbpreview).

Misc:

- [rich-preview.yazi](https://github.com/AnirudhG07/rich-preview.yazi) - Preview Markdown, JSON, CSV, etc. using [rich-cli](https://github.com/textualize/rich-cli)

### 🧩 Functional plugins {#functional}

Jumping:

- [relative-motions.yazi](https://github.com/dedukun/relative-motions.yazi) - A Yazi plugin based about vim motions.
- [jump-to-char.yazi](https://github.com/yazi-rs/plugins/tree/main/jump-to-char.yazi) - Vim-like `f<char>`, jump to the next file whose name starts with `<char>`.
- [percent-jump.yazi](https://github.com/ownself/percent-jump.yazi) - Percent-based navigation for the file list - jump to any position by entering a percentage (0-100).
- [time-travel.yazi](https://github.com/iynaix/time-travel.yazi) - Browse forwards and backwards in time via BTRFS / ZFS snapshots.
- [cdhist.yazi](https://github.com/bulletmark/cdhist.yazi) - Use cdhist to fuzzy select and navigate within Yazi from your directory history.
- [cd-git-root.yazi](https://github.com/ciarandg/cd-git-root.yazi) - Changes directory to the root of the git repository you are currently in.
- [fazif.yazi](https://github.com/Shallow-Seek/fazif.yazi) - Search over selected item with `fd`, `rg` `rga` and spawn any FZF configurations in Yazi.
- [yafg.yazi](https://github.com/XYenon/yafg.yazi) - Fuzzy find and grep in Yazi with ripgrep and fzf, opening selected matches in your editor at the matched line.

Bookmarks:

- [bookmarks.yazi](https://github.com/dedukun/bookmarks.yazi) - A Yazi plugin that adds the basic functionality of Vi-like marks.
- [mactag.yazi](https://github.com/yazi-rs/plugins/tree/main/mactag.yazi) - Bring macOS's awesome tagging feature to Yazi! The plugin is only available for macOS just like the name says.
- [simple-tag.yazi](https://github.com/boydaihungst/simple-tag.yazi) - Tagging feature for Linux, macOS and Windows!
- [yamb.yazi](https://github.com/h-hg/yamb.yazi) - Yet another bookmarks plugins. It supports persistence, jumping by a key, jumping by [fzf](https://github.com/junegunn/fzf).
- [bunny.yazi](https://github.com/stelcodes/bunny.yazi) - Bookmarks menu with both persistent and ephemeral bookmarks, fuzzy searching, going back to previous directory, and changing to a directory open in another tab.
- [whoosh.yazi](https://gitlab.com/WhoSowSee/whoosh.yazi) - Advanced bookmark manager with persistent/temporary bookmarks, directory history, fzf integration, path truncation, and cross-platform support. Jump between locations instantly with keys or fuzzy search.

Tabs:

- [projects.yazi](https://github.com/MasouShizuka/projects.yazi) - Save all tabs and their states as a project, and restore them at any time.
- [close-and-restore-tab.yazi](https://github.com/MasouShizuka/close-and-restore-tab.yazi) - Restore closed tabs.
- [autosession.yazi](https://github.com/barbanevosa/autosession.yazi) - Automatic session persistence that saves the current state on exit and restores the last saved state on startup.

File actions:

- [chmod.yazi](https://github.com/yazi-rs/plugins/tree/main/chmod.yazi) - Execute `chmod` on the selected files to change their mode.
- [diff.yazi](https://github.com/yazi-rs/plugins/tree/main/diff.yazi) - Diff the selected file with the hovered file, create a living patch, and copy it to the clipboard.
- [compress.yazi](https://github.com/KKV9/compress.yazi) - A Yazi plugin that compresses selected files to an archive.
- [lin-decompress.yazi](https://github.com/ZimCodes/lin-decompress.yazi) - **(Linux-only)** Extract each archive using a specified tool
- [ouch.yazi](https://github.com/ndtoan96/ouch.yazi) - An [ouch](https://github.com/ouch-org/ouch) plugin for Yazi, supporting preview and compression.
- [archivemount.yazi](https://github.com/AnirudhG07/archivemount.yazi) - Mounting and unmounting archives in yazi using [archivemount](https://github.com/cybernoid/archivemount).
- [reflink.yazi](https://github.com/Ape/reflink.yazi) - Create reflinks to files.
- [rsync.yazi](https://github.com/GianniBYoung/rsync.yazi) - Simple rsync copying locally and to remote servers.
- [sshfs.yazi](https://github.com/uhs-robert/sshfs.yazi) - Mount and manage remote directories over SSH using SSHFS. Supports hosts from `~/.ssh/config` or custom-defined connections. Includes key/password auth.
- [what-size.yazi](https://github.com/pirafrank/what-size.yazi) - Calculate total size of current selection or of current working directory.
- [lazygit.yazi](https://github.com/Lil-Dank/lazygit.yazi) - Manage Git directories with [lazygit](https://github.com/jesseduffield/lazygit) with a quick shortcut.
- [open-git-remote.yazi](https://github.com/larry-oates/open-git-remote.yazi) - Shortcut to open a git remote's webpage for the current yazi directory
- [sudo.yazi](https://github.com/TD-Sky/sudo.yazi) - Execute specific file operations with `sudo` privileges.
- [restore.yazi](https://github.com/boydaihungst/restore.yazi) - Restore/recover latest deleted files/folders using `trash-cli`.
- [recycle-bin.yazi](https://github.com/uhs-robert/recycle-bin.yazi) - Manage your Trash from Yazi: browse contents, restore or delete selected items, empty by age, or empty completely using `trash-cli`.
- [omni-trash.yazi](https://github.com/goon/omni-trash.yazi) - Manage your trash across all drives in a single unified interface using `trash-cli` to delete and restore selected items or empty every trash directory at once.
- [gvfs.yazi](https://github.com/boydaihungst/gvfs.yazi) - Mount and manage MTP, GPhoto2 (PTP) devices (Android, Cameras, etc), SMB, SFTP, NFS, FTP, Google Drive, DNS-SD, DAV (WebDAV), AFP, AFC (Linux only). List of [supported protocals](<https://wiki.gnome.org/Projects(2f)gvfs(2f)schemes.html>).
- [kdeconnect-send.yazi](https://github.com/Deepak22903/kdeconnect-send.yazi) - Send selected files to your smartphone or other devices using KDE Connect.
- [zoom.yazi](https://github.com/yazi-rs/plugins/tree/main/zoom.yazi) - Zoom in or out of the preview image.
- [pandoc.yazi](https://github.com/lmnek/pandoc.yazi) - Convert markup files to different formats via Pandoc.

Clipboard:

- [clipboard.yazi](https://github.com/XYenon/clipboard.yazi) - Copy and paste files via the system clipboard, with cross-platform support.
- [copy-file-contents.yazi](https://github.com/AnirudhG07/plugins-yazi/tree/main/copy-file-contents.yazi) - A simple plugin to copy file contents just from Yazi without going into editor.
- [system-clipboard.yazi](https://github.com/orhnk/system-clipboard.yazi) - Cross platform implementation of a simple system clipboard.
- [wl-clipboard.yazi](https://github.com/grappas/wl-clipboard.yazi) - Wayland implementation of a simple system clipboard.
- [path-from-root.yazi](https://github.com/aresler/path-from-root.yazi) - Copy file path relative to git root
- [clippy.yazi](https://github.com/gallardo994/clippy.yazi) - Copy files to clipboard with Clippy on macOS
- [relative-path.yazi](https://github.com/qwjyh/relative-path.yazi) - Copy file path relative to current working directory.

`filter` enhancements:

- [smart-filter.yazi](https://github.com/yazi-rs/plugins/tree/main/smart-filter.yazi) - Makes filters smarter: continuous filtering, automatically enter unique directory, open file on submitting.

`enter` enhancements:

- [smart-enter.yazi](https://github.com/yazi-rs/plugins/tree/main/smart-enter.yazi) - `Open` files or `enter` directories all in one key!
- [bypass.yazi](https://github.com/Rolv-Apneseth/bypass.yazi) - Yazi plugin for skipping directories with only a single sub-directory.
- [fast-enter.yazi](https://github.com/ourongxing/fast-enter.yazi) - Auto-decompress archives and enter them, or enter the deepest directory until it's not the only subdirectory.
- [wise-enter.yazi](https://github.com/jaam8/wise-enter.yazi) - Enter the deepest subfolder, extract archives, open files - all in one key.

`shell` enhancements:

- [open-with-cmd.yazi](https://github.com/Ape/open-with-cmd.yazi) - Open files using a prompted command.

`search` enhancements:

- [vcs-files.yazi](https://github.com/yazi-rs/plugins/tree/main/vcs-files.yazi) - Show Git file changes.
- [git-files.yazi](https://github.com/ktunprasert/git-files.yazi) - Show Git file changes (with untracked, via `git status --porcelain`)
- [modif.yazi](https://github.com/Shallow-Seek/modif.yazi) - Show recently modified.

`paste` enhancements:

- [smart-paste.yazi](https://github.com/yazi-rs/plugins/tree/main/smart-paste.yazi) - Paste files into the hovered directory or to the CWD if hovering over a file.

General action enhancements:

- [augment-command.yazi](https://github.com/hankertrix/augment-command.yazi) - Enhances a few Yazi actions with better handling of the choice between selected items and the hovered item.

UI enhancements:

- [full-border.yazi](https://github.com/yazi-rs/plugins/tree/main/full-border.yazi) - Add a full border to Yazi to make it look fancier.
- [toggle-pane.yazi](https://github.com/yazi-rs/plugins/tree/main/toggle-pane.yazi) - Toggle the show, hide, and maximize states for different panes: parent, current, and preview.
- [git.yazi](https://github.com/yazi-rs/plugins/tree/main/git.yazi) - Show the status of Git file changes as linemode in the file list.
- [mount.yazi](https://github.com/yazi-rs/plugins/tree/main/mount.yazi) - A mount manager for Yazi, providing disk mount, unmount, and eject functionality.
- [starship.yazi](https://github.com/Rolv-Apneseth/starship.yazi) - Starship prompt plugin for Yazi.
- [omp.yazi](https://github.com/saumyajyoti/omp.yazi) - oh-my-posh prompt plugin for Yazi.
- [yatline.yazi](https://github.com/imsi32/yatline.yazi) - Customize header-line and status-line with an easy configuration.
- [simple-status.yazi](https://github.com/Ape/simple-status.yazi) - Minimalistic status line with useful file attribute information.
- [no-status.yazi](https://github.com/yazi-rs/plugins/tree/main/no-status.yazi) - Remove the status bar.
- [pref-by-location.yazi](https://github.com/boydaihungst/pref-by-location.yazi) - Save and restore linemode/sorting/hidden preferences based on directory location.
- [linemode-plus.yazi](https://github.com/barbanevosa/linemode-plus.yazi) - Advanced linemode customization with configurable date format and combined size+mtime view.

### 🚀 Preloaders {#preloaders}

Images:

- [allmytoes.yazi](https://github.com/Sonico98/allmytoes.yazi) - Preview freedesktop-compatible thumbnails using [allmytoes](https://gitlab.com/allmytoes/allmytoes).

### 🔍Fetchers {#fetchers}

Mime-type:

- [`mime-ext.yazi`](https://github.com/yazi-rs/plugins/tree/main/mime-ext.yazi) - A mime-type provider based on a file extension database, replacing the builtin `file(1)` to speed up mime-type retrieval at the expense of accuracy.

### 🧑‍💻 Devtools {#devtools}

[types.yazi](https://github.com/yazi-rs/plugins/tree/main/types.yazi) - Type definitions for Yazi's Lua API, empowering an efficient plugin development experience.

### 📝 (Neo)vim plugins {#vim}

Neovim:

- [yazi.nvim](https://github.com/mikavilpas/yazi.nvim) - A Neovim plugin for the yazi terminal file manager.
- [tfm.nvim](https://github.com/Rolv-Apneseth/tfm.nvim) - Neovim plugin for terminal file manager integration.
- [fm-nvim](https://github.com/Eric-Song-Nop/fm-nvim) - Neovim plugin that lets you use your favorite terminal file managers.

Vim:

- [vim-yazi](https://github.com/yukimura1227/vim-yazi) - Vim plugin integrating Yazi for seamless in-editor file browsing and navigation.
- [yazi.vim](https://github.com/chriszarate/yazi.vim) - Vim plugin for Yazi.

### 📝 Helix {#helix}

- [Yazelix](https://github.com/luccahuguet/yazelix) - Adding a file tree to Helix & helix-friendly keybindings for Zellij

### 🐚 Shell plugins {#shell}

- [yazi-prompt.sh](https://github.com/Sonico98/yazi-prompt.sh) - Display an indicator in your prompt when running inside a yazi subshell.
- [custom-shell.yazi](https://github.com/AnirudhG07/custom-shell.yazi) - Run any commands through your default system shell.
- [command.yazi](https://github.com/KKV9/command.yazi) - Display a prompt for executing yazi actions.

### 🛠️ Utilities {#utilities}

- [icons-brew.yazi](https://github.com/lpnh/icons-brew.yazi) - Make a hot `theme.toml` for your Yazi icons with your favorite color palette.
- [lsColorsToToml](https://github.com/Mellbourn/lsColorsToToml) - Generate the color rules for the `[filetype]` section in `theme.toml` based on your `$LS_COLORS`.
- [osc7.yazi](https://github.com/coder0x6675/osc7.yazi) - Synchronize the terminal's working directory to Yazi.

### 💖 Add yours {#add-yours}

We are so happy to add your plugin to this page!

If your plugin meets the following requirements, please click "Edit this page" below to add it:

- **Functional** - we will install and test to make sure all links included on this page are valid. If it's available only on a specific platform, a note should be added in the README.
- **Follow conventions** - it should be a directory/repository ending with `.yazi`, and include the files listed in the [plugin documentation](/docs/plugins/overview).
- **i18n** - the README should be in English, or at least include an English README if there are multiple languages available.

If it's a Neovim or shell plugin, appending `.nvim` or `.sh` to the name to make it distinguishable is a best practice, but it's not required.

---

## Terminology

Yazi is developed following domain-driven design principles, and by incorporating domain-specific terminology, it reduces communication costs and ensures that we are aligned with it.

### Layers

Yazi adopts a layered architectural design, with each layer having clear responsibilities and functions:

- `app`: Entire application. This layer is not directly accessed by users but mediates interactions between the user and the terminal or system environment, such as listening for and handling mouse or key events, processing system signals, redrawing interfaces, etc.
- `mgr`: Main user interface of the manager, where most user actions take place, such as browsing, selecting, opening, and editing files.
- `tasks`: Task manager, responsible for managing asynchronous shell processes, plugins, preloading, and file operations (copying, moving, deleting, etc.).
- `spot`: File information spotter, which uses user-configured spotters to display metadata for different file types, such as dimensions and color space for image files, duration and encoding for video files, total size of directories, etc.
- `pick`: Picker component used to choose a method for opening files.
- `input`: Input component used to receive user input, such as plain text or password entries.
- `confirm`: Confirmation component used to prompt the user for confirmations, such as deleting or overwriting files.
- `cmp`: Auto-completion component used to provide suggestions for file names, paths, etc.
- `help`: Help menu used to display the list of available key bindings for different layers along with their descriptions.

### File System

- `url`: Uniform resource locator of a file.
- `cha`: Metadata of a file.

### Layout System

- `rect`: A rectangular area.
- `area`: Parameters for an area with a rect type.
- `pad`: Padding.
- `pos`: Relative position of a layout element.
- `constraint`: Layout constraints that define the size of a layout element.

### Plugin System

- fetcher: A Lua plugin used for preloading metadata of multiple files in bulk.
- spotter: A Lua plugin used to spot the metadata of a single file.
- preloader: A Lua plugin used to preload the content of a single file.
- previewer: A Lua plugin used to preview the content of a single file.

### Lua API

- `cx`: Synchronous context state.
- `rt`: Runtime information, such as user terminal emulator properties and global user preferences.
- `th`: Theme system configuration.
- `fs`: File system API.
- `ui`: Layout system.
- `ya`: Utility API, including functions for system time, debugging, shell commands, etc.
- `ps`: Publish-subscribe system/data distribution service.

### Data Distribution Service

- `DDS`: Data Distribution Service.
- `instance`: A Yazi process.
- `local`: Current instance.
- `remote`: Instances that are not the current one.
- `message`: Smallest unit of one-shot communication between different instances.
- `static message`: Messages that begin with `@`, whose state is automatically persisted and restored when a new instance starts.

---

## Frequently Asked Questions

### Why is Yazi fast? {#why-yazi-fast}

See [Why is Yazi fast?](/blog/why-is-yazi-fast).

### Why can't I edit text files? {#why-cant-edit}

Yazi defaults to using `$EDITOR` as the text editor for Linux/macOS.
If you are unable to edit files, please check your Bash/Zsh/Fish configuration file for settings like `export EDITOR=vim`. You can also [change Yazi's text opener](/docs/configuration/yazi#opener) from `$EDITOR` to vim/nvim/nano, etc.

For Windows, there is no concept of `$EDITOR`, so users need to modify the text opener as needed.

### Why can't I open/edit/preview files? {#why-cant-preview}

Yazi relies on `file(1)` to obtain the file mimetype to run the corresponding opener and previewer rules, please check whether your system has it pre-installed.

For Windows, please make sure you have set the `YAZI_FILE_ONE` environment variable as per the [Windows Requirements](/docs/installation#windows).

### Why are the icons not displayed properly? {#icons-incorrect-display}

If your terminal doesn't have Nerd Font support built in, it will render the icons as placeholder characters like squares or question marks, in that case you'll need to manually set your terminal up:

1. Download a Nerd Font from https://www.nerdfonts.com/font-downloads
   - If your terminal lets you specify a fallback font in addition to the main font, download the `Symbols Nerd Font` and set that as the fallback.
   - If your terminal only lets you use a single font, choose any patched Nerd Font you like, e.g. `JetBrainsMono Nerd Font`, and set your terminal font to that.
2. Restart your terminal.

### Why is my text color not distinct? {#why-text-indistinct}

Yazi's default theme uses base16 colors to match the user's terminal theme as closely as possible.

Unfortunately, this cannot cater to all users, and even the colors needed by the same user in light/dark mode can vary, not to mention that some terminals have poor default color schemes, like this [#149 (comment)](https://github.com/sxyazi/yazi/issues/149#issuecomment-1798349727).

So, please [use a Yazi flavor](https://github.com/yazi-rs/flavors) that matches your terminal theme. Of course, if you find a color that better covers most terminals, feel free to create a PR!

### Why can't "Open" and "Enter" be a single action? {#why-separate-open-enter}

The decision to separate `enter` and `open` actions was intentional.

In the future, Yazi will support "archives as directories", allowing direct operations on the files inside.

An archive is a file, so it's "openable", but it's also "enterable" as a directory, allowing users to choose the action they want to take.

This is also true for an actual directory: it can be entered in Yazi or opened in programs like VS Code or desktop file managers.

If you truly don't need to distinguish between them, use this [smart-enter tip](/docs/tips#smart-enter).

### Why do my icons shrink in [kitty](https://sw.kovidgoyal.net/kitty/), and enlarge when scrolling? {#why-icons-shrink}

TL;DR: Use a flavor for Yazi, https://github.com/yazi-rs/flavors

This might be a bug in kitty (or feature? I don't know). In kitty, you have to add a style to file list items (such as a foreground color) to make the icons match the text size. However, Yazi's default theme can't add that color, because it can't predict whether the user's terminal has a white background with black text or a black background with white text.

So it inherits the default terminal font color. This causes the icon size issue, and this problem has only been observed in kitty. Therefore, please use a Yazi flavor with kitty.

### How to troubleshoot terminal response timeout errors? {#trt}

Yazi sends [`DA1`](https://vt100.net/docs/vt510-rm/DA1.html) and [`DSR`](https://vt100.net/docs/vt510-rm/DSR.html)-based requests at startup to detect and enable some modern terminal features. This error means the terminal didn't respond within the timeout, which can happen because:

1. Your terminal is having performance issues and can't reply fast enough. You may check if it happens on other terminals to rule out a terminal-specific problem.
2. You're using an older version of `st` that doesn't support DSR. Make sure your `st` or its fork has incorporated [this fix](https://git.suckless.org/st/commit/f17abd25b376c292f783062ecf821453eaa9cc4c.html).
3. You're on a high-latency / slow SSH connection and the request timed out.

If you don't see any weird behavior besides this error being printed, just ignore it.

If you use tmux: tmux tends to interfere with communication between CLI apps and the terminal, to avoid the interference, Yazi has to implement a bunch of hacks, most of which work fine in most cases, if it doesn't work for you, please check:

1. Is your tmux up-to-date?
2. Have you [enabled passthrough for tmux](/docs/image-preview#tmux)?
3. Have you bound `M-[` to tmux? `Alt+[` is `ESC [` which is the [CSI introducer](https://en.wikipedia.org/wiki/ANSI_escape_code#Control_Sequence_Introducer_commands), tmux might interpret terminal responses that include it as key events.
4. Comment out all custom configurations _except_ [passthrough](/docs/image-preview#tmux) to see if your settings are causing the issue. If so, add them back piece by piece to find the culprit.

### Why is "orphan" set to false by default? {#why-orphan-false}

`orphan=true` is an emergency exit; once specified, your task will not be managed by Yazi.

For instance, if you realize that you've used `unzip` on the wrong files, and you need to cancel it, with `orphan=false`, you can easily do that by pressing `x` in Yazi's task manager.
However, with `orphan=true`, you can only return to the shell to terminate it.

On the other hand, tasks with `orphan=false` are scheduled through the Yazi task system. It can limit the number of concurrent tasks (configurable by the user), to prevent system resource depletion, such as when you're extracting 100 files.

### I don't like nerd‐fonts! {#dont-like-nerd-fonts}

Yazi has `nerd-fonts` icons enabled by default, it looks really cool!

If you don't want to use it and want things to be calm, sure, you can modify these icons as much as you want in [`theme.toml`](/docs/configuration/theme):

```toml
[status]
sep_left = { open = "", close = "" }
sep_right = { open = "", close = "" }

[icon]
globs = []
dirs  = []
files = []
exts  = []
conds = []
```

The code above hides all icons, and the entire world goes quiet. Nice!

---
