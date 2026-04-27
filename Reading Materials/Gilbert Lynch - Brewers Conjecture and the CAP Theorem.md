---
title: "Brewer's Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services"
authors: ["Seth Gilbert", "Nancy Lynch"]
year: 2002
type: "[[reading-comment]]"
icon: "📄"
domain: "[[The Commons]]"
tags: [interdimensional-semiotics, distributed-systems, impossibility-results, CAP-theorem]
source: "ACM SIGACT News, Volume 33, Issue 2, June 2002, pp. 51-59"
pdf: "https://users.ece.cmu.edu/~adrian/731-sp04/readings/GL-cap.pdf"
---

# Brewer's Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services

**Seth Gilbert and Nancy Lynch**
Laboratory for Computer Science, Massachusetts Institute of Technology

---

## Abstract

When designing distributed web services, there are three properties that are commonly desired: consistency, availability, and [[Partition Tolerance|partition tolerance]]. It is impossible to achieve all three. In this note, we prove this conjecture in the asynchronous network model, and then discuss solutions to this dilemma in the [[Partial Synchrony|partially synchronous]] model.

---

## 1. Introduction

At PODC 2000, Brewer, in an invited talk, made the following conjecture: it is impossible for a web service to provide the following three guarantees:

- **Consistency**
- **Availability**
- **Partition-tolerance**

All three of these properties are desirable — and expected — from real-world web services. The note first discusses what Brewer meant by the conjecture; next formalizes these concepts and proves the conjecture; finally, describes and attempts to formalize some real-world solutions to this practical difficulty.

Most web services today attempt to provide strongly consistent data. There has been significant research designing ACID (Atomic, Consistent, Isolated, Durable) databases, and most of the new frameworks for building distributed web services depend on these databases. Interactions with web services are expected to behave in a transactional manner: operations commit or fail in their entirety (atomic), committed transactions are visible to all future transactions (consistent), uncommitted transactions are isolated from each other (isolated), and once a transaction is committed it is permanent (durable).

Web services are similarly expected to be highly available. Every request should succeed and receive a response. The goal of most web services today is to be as available as the network on which they run: if any service on the network is available, then the web service should be accessible.

Finally, on a highly distributed network, it is desirable to provide some amount of fault-tolerance. When some nodes crash or some communication links fail, it is important that the service still perform as expected. One desirable fault tolerance property is the ability to survive a network partitioning into multiple components.

---

## 2. Formal Model

### 2.1 Atomic Data Objects

The most natural way of formalizing the idea of a consistent service is as an atomic data object. Atomic, or [[Linearizability|linearizable]], consistency is the condition expected by most web services today. Under this consistency guarantee, there must exist a total order on all operations such that each operation looks as if it were completed at a single instant. This is equivalent to requiring requests of the distributed shared memory to act as if they were executing on a single node, responding to operations one at a time. One important property of an atomic read/write shared memory is that any read operation that begins after a write operation completes must return that value, or the result of a later write operation.

### 2.2 Available Data Objects

For a distributed system to be continuously available, every request received by a non-failing node in the system must result in a response. That is, any algorithm used by the service must eventually terminate. When qualified by the need for partition tolerance, this can be seen as a strong definition of availability: even when severe network failures occur, every request must terminate.

### 2.3 Partition Tolerance

The network will be allowed to lose arbitrarily many messages sent from one node to another. When a network is partitioned, all messages sent from nodes in one component of the partition to nodes in another component are lost. (And any pattern of message loss can be modeled as a temporary partition separating the communicating nodes at the exact instant the message is lost.)

---

## 3. Asynchronous Networks

### 3.1 Impossibility Result

**Theorem 1.** It is impossible in the asynchronous network model to implement a read/write data object that guarantees the following properties:
- Availability
- Atomic consistency

in all fair executions (including those in which messages are lost).

**Proof:** By contradiction. Assume an algorithm A exists that meets atomicity, availability, and partition tolerance. The network consists of at least two nodes, divided into two disjoint, non-empty sets: {G1, G2}. All messages between G1 and G2 are lost. If a write occurs in G1, and later a read occurs in G2, then the read operation cannot return the results of the earlier write operation.

Let v0 be the initial value. Let α1 be the prefix of an execution in which a single write of a value not equal to v0 occurs in G1, ending with the termination of the write operation. No messages between G1 and G2 are delivered. By availability, the write completes. Similarly, let α2 be the prefix of an execution in which a single read occurs in G2. The value returned must be v0, as no write has occurred in α2.

