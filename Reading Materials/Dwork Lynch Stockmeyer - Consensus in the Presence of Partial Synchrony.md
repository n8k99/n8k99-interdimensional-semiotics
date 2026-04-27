---
title: "Consensus in the Presence of Partial Synchrony"
authors: ["Cynthia Dwork", "Nancy Lynch", "Larry Stockmeyer"]
year: 1988
type: "[[reading-comment]]"
icon: "📄"
domain: "[[The Commons]]"
tags: [interdimensional-semiotics, distributed-systems, consensus, partial-synchrony, fault-tolerance]
source: "Journal of the ACM, Vol. 35, No. 2, April 1988, pp. 288-323"
pdf: "https://groups.csail.mit.edu/tds/papers/Lynch/jacm88.pdf"
award: "2007 Dijkstra Prize"
---

# Consensus in the Presence of Partial Synchrony

**Cynthia Dwork** — IBM Almaden Research Center (later Harvard)
**Nancy Lynch** — Massachusetts Institute of Technology
**Larry Stockmeyer** — IBM Almaden Research Center

---

## Abstract

The concept of [[Partial Synchrony|partial synchrony]] in a distributed system is introduced. Partial synchrony lies between the cases of a synchronous system and an asynchronous system. In a synchronous system, there is a known fixed upper bound Δ on the time required for a message to be sent from one processor to another and a known fixed upper bound Φ on the relative speeds of different processors. In an asynchronous system no fixed upper bounds Δ and Φ exist.

In one version of partial synchrony, fixed bounds Δ and Φ exist, but they are not known a priori. The problem is to design protocols that work correctly regardless of the actual values of the bounds. In another version, the bounds are known, but are only guaranteed to hold starting at some unknown time T (the [[Global Stabilization Time]], or GST), and protocols must be designed to work correctly regardless of when T occurs.

Fault-tolerant consensus protocols are given for various cases of partial synchrony and various fault models. Lower bounds that show in most cases that the protocols are optimal with respect to the number of faults tolerated are also given. The consensus protocols for partially synchronous processors use new protocols for fault-tolerant "distributed clocks" that allow partially synchronous processors to reach some approximately common notion of time.

---

## 1. Introduction

### 1.1 Background

The role of synchronism in distributed computing had received considerable attention. One method of comparing two models with differing amounts of synchronism is to examine a specific problem in both models. The problem chosen is often that of reaching agreement ([[Consensus|consensus]]).

**The consensus problem:** A collection of N processors p1, ..., pN communicate by sending messages. Initially each processor pi has a value vi. The correct processors must all decide on the same value; if the initial values are all the same (say v), then v must be the common decision. The protocol should operate correctly even if some processors are faulty.

**Fault types:**
- **Fail-stop faults**: processors crash
- **Omission faults**: processors fail to send or receive messages when they should
- **[[Byzantine Fault|Byzantine faults]]**: processors send erroneous messages (with or without authentication)

**Prior results:**
- In fully synchronous systems with known bounds, N-resilient protocols exist for Byzantine failures with authentication (any number of faults can be tolerated)
- For Byzantine faults without authentication: t-resilient consensus possible iff N ≥ 3t + 1
- Fischer, Lynch, and Paterson (FLP) proved: if communication is fully asynchronous, there is no consensus protocol resilient to even one fail-stop fault

### 1.2 Partially Synchronous Communication

Two natural formulations:

**Unknown bounds:** An upper bound Δ on message delivery time exists, but its value is not known a priori. Design protocols that work correctly for any Δ.

**Eventually holding bounds (GST model):** Δ is known, but messages may be unreliable. For each execution there is a [[Global Stabilization Time]] (GST), unknown to processors, such that the message system respects Δ from time GST onward.

**Key insight:** Safety conditions (no disagreement, no invalid decisions) must hold no matter how asynchronously the message system behaves. Termination (each correct processor eventually decides) is only required when Δ holds eventually. These conditions are equivalent to the GST formulation.

### 1.3 Partially Synchronous Communication and Processors

Combining both partially synchronous communication and partially synchronous processors.

### 1.4 Partially Synchronous Processors

Analogous treatment to communication: processor speed bounds Φ either unknown or eventually holding.

---

## 2. Definitions

### 2.1 Model of Computation

Processors are modeled as (potentially infinite-state) automata connected by point-to-point channels. Computation proceeds in continuous real time. Each processor has a local clock that may run at varying rates.

### 2.2 Failures

- **Fail-stop**: processor stops executing, detectable by other processors
- **Send-omission**: processor fails to send messages it should
- **Receive-omission**: processor fails to receive messages sent to it
- **Omission**: send-omission or receive-omission
- **Byzantine**: processor deviates arbitrarily from its protocol (with authentication: cannot forge authenticated messages; without: no restrictions)

### 2.3 Partial Synchrony

Formally defined as constraints on message delivery times and processor speeds that hold either always (with unknown bounds) or from some unknown GST onward (with known bounds).

### 2.4 Correctness of a Consensus Protocol

