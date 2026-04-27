---
title: "Knowledge and Common Knowledge in a Distributed Environment"
authors: ["Joseph Y. Halpern", "Yoram Moses"]
year: 1990
type: "[[reading-comment]]"
icon: "📄"
domain: "[[The Commons]]"
tags: [interdimensional-semiotics, epistemic-logic, distributed-systems, common-knowledge, impossibility-results]
source: "Journal of the ACM, Vol. 37, No. 3, July 1990, pp. 549-587"
pdf: "https://web.eecs.umich.edu/~manosk/assets/papers/p549-halpern.pdf"
arxiv: "https://arxiv.org/abs/cs/0006009"
---

# Knowledge and Common Knowledge in a Distributed Environment

**Joseph Y. Halpern** — IBM Almaden Research Center, San Jose, California
**Yoram Moses** — The Weizmann Institute of Science, Rehovot, Israel

---

## Abstract

Reasoning about knowledge seems to play a fundamental role in distributed systems. Indeed, such reasoning is a central part of the informal intuitive arguments used in the design of distributed protocols. Communication in a distributed system can be viewed as the act of transforming the system's state of knowledge. This paper presents a general framework for formalizing and reasoning about knowledge in distributed systems. It is shown that states of knowledge of groups of processors are useful concepts for the design and analysis of distributed protocols. In particular, *[[Distributed Knowledge|distributed knowledge]]* corresponds to knowledge that is "distributed" among the members of the group, while *[[Common Knowledge|common knowledge]]* corresponds to a fact being "publicly known." The relationship between common knowledge and a variety of desirable actions in a distributed system is illustrated. Furthermore, it is shown that, formally speaking, in practical systems common knowledge cannot be attained. A number of weaker variants of common knowledge that are attainable in many cases of interest are introduced and investigated.

---

## 1. Introduction

Distributed systems of computers are rapidly gaining popularity in a wide variety of applications. However, the distributed nature of control and information in such systems makes the design and analysis of distributed protocols and plans a complex task. Basic foundations, general techniques, and a clear methodology are needed to improve our understanding and ability to deal effectively with distributed systems.

Although the tasks that distributed systems are required to perform are normally stated in terms of the global behavior of the system, the actions that a processor performs can depend only on its local information. Since the design of a distributed protocol involves determining the behavior and interaction between individual processors in the system, designers frequently find it useful to reason intuitively about processors' "states of knowledge" at various points in the execution of a protocol.

Ironically, formal descriptions of distributed protocols, as well as actual proofs of their correctness or impossibility, have traditionally avoided any explicit mention of knowledge. The intuitive arguments about the state of knowledge of components of the system are customarily buried in combinatorial proofs that are unintuitive and hard to follow.

The basic thesis of this paper is that explicitly reasoning about the states of knowledge of the components of a distributed system provides a more general and uniform setting that offers insight into the basic structure and limitations of protocols in a given system.

---

## 2. The Muddy Children Puzzle

A classical example illustrating the subtleties of reasoning about knowledge in a group context. *n* children are playing; *k* of them get mud on their foreheads. Each can see others' foreheads but not their own. The father announces "At least one of you has mud on your head" — a fact already known to each individually (if k > 1). He then repeatedly asks "Can any of you prove you have mud on your head?"

The first k - 1 times, they all say "no," but the kth time the dirty children answer "yes." The father's announcement, though it conveyed no new *individual* knowledge (each child already knew at least one was muddy), created **common knowledge** of the fact — and it is this common knowledge that enables the inductive reasoning.

---

## 3. A Hierarchy of States of Knowledge

The paper defines a hierarchy of group knowledge states:

1. **Individual knowledge** — Agent i knows φ
2. **Everyone knows** — E(φ): every agent in the group knows φ
3. **Distributed knowledge** — D(φ): the knowledge is distributed among members of the group, without any individual necessarily having it. If agents could pool their knowledge, they would know φ.
4. **Common knowledge** — C(φ): everyone knows φ, everyone knows that everyone knows φ, everyone knows that everyone knows that everyone knows φ, and so on *ad infinitum*.

The hierarchy satisfies: D(φ) is implied by any individual's knowledge; C(φ) implies E^k(φ) for all finite k.

---

## 4. The Coordinated Attack Problem

Two divisions of an army are camped on hills overlooking a valley. They must attack simultaneously or not at all — an uncoordinated attack is worse than no attack. Their only communication is by messenger through the valley, but messengers can be captured (unreliable communication).

General A sends a message to General B: "Attack at dawn." B sends an acknowledgment. But how does B know A received the acknowledgment? A sends an acknowledgment of the acknowledgment... This leads to an infinite regress. No finite number of messages can establish common knowledge of the attack plan.

**Result:** With unreliable communication, common knowledge cannot be attained. The [[Coordinated Attack Problem|coordinated attack problem]] has no solution.

---

## 5. A General Model of a Distributed System

