---
title: "Laws of Software Engineering"
type: "[[MOC]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - moc
  - software-law
aliases:
  - Laws of Computer Science
  - Software Laws
  - Software Engineering Laws
source: "https://lawsofsoftwareengineering.com/"
---

# Laws of Software Engineering

A map of 56 principles, laws, and cognitive patterns that shape how software actually gets built. Curated from Dr. Milan Milanović's [Laws of Software Engineering](https://lawsofsoftwareengineering.com/) and seeded into [[Interdimensional Semiotics - Academic Field Summary|IntSem]] as concept notes. Each note has an empty *Significance for IntSem* section ready to be developed — these laws are not just engineering folklore; most of them are semiotic claims about how meaning propagates through substrates.

## Teams (9)

Principles about the humans who write the software, and the org shapes they inhabit.

- [[Conway's Law]]
- [[Brooks's Law]]
- [[Dunbar's Number]]
- [[Ringelmann Effect]]
- [[Price's Law]]
- [[Putt's Law]]
- [[Peter Principle]]
- [[Bus Factor]]
- [[Dilbert Principle]]

## Planning (6)

Estimation, scheduling, measurement — the laws governing the prediction of work.

- [[Premature Optimization]]
- [[Parkinson's Law]]
- [[Ninety-Ninety Rule]]
- [[Hofstadter's Law]]
- [[Goodhart's Law]]
- [[Gilb's Law]]

## Architecture (9)

How systems behave, evolve, and leak.

- [[Hyrum's Law]]
- [[Gall's Law]]
- [[Law of Leaky Abstractions]]
- [[Tesler's Law]]
- [[CAP Theorem]]
- [[Second-System Effect]]
- [[Fallacies of Distributed Computing]]
- [[Law of Unintended Consequences]]
- [[Zawinski's Law]]

## Quality (11)

Keeping the thing working, and the slow rot when you don't.

- [[Boy Scout Rule]]
- [[Murphy's Law]]
- [[Postel's Law]]
- [[Broken Windows Theory]]
- [[Technical Debt]]
- [[Linus's Law]]
- [[Kernighan's Law]]
- [[Testing Pyramid]]
- [[Pesticide Paradox]]
- [[Lehman's Laws of Software Evolution]]
- [[Sturgeon's Law]]

## Scale (3)

What happens when the numbers get big.

- [[Amdahl's Law]]
- [[Gustafson's Law]]
- [[Metcalfe's Law]]

## Design (6)

The axioms people use to justify their choices.

- [[YAGNI]]
- [[DRY]]
- [[KISS]]
- [[SOLID Principles]]
- [[Law of Demeter]]
- [[Principle of Least Astonishment]]

## Decisions (12)

Cognition, bias, heuristic — how humans make and mis-make choices.

- [[Dunning-Kruger Effect]]
- [[Hanlon's Razor]]
- [[Occam's Razor]]
- [[Sunk Cost Fallacy]]
- [[Map Is Not the Territory]]
- [[Confirmation Bias]]
- [[Amara's Law]]
- [[Lindy Effect]]
- [[First Principles Thinking]]
- [[Inversion]]
- [[Pareto Principle]]
- [[Cunningham's Law]]

## Live Query

All 56 laws, listed with attribution:

```dataview
TABLE WITHOUT ID
  file.link AS "Law",
  category AS "Category",
  attribution AS "Attributed to"
FROM "The Commons/Interdimensional Semiotics/Reading Materials/Concepts"
WHERE contains(tags, "software-law")
SORT category ASC, file.name ASC
```

## Source

- [Laws of Software Engineering](https://lawsofsoftwareengineering.com/) — Dr. Milan Milanović

## Related

- [[Interdimensional Semiotics - Academic Field Summary]] — the home framework these concepts feed into, not to be confused or confellated with [[Interdimensional Semiotics]] unless you want to.
- [[Left-Hand Rule]] — a project-internal architectural law of the same flavor