Let α be an execution beginning with α1 and continuing with α2. To nodes in G2, α is indistinguishable from α2 (all messages from G1 are lost). Therefore the read must still return v0. However the read begins after the write completes — contradicting atomicity.

**Corollary 1.1.** It is impossible in the asynchronous network model to implement a read/write data object that guarantees availability in all fair executions, and atomic consistency in fair executions in which no messages are lost.

**Proof:** In the asynchronous model, an algorithm has no way of determining whether a message has been lost or arbitrarily delayed. Therefore if an algorithm guaranteed atomic consistency when all messages are delivered, it would guarantee atomic consistency in all executions, violating Theorem 1.

### 3.2 Solutions in the Asynchronous Model

While it is impossible to provide all three properties, any two can be achieved:

**Atomic, Partition Tolerant:** A centralized algorithm where a single designated node maintains the value. Available when all messages are delivered.

**Atomic, Available:** If there are no partitions, it is clearly possible to provide atomic, available data. Systems on intranets and LANs are an example.

**Available, Partition Tolerant:** Possible if atomic consistency is not required. Web caches are one example of a weakly consistent network.

---

## 4. Partially Synchronous Networks

### 4.1 Partially Synchronous Model

Every node has a clock; all clocks increase at the same rate but may display different values at the same real time (acting as timers). Every message is either delivered within a given, known time tmsg, or it is lost. Every node processes a received message within a given, known time tlocal.

### 4.2 Impossibility Result

**Theorem 2.** It is impossible in the partially synchronous network model to implement a read/write data object that guarantees availability and atomic consistency in all executions (even those in which messages are lost).

### 4.3 Solutions in the Partially Synchronous Model

The analogue of Corollary 1.1 does *not* hold in the partially synchronous model. There are algorithms that return atomic data when all messages are delivered, and only return inconsistent (stale) data when messages are lost.

### 4.4 Weaker Consistency Conditions: Delayed-t Consistency

**Definition 3.** A timed execution α of a read-write object is **Delayed-t Consistent** if:

1. P is a partial order that orders all write operations, and orders all read operations with respect to the write operations.
2. The value returned by every read operation is exactly the one written by the previous write operation in P (or the initial value).
3. The order in P is consistent with the order of read and write requests submitted at each node.
4. **(Atomicity)** If all messages are delivered, and an operation θ completes before an operation φ begins, then φ does not precede θ in P.
5. **(Weakly Consistent)** If there exists an interval of time longer than t in which no messages are lost, and θ completes before the interval begins, and φ begins after the interval ends, then φ does not precede θ in P.

This allows stale data when messages are lost, but provides a time limit on how long inconsistency can continue once the partition heals.

**Theorem 4.** The modified centralized algorithm is Delayed-t consistent.

---

## 5. Conclusion

It is impossible to reliably provide atomic, consistent data when there are partitions in the network. It is feasible, however, to achieve any two of the three properties: consistency, availability, and partition tolerance. In an asynchronous model, the [[Impossibility Result|impossibility result]] is strong: it is impossible to provide consistent data, even allowing stale data when messages are lost. In partially synchronous models it is possible to achieve a practical compromise between consistency and availability. Most real-world systems today are forced to settle with returning "most of the data, most of the time."

---

## References

1. Attiya, Bar-Noy, Dolev, Koller, Peleg, and Reischuk. Achievable cases in an asynchronous environment. In 28th Annual Symposium on Foundations of Computer Science, 1987.
2. Eric A. Brewer. Towards robust distributed systems. (Invited Talk) Principles of Distributed Computing, Portland, Oregon, July 2000.
3. Fekete, Gupta, Luchangco, Lynch, and Shvartsman. Eventually-serializable data services. Theoretical Computer Science, 220(1):113-156, June 1999.
4. Herlihy, M.P. and Wing, J.M. [[Linearizability]]: A correctness condition for concurrent objects. ACM TOPLAS, 12(3):463-492, July 1990.
5. Lamport, L. On interprocess communication — parts I and II. Distributed Computing, 1(2):77-101, April 1986.
6. Lynch, N. Distributed Algorithms, pp. 397-350. Morgan Kaufman, 1996.
7. Lynch, N. Distributed Algorithms, pp. 199-231. Morgan Kaufman, 1996.
8. Lynch, N. Distributed Algorithms, p. 581. Morgan Kaufman, 1996.
9. Lynch, N. Distributed Algorithms, pp. 735-770. Morgan Kaufman, 1996.