A distributed system is modeled as a collection of interacting agents (processors). The system's execution over time is captured as a *run* — a function from time to global states. A global state is a tuple of local states, one for each agent plus one for the "environment." The set of all possible runs constitutes a *system*.

---

## 6. Ascribing Knowledge to Processors

Knowledge is formalized using possible-worlds semantics (Kripke structures). Processor i **knows** fact φ at point (r, m) if φ holds at all points (r', m') that i considers possible — that is, at all points where i has the same local state.

Formally: (r, m) ⊨ K_i(φ) iff for all (r', m') such that r_i(m) = r'_i(m'), we have (r', m') ⊨ φ.

This captures the intuition that knowledge is determined by local state: an agent knows everything that follows from its local information.

---

## 7. Coordinated Attack Revisited

The paper formalizes the connection: performing a simultaneous action (like coordinated attack) requires common knowledge of the decision to act. Since common knowledge cannot be attained with unreliable communication, simultaneous coordinated actions are impossible in such systems.

---

## 8. Attaining Common Knowledge

**Central [[Impossibility Result|impossibility result]]:** In systems where communication is not guaranteed (messages can be lost or delayed by unpredictable amounts), common knowledge of any fact that was not common knowledge initially **cannot** be attained.

More precisely, if the system allows for the possibility that any given message might not be delivered, then sending messages cannot increase common knowledge.

This result generalizes the coordinated attack impossibility. It applies to any system where communication is imperfect — which includes virtually all practical distributed systems.

---

## 9. A Paradox?

If common knowledge is required for coordination and common knowledge is unattainable, how does anything ever get coordinated in practice? The resolution comes from recognizing that:

1. Approximate forms of coordination are often sufficient
2. Weaker notions of common knowledge can serve as practical substitutes
3. The impossibility applies to *guaranteed* simultaneous coordination, not to coordination that works "most of the time"

---

## 10. Common Knowledge Revisited

The paper reconsiders common knowledge in light of the impossibility result, motivating the study of weaker variants that can be achieved in practice.

---

## 11. ε-Common Knowledge and Eventual Common Knowledge

**[[ε-Common Knowledge]]:** Everyone knows φ with high probability, everyone knows that everyone knows with high probability, etc. Achievable in practice when communication is reliable with high probability.

**Eventual [[Common Knowledge]]:** At some future time, the group will have common knowledge of φ. Useful for reasoning about protocols that eventually reach a stable state.

---

## 12. Timestamping: Using Relativistic Time

In systems with bounded message delivery times, a form of common knowledge based on temporal guarantees becomes possible. If it is known that message delivery takes at most d time units, then d time units after broadcasting a message, the sender can know that all recipients have the information — and reason about what they know about what others know, up to bounded depth.

---

## 13. Internal Knowledge Consistency

It is *internally knowledge consistent* to assume that a certain state of knowledge holds at a given point if nothing the processors in the system will ever encounter will be inconsistent with this assumption. This provides a practical criterion for when it is safe to act as if common knowledge holds, even though strictly speaking it does not.

---

## 14. Conclusions

Explicitly reasoning about knowledge provides a powerful tool for understanding distributed systems. The hierarchy of knowledge states — from distributed knowledge through common knowledge — captures essential aspects of coordination problems. While true common knowledge is unattainable in practice, weaker variants provide workable substitutes that enable practical protocol design.

The framework connects classical epistemic logic to computer science, providing formal tools for what protocol designers do intuitively: reason about what processors know, and what they know about what others know.

---

## Key Contributions

1. **Formal framework** for reasoning about knowledge in distributed systems using possible-worlds semantics
2. **Hierarchy of group knowledge**: distributed knowledge → individual knowledge → everyone knows → common knowledge
3. **Impossibility result**: common knowledge cannot be attained with unreliable communication
4. **Practical variants**: ε-common knowledge, eventual common knowledge, timestamped knowledge
5. **Internal knowledge consistency**: criterion for safely assuming common knowledge

---

## References (selected)

- Aumann, R.J. Agreeing to disagree. Ann. Stat. 4, 6 (1976), 1236-1239.
- Barwise, J. Scenes and other situations. J. Philo. LXXVIII 7 (1981), 369-397.
- Chandy, K.M. and Lamport, L. Distributed snapshots: Determining global states of distributed systems. ACM TOCS 3, 1 (1985), 63-75.
- Dwork, C. and Moses, Y. Knowledge and common knowledge in a Byzantine environment I: Crash failures. Inf. Comput. 88, 2 (1990), 156-186.
- Fagin, R. and Halpern, J.Y. Belief, awareness, and limited reasoning. Artif. Int. 34 (1988), 39-76.
- Fischer, M.J., Lynch, N., and Paterson, M. Impossibility of distributed consensus with one faulty process. JACM 32, 2 (1985), 374-382.
- Gray, J. Notes on database operating systems. In Operating Systems: An Advanced Course, Lecture Notes in Computer Science 60, 1978.
- Lewis, D. Convention, A Philosophical Study. Harvard University Press, Cambridge, MA, 1969.
