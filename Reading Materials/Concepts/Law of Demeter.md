---
title: "Law of Demeter"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - concept
  - software-law
  - design
aliases: []
attribution: "Ian Holland, Northeastern University, 1987"
category: Design
source: "https://lawsofsoftwareengineering.com/"
---

# Law of Demeter

> A module should only talk to its immediate collaborators — don't talk to strangers.

**Attribution:** Ian Holland, Northeastern University, 1987
**Category:** Design

## Statement

Also: the Principle of Least Knowledge. Long chains like `a.b().c().d()` couple the caller to the internals of `b` and `c`. Demeter-compliant code has fewer coupling paths and therefore fewer unexpected break sites.

## Significance for Interdimensional Semiotics

> *How does this law function as a sign operating across substrates? Which [[HEMM Space]] layer does it inhabit — is it a property of the symbolic order, the material substrate, or the meaning-making process itself?*

## Cross-Domain Resonance

> *Where else does this pattern appear outside of software — in writing, music composition, biology, organizational dynamics, [[T.A.S.K.S.]] observation architecture?*

## Related Laws

- [[YAGNI]]
- [[DRY]]
- [[KISS]]
- [[SOLID Principles]]
- [[Principle of Least Astonishment]]

## Source

- [Laws of Software Engineering](https://lawsofsoftwareengineering.com/) — Dr. Milan Milanović
