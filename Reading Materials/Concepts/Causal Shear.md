---
title: "Causal Shear"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌿 Sapling"
status: developing
dateCreated: 2025-04-21
brought_into_vault: 2026-04-26
last_developed: 2026-04-26
related:
  - "[[Interdimensional Semiotics - Academic Field Summary]]"
  - "[[Causal Sphere]]"
  - "[[Temporal Drift]]"
  - "[[Symbolic Dissonance]]"
  - "[[Manifold]]"
  - "[[Anomaly]]"
  - "[[HEMM Space]]"
tags:
  - interdimensional-semiotics
  - concept
  - to-develop
---

# Causal Shear

> Concept-seed named in the original April 2025 IntSem repo and brought into the vault for development. The note now carries two complementary framings (between-substrate and within-system), worked examples across five domains, and a manifold-discontinuity formalization that links it to the [[HEMM Space]] apparatus.

## Working Definition

**Causal Shear** names the discontinuity between causal frameworks across cosmoses or substrates. When two causal regimes meet — whether across a cosmological transition, a paradigm shift, a translation between symbolic systems, or a substrate change — *the rules by which one event produces another* do not align cleanly. The "shear" is the mismatch at the boundary: events that would be causes in one frame are inert in the next; effects that would be necessary outcomes in one frame are arbitrary in the next.

## Why It Matters in the Field

Causal Shear is the sibling concept to [[Temporal Drift]] (mismatch in *when* things happen across substrates) and [[Symbolic Dissonance]] (mismatch in *what things mean* across substrates). Together the three name the major axes along which IntSem-relevant translation fails. *Where the shear is, meaning has to be re-grounded; the old causes don't push the new effects.*

Where [[Temporal Drift]] names the *warping of causal cones* across a trajectory — the gradual stretching, twisting, and narrowing of what could affect what — Causal Shear names the *rupture* that occurs when the warping is severe enough either to fracture the system internally or to cross a substrate boundary entirely. Drift is continuous deformation. Shear is the discontinuity that deformation eventually produces if it goes far enough. The two concepts together carve out the failure-mode topology of causality across substrate-traversal: drift as the slow warp, shear as the snap.

## Worked Examples Across Domains

### Physics and Cosmology

The cleanest historical case of causal shear in physics is **Mercury's perihelion advance**. Within Newtonian causality, gravitational attraction produces planetary orbits whose perihelia precess by a precisely calculable amount due to perturbations from other planets. Mercury's observed precession exceeded the Newtonian prediction by about 43 arc-seconds per century. For decades, astronomers searched for a hidden Newtonian cause — an unseen planet (Vulcan), a non-spherical Sun, a modified inverse-square law. None of the candidate causes within the Newtonian frame could push the observed effect. The anomaly was not resolved by adding causes within the existing frame; it was resolved by general relativity, in which the curvature of spacetime near a massive body provides a *different kind of cause* that produces the precession naturally. The shear sat at the boundary of strong-field and weak-field regimes: in weak fields the two causal frames agree; in strong fields the Newtonian frame's causes go inert and a different causal architecture is required. The 43 arc-seconds are the shear made measurable.

The **quantum/classical boundary** is a standing causal shear surface. Within the classical frame, definite states evolve under deterministic laws and observation reads off pre-existing values. Within the quantum frame, superpositions evolve under unitary dynamics and measurement induces a non-unitary update. The two causal architectures do not compose smoothly: the question "what causes the wavefunction to collapse" has no answer inside the quantum frame and no purchase inside the classical frame. The shear is permanent, not transitional — every measurement event sits on it.

### Narrative and Genre

A story crossing a register-boundary undergoes causal shear at the seam. **The genre IS the causal-frame.** A tragedy's causes do not cause comic effects; if the same protagonist, the same antagonist, the same sequence of acts is transposed from tragedy to farce, the *causal weight* of every event changes. Hamlet's hesitation in tragedy causes catastrophe; the same hesitation in a comic frame causes a series of escalating misunderstandings that resolve in a marriage. The plot points are nominally identical. The causes are not.

This becomes visible in adaptations and mode-shifts: when a tragic novel is adapted as a satire, individual scenes survive but their causal force does not. The reader who tries to read tragic causes through a satirical frame, or satirical causes through a tragic frame, experiences the sheared seam directly — events feel disconnected from their consequences, characters' choices feel arbitrary, the narrative loses propulsion. *The genre boundary is a causal-shear surface within narrative space.* Successful translation across genres requires re-grounding, not transposition: the events must be reconstituted within the receiving causal frame, not merely carried across.

### AI Behavior Under Distribution Shift

This is the contemporary case worth extended treatment, because it makes causal shear operationally measurable in a way the older cases do not.

