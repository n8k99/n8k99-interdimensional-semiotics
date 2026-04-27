---
title: "Coordinated Attack Problem"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
tags:
  - interdimensional-semiotics
  - concept
aliases: []
---

The coordinated attack problem is the canonical impossibility result for achieving coordinated action under unreliable communication. Two generals, camped on opposite sides of a valley, must agree to attack simultaneously or not at all. Their only communication channel is a messenger who must cross the valley and may be captured. [[Halpern Moses - Knowledge and Common Knowledge in a Distributed Environment|Halpern and Moses]] prove in §4 and §7 that no finite exchange of messages can establish the common knowledge required for guaranteed coordination — each acknowledgment requires its own acknowledgment, generating an infinite regress. The first general sends "attack at dawn," but cannot act until receiving confirmation. The second general confirms but cannot act until knowing the confirmation arrived. No finite protocol terminates this chain. The problem is not about bandwidth or latency but about the logical structure of mutual knowledge under unreliable channels.

## Cross-Book Development

Halpern and Moses treat the coordinated attack as the motivating example for their central theorem: simultaneous coordinated action requires common knowledge, and common knowledge is unachievable in systems with unreliable communication. Their formal proof shows that in any run of any protocol where messages can be lost, no agent can distinguish a run where all messages arrived from one where the last message was lost — and therefore no agent can know that the other agent knows enough to act. The impossibility is absolute within the model. [[Dwork Lynch Stockmeyer - Consensus in the Presence of Partial Synchrony|Dwork, Lynch, and Stockmeyer's]] consensus protocols are, in effect, solutions to the generalized coordinated attack problem under relaxed assumptions. By introducing partial synchrony — the guarantee that communication will eventually become reliable, even if the moment of stabilization is unknown — they escape the impossibility. Their protocols do not achieve simultaneous action but achieve eventual agreement: all correct processes will eventually decide on the same value, even if they cannot pinpoint the exact moment of convergence. The DLS resilience bounds (t < n/3 for unauthenticated Byzantine, t < n/2 for authenticated) quantify exactly how many faulty participants the generalized attack can tolerate. [[Gilbert Lynch - Brewers Conjecture and the CAP Theorem|Gilbert and Lynch's]] CAP impossibility is a descendant of the coordinated attack: if a network partitions, the nodes on either side of the partition are the two generals, and no protocol can guarantee they maintain consistent state while both remaining available.

## Significance for Interdimensional Semiotics

The coordinated attack is the fundamental problem of coordinated semiotic action — can two agents in different dimensions, different substrates, different interpretive frameworks act on the same meaning simultaneously? The Halpern/Moses result says: no, not with certainty. But this impossibility does not paralyze the IS framework; it clarifies it. Approximate coordination — ε-common knowledge — suffices for practical semiotic purposes. Two readers of the same text do not need to arrive at identical interpretations at the same instant. They need only converge closely enough, with sufficient mutual confidence, to enable meaningful discourse. The Noosphere does not require the two generals to attack at dawn; it requires only that they both eventually understand that dawn is coming. InnateScript's `until` operator encodes this pragmatic stance directly. It does not demand that a condition hold with certainty at a fixed time — it specifies a temporal bound within which convergence is expected, acknowledging that coordination is time-bounded and approximate rather than instantaneous and perfect. Meaning persistence, the IS principle that meaning survives substrate transitions, is not a claim of simultaneous agreement but of eventual convergence — the semiotic equivalent of DLS consensus rather than Halpern/Moses common knowledge. The coordinated attack tells us what is impossible; the IS framework builds on what remains possible.

## In the IS Reading List

- Halpern/Moses §4: formal statement and proof of the coordinated attack impossibility
- Halpern/Moses §7: relationship between coordinated attack and simultaneous Byzantine agreement
- Halpern/Moses §11: ε-common knowledge as the practical escape from the impossibility
- DLS §3-4: consensus protocols as generalized solutions under partial synchrony
- Gilbert/Lynch §3: CAP impossibility as a consequence of the same underlying structure

## Related

- [[ε-Common Knowledge]]
- [[Common Knowledge]]
- [[Partition Tolerance]]
- [[Consensus]]
- [[Partial Synchrony]]