Agreement (all correct processors decide the same value), validity (the decision value must be some processor's initial value), and termination (all correct processors eventually decide).

---

## 3. The Basic Round Model

### 3.1 Definition

Processing is divided into synchronous rounds. In each round, every processor sends messages, receives messages, and performs local computation.

### 3.2 Protocols

#### 3.2.1 Fail-Stop and Omission Faults

Algorithm achieving consensus with N ≥ 2t + 1 processors. Uses a rotating coordinator approach with N phases per round.

#### 3.2.2 Byzantine Faults with Authentication

Algorithm achieving consensus with N ≥ 3t + 1. Again uses rotating coordinator, but with additional authentication steps.

#### 3.2.3 Byzantine Faults without Authentication

Modified algorithm maintaining N ≥ 3t + 1 requirement, but without relying on unforgeable signatures.

---

## 4. Partially Synchronous Communication and Synchronous Processors

### Main Results Table

| Failure type | Asynchronous | Synchronous | Partially synchronous comm. + sync. processors |
|---|---|---|---|
| Fail-stop | ∞ (impossible) | t + 1 | 2t + 1 |
| Omission | ∞ | t + 1 | 2t + 1 |
| Authenticated Byzantine | ∞ | t + 1 | 3t + 1 |
| Byzantine | 3t + 1 | 3t + 1 | 3t + 1 |

(Table entries show minimum N for which a t-resilient consensus protocol exists)

### 4.1 Upper Bounds When Δ Holds Eventually (GST model)

Adapts the basic round model algorithms. Key challenge: processors don't know when GST occurs, so they must maintain safety even during the asynchronous period.

### 4.2 Upper Bounds for Δ Unknown

Protocols that work for any value of Δ. Uses a "doubling" technique: try successively larger values of the timeout.

### 4.3 Lower Bounds

Matching lower bounds proving the protocols are optimal:
- Fail-stop/omission: N ≥ 2t + 1 is necessary
- Authenticated Byzantine: N ≥ 3t + 1 is necessary

---

## 5. Partially Synchronous Communication and Processors

When both communication and processor speeds are partially synchronous, the problem becomes harder. The paper introduces **distributed clocks** — protocols that allow processors with unsynchronized clocks to achieve an approximately common notion of time.

### 5.1 Distributed Clock for Byzantine Faults without Authentication

A protocol allowing processors to maintain approximately synchronized round counters despite Byzantine faults, even when processor speeds are partially synchronous.

### 5.2 Distributed Clock for Byzantine Faults with Authentication

Similar protocol leveraging authentication.

### 5.3 Upper Bounds When Δ and Φ Hold Eventually

Combines distributed clocks with consensus protocols from Section 4.

### 5.4 Upper Bounds When Δ and Φ Are Unknown

Combines the doubling technique with distributed clocks.

---

## 6. Lower Bounds for Partially Synchronous Processors

The paper proves that many of the upper bounds are tight, establishing exact thresholds.

---

## 7. Open Problems

- Tight bounds for some remaining cases
- Message complexity improvements
- Relationship to other distributed computing problems

---

## Key Contributions

1. **Defined partial synchrony** — the critical middle ground between synchronous and asynchronous models that captures real-world systems
2. **[[Global Stabilization Time]] (GST)** — elegant formulation separating safety (always) from liveness (after GST)
3. **Exact resilience bounds** for four fault models under partial synchrony
4. **Distributed clocks** — novel technique for processors with unsynchronized clocks to coordinate
5. **The standard escape hatch from FLP** — showed that with upper bounds on message delays (even unknown ones), consensus becomes solvable

---

## Significance

This paper, along with FLP (Fischer, Lynch, Paterson 1985), forms the theoretical foundation of practical distributed consensus. Virtually all real-world consensus protocols (Paxos, Raft, PBFT, Tendermint) operate in the partial synchrony model: they guarantee safety always and liveness after GST. The paper received the **2007 Dijkstra Prize** for its profound influence on distributed computing.

---

## References (selected)

1. Ben-Or, M. Another advantage of free choice: Completely asynchronous agreement protocols. In Proceedings of the 2nd ACM PODC, 1983.
2. Bracha, G. An asynchronous [(n-1)/3]-resilient consensus protocol. In Proceedings of the 3rd ACM PODC, 1984.
3. Dolev, D. and Strong, H.R. Authenticated algorithms for Byzantine agreement. SIAM J. Comput. 12, 4 (1983), 656-666.
4. Dolev, D., Dwork, C., and Stockmeyer, L. On the minimal synchronism needed for distributed consensus. JACM 34, 1 (1987), 77-97.
5. Fischer, M.J., Lynch, N., and Paterson, M. Impossibility of distributed consensus with one faulty process. JACM 32, 2 (1985), 374-382.
6. Hadzilacos, V. On the relationship between the atomic commitment and consensus problems. In Fault-Tolerant Distributed Computing, Lecture Notes in Computer Science 448, 1990.
7. Lamport, L. Time, clocks, and the ordering of events in a distributed system. CACM 21, 7 (1978), 558-565.
8. Lamport, L., Shostak, R., and Pease, M. The Byzantine Generals problem. ACM TOPLAS 4, 3 (1982), 382-401.
9. Pease, M., Shostak, R., and Lamport, L. Reaching agreement in the presence of faults. JACM 27, 2 (1980), 228-234.