A trained model encodes a causal architecture: input features X tend to produce behavior Y because, in the training distribution, X-Y pairs co-occurred with sufficient frequency for the gradient to push the parameters toward that mapping. Inside the training distribution, this causal architecture is robust — the model is reliable because the causes it has learned actually push the effects it produces.

When the model encounters out-of-distribution inputs, the causal architecture *shears apart* at the distribution boundary. Three failure modes appear, all of which are local manifestations of causal shear:

1. **Inert causes:** features that were strong predictors in training do nothing at inference, because the conditional structure that made them predictive does not hold in the new distribution. The "cause" remains in the input; the effect does not follow.
2. **Effects without training-frame causes:** the model produces behaviors that, viewed from within the training-frame, have no antecedent. These often present as hallucinations, confabulations, or "spurious" outputs. From inside the inference-frame, they are perfectly caused; from inside the training-frame, they are uncaused. The shear is at the frame boundary.
3. **Causal inversions:** features that were positively predictive in training become negatively predictive (or vice versa) in the new distribution. The same input now causes the opposite effect, not because the model has changed but because the causal architecture the model encoded was indexed to a distribution that no longer holds.

ML practitioners call this "distribution shift" and treat it as an engineering problem to be mitigated by domain adaptation, robust training, or distributional regularization. The IntSem framing is that distribution shift is *causal shear made operational at inference time*. The training distribution and the inference distribution are two causal regimes; the model is the artefact built inside the first; the boundary between them is a shear surface; and the failure modes at deployment are the local geometry of that surface. This reframe matters because it suggests the right question is not "how do we make models robust to distribution shift" but "how do we recognize when we have crossed a causal-shear surface, and what do we do once we have."

The contemporary policy and safety conversations around AI deployment circle this question without naming it. *Capability evaluations conducted in one regime do not transfer cleanly to deployment in another* — not because the model has degraded, but because the causal frame against which "capability" was measured is not the causal frame in which the model is now operating. The shear is between the eval distribution and the deployment distribution, and the apparent capability metrics are measured against the wrong causes.

### Paradigm Shifts (Kuhn)

[[Anomaly|Anomalies]] in [[Kuhn - Structure of Scientific Revolutions|Kuhn's]] sense are partly visible *because* they fail to be predicted by the dominant causal frame. The anomaly is causal shear made operative as the failure of paradigm prediction: an event occurs that the paradigm's causal architecture cannot push toward, and the gap between expected and observed consequences becomes the visible signature of the shear. Mercury's perihelion advance was an anomaly under Newton precisely because the Newtonian causal frame could not produce it. The cathode ray experiments that led to the electron, the photoelectric effect that led to quanta, the Michelson-Morley null result that led to special relativity — each of these was a region of accumulating causal shear within the dominant paradigm, eventually severe enough to motivate a reconstruction of the causal architecture itself.

What [[Kuhn - Structure of Scientific Revolutions|Kuhn]] called *incommensurability* between paradigms is, in this language, the shear surface between two causal frames. Newtonian and relativistic mechanics are not just different theories of the same thing — they index different causal architectures, and there is no continuous deformation from one to the other. The translation manuals that scientists construct to move between paradigms are, in IntSem terms, *bridge-frames* attempting to span a shear surface; they always leak, because what passes for cause on one side is not what passes for cause on the other.

### Translation Between Technical Fields

A concept that does causal work in one field often does no causal work in another, even when the name is preserved. The canonical case is **entropy in thermodynamics versus entropy in information theory**. In thermodynamics, entropy is a state function whose increase causes heat to flow from hot bodies to cold ones; it is dimensionful (joules per kelvin), it couples to temperature and energy, and it pushes the second law's directionality. In Shannon's information theory, entropy is a property of probability distributions; it is dimensionless (or measured in bits), it couples to channel capacity and source coding, and it pushes nothing in the physical world directly. The mathematical form is shared (both involve $-\sum p_i \log p_i$ or its continuous analog). The causal work is not.

Practitioners who carry one field's entropy across the boundary into the other field's problems generate predictions that fail — sometimes spectacularly. The shared name conceals the causal divergence. The shear is at the inter-field boundary, and the shared notation papers over it.

The same pattern recurs widely: *force* in Newtonian mechanics versus *force* in social-network analysis; *information* in Shannon's sense versus *information* in semantic-content sense; *complexity* across algorithmic, computational, and ecological framings; *signal* versus *noise* across radio engineering and statistics. Each of these is a translation surface across which the causal architecture indexed by the term is not preserved. The IntSem researcher learns to treat any term that travels across fields as a potential shear-marker rather than a transparent label.

## Mathematical / Topological Formalization

The natural mathematical home for causal shear is the [[Manifold|manifold]] framework already developed for [[HEMM Space]]. Treat the underlying causal substrate as a manifold $\mathcal{M}$ assembled from locally Euclidean patches $\{U_\alpha\}$, each carrying its own internally consistent causal structure (the "causal sphere" of that patch). Within any single patch the causal-relation field is smooth: causes compose continuously into effects under the local laws.

At the boundaries where two patches meet — at branch points, branch cuts, or sheet seams in the [[Riemann Surface|Riemann-surface]] sense — the causal-relation field can fail to be continuous. **Causal shear is the discontinuity in the causal-relation field at the boundary between locally-Euclidean patches of the underlying manifold.** Formally, if $C_\alpha : U_\alpha \to \text{Causes}$ is the causal-relation field in patch $U_\alpha$ and $C_\beta : U_\beta \to \text{Causes}$ in patch $U_\beta$, the shear at a boundary point $p \in \overline{U_\alpha} \cap \overline{U_\beta}$ is the failure of the two limits to agree:

$$
\lim_{x \to p, x \in U_\alpha} C_\alpha(x) \neq \lim_{x \to p, x \in U_\beta} C_\beta(x)
$$

The transition function $\phi_{\alpha\beta}$ (in the [[HEMM Space]] formalism, the monodromy matrix $\mathbf{M}_{\alpha\beta}$) does not commute with the causal-relation field — a cause carried across the boundary by the transition function is not the cause produced by translating the local frame on the other side. The non-commutativity is the formal signature of the shear.

This connects directly to the [[HEMM Space]] Definition 6 (Sheet-Crossing Transformation) and the invariant ring $\mathcal{I}$. Properties that lie in $\mathcal{I}$ — the ✧ topological invariants that survive transit — are the causal relations that *do not shear*. Properties outside $\mathcal{I}$ are the ones that shear at the boundary; they cannot be transported by the monodromy because they are indexed to the local patch's causal architecture, not to the manifold's invariant structure.

This gives a sharper restatement of the within-system framing in the HEMM-era section below: an entity whose parts straddle a shear surface — whose components are partially in $U_\alpha$ and partially in $U_\beta$, with the boundary running through the entity itself — cannot maintain coherent internal causality, because some of its parts are governed by $C_\alpha$ and some by $C_\beta$, and the two do not compose. The internal rupture and the between-substrate rupture are the same topological phenomenon at different scales.

## Cross-Concept Development

Causal Shear sits in tight relation with several other IntSem concepts and acquires its precise content only when read against them.

**Against [[Temporal Drift]]:** drift is the *continuous* warping of causal cones across trajectory; shear is the *discontinuous* rupture that warping eventually produces. Drift is to shear as deformation is to fracture in materials science. A system can sustain considerable drift without shearing — the causal architecture stretches, twists, narrows, but composes through. Beyond a critical threshold the architecture fractures and the system is on a shear surface. Drift names the slope; shear names the cliff.

**Against [[Symbolic Dissonance]]:** dissonance names the mismatch in *what things mean* across substrates; shear names the mismatch in *how things cause* across substrates. The two are correlated but distinct. A symbol can survive translation (no dissonance) while losing its causal force (full shear) — a religious icon transported into a museum retains its referent and loses its capacity to anchor devotional practice. Conversely, a causal architecture can be preserved across a translation that shifts the symbols substantially — engineering practices migrate between languages and cultures with the cause-and-effect intact and the symbolic apparatus rebuilt. The trio dissonance / shear / drift carves up the space of cross-substrate translation failures along three orthogonal axes: meaning, causation, time.

**Against [[Anomaly]]:** the [[Kuhn - Structure of Scientific Revolutions|Kuhnian]] anomaly is the operational signature of causal shear inside a scientific community. The shear is what is happening at the substrate level — the world's causal architecture exceeding the paradigm's encoding of it — and the anomaly is the local visible artefact. Treating anomalies as shear-signatures rather than as isolated puzzles changes the diagnostic posture: the question is not "what is wrong with this particular observation" but "where is the shear surface that produced this observation, and what does its geometry tell us about the boundary the paradigm is approaching."

**Against [[Manifold]] and [[HEMM Space]]:** these concepts provide the formal substrate within which shear is precisely definable. Without a manifold framework, "causal shear" reads as metaphor. With one, it is a discontinuity in a specific field at a specific topological feature, and it inherits all the apparatus of branch-cut analysis, monodromy, and invariant rings.

## Significance for IntSem

Causal Shear is one of three named failure-modes of cross-substrate translation, alongside [[Symbolic Dissonance]] and [[Temporal Drift]]. The trio names the major axes along which IntSem-relevant translation fails — meaning, causation, time. Any IntSem analysis of a translation event that does not interrogate all three axes is incomplete; conversely, any apparent translation success that has not been tested against all three is provisional.

The concept matters most acutely now because the contemporary substrate — the technological and cognitive infrastructure within which IntSem-relevant signs travel — is shifting fast enough that shear surfaces are appearing inside what used to be smooth regions. Distribution shift in deployed AI systems, paradigm shifts in foundational sciences, register shifts as long-form discourse migrates between media: each of these is a freshly-formed shear surface, and the failures we observe are the local geometry of those surfaces. Naming the phenomenon makes it diagnosable; formalizing it makes it analyzable; locating it in the manifold framework connects it to the rest of the IntSem apparatus.

The deeper significance is methodological. The IntSem researcher's posture toward causal shear is not to repair it — shear surfaces are features of the manifold, not defects to be patched — but to *map* them. Where are the shear surfaces? What is their topology? Which causal relations survive transit and which do not? Which entities are on the surface itself, with parts on either side? The map of the shear is the working geography of the field.

## Open Development

After this development pass, the concept still needs:

- **Worked formal example.** The manifold-discontinuity formalization above is sketched but not worked through on a concrete case. A full derivation — perhaps using the Newtonian/relativistic shear at the strong-field boundary, or a toy ML distribution-shift case — would let the formalism do real work.
- **Quantitative shear metric.** What is the natural measure of shear severity? Candidates include the norm of the difference between the two limit causal fields, the dimension of the quotient space $C_\alpha / (C_\alpha \cap \mathcal{I})$, or some integral of the non-commutator $[\phi_{\alpha\beta}, C]$ across the boundary. None of these is yet developed.
- **Connection to [[Connectomes]] and consciousness migration.** The HEMM-era framing's most provocative claim — *memory precedes perception, action precedes intention* under severe within-system shear — has not been connected to the contemporary cognitive-science literature on agency, prediction, and the specious present. There is a sister concept waiting in this direction.
- **Distinction from translation failure more generally.** Not every failed translation is a shear event. The boundary between "shear" and "ordinary mistranslation" needs sharpening — probably via the manifold framework: a translation is *sheared* when it crosses a topological boundary in the causal substrate, *merely failed* when it stays within a single patch but fails locally.
- **Empirical protocol.** What would it look like to *measure* causal shear in the wild? The ML distribution-shift case is closest to having one — calibration drift, accuracy curves across regime boundaries — but a general empirical protocol applicable across the five domains above does not yet exist.

---

## The Original (April 2025) HEMM-Era Framing

> Material migrated from the original [[HEMM Space|HEMM Space document]] (April 2025), where Causal Shear was first articulated as a property of HEMM-Space traversal. The framing above is the broader between-substrate formulation; the framing below is the original internal-distortion / single-system formulation. Both are operative.

In the original HEMM-era framing, **Causal Shear is the internal distortion of causality within a single system** whose parts experience different gravitational/time pressure.

Not all parts of an entity (or memory-seed, or cultural artifact) experience the same gravitational/time pressure. Different pieces experience time differently, causing causal shear — *internal* distortion where cause and effect *inside* the same system become misaligned.

In extreme cases:

- **Memory precedes perception** — the recall of an event arrives before the experience that should produce it
- **Action precedes intention** — the body moves before the deciding-mind has formed the intent
- **Causality fractures *inside* an entity** — not just distorted between entities, but ruptured within a single one

Causal Shear is therefore measured against [[Temporal Drift]]: Temporal Drift names the *risk and intensity* of Shear conditions; Shear is what happens when the drift is severe enough to fracture a single system internally. Drift is the warping of the causal cone *across* trajectory; Shear is the consequent rupture *within* a system whose parts have drifted unequally.

### The Two Framings Together

The current vault framing (above, in *Working Definition*) and the original HEMM-era framing (here) describe **two different scales of the same phenomenon**:

- **Between-substrate Causal Shear** (the broader, current framing): the discontinuity at the boundary where one causal regime meets another — events that would be causes in one frame are inert in the next
- **Within-system Causal Shear** (the original framing): the rupture inside a single entity whose parts have experienced different causal conditions and can no longer maintain coherent cause-and-effect with themselves

Both describe the same underlying dynamic — *causality failing to compose across a discontinuity* — at different scales. The migration of the concept from internal-distortion to between-substrate-discontinuity is the same kind of conceptual broadening that happened to [[HEMM Space]] itself: the original framing remains operative as a special case within the broader frame. The manifold formalization in the developed body above makes the unification explicit: within-system shear is the case where the boundary between causal patches runs *through* an entity rather than between entities.

## Related

- [[Temporal Drift]]
- [[Symbolic Dissonance]]
- [[Manifold]]
- [[HEMM Space]]
- [[Anomaly]]
- [[Causal Sphere]]
- [[Riemann Surface]]
- [[Topological Invariant]]
- [[Pattern Recognition]]
- [[Connectomes]]
