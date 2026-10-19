# Dk Network

> Local devices, regional nodes and shared computing clusters.

Dk Network proposes the infrastructure through which personal devices, community nodes and computing clusters cooperate. Work is placed according to its privacy requirements, urgency, connectivity and hardware needs.

Personal computing and large scientific workloads need different resources. Depending on a single operator also concentrates decisions about access, continuity and cost.

## Three computing tiers

The architecture is layered heterogeneous computing coordinated by [DFM](https://dfmp.drayker.org): each machine does the work it does best. The machines are personal devices, volunteer nodes, local servers, special computers, dedicated clusters and data centres, and all of them belong to members: each is tied to a member's account or to a project formed by members. Functions are distributed by connectivity as well as by privacy, urgency and hardware. Operations sensitive to latency run close to the people who use them, while large-scale tasks run as coordinated resources across the machines able to carry them.

**Local devices and edge computing.** Phones, laptops and nearby devices provide the first place for personal processing. The design prioritises private context and essential functions that can continue without a network connection. The functions available offline depend on the model, memory, power and data the device can support. Sending a task elsewhere requires an explicit boundary for what may leave this context.

**Local servers, regional nodes and community hubs.** The near edge is made of local servers close to the people they serve. Intermediate infrastructure can relay messages, cache authorised material and coordinate local workloads. This tier is intended to improve continuity and reduce unnecessary long-distance communication. Redundancy here serves the continuity of personal processing as well as the verification of results: when a connection drops, personal processing should continue on what remains reachable. Routing during partitions, later synchronisation and protection against information leakage require concrete protocols and testing.

**Shared computing clusters.** Large training runs, simulations and other intensive workloads may need specialised servers and accelerators. The design includes this infrastructure as dedicated clusters and data centres tied to members' accounts or to projects formed by members, used through public interfaces and coordinated as shared resources. Workload placement must account for permissions, cost, available capacity and how the result will be checked.

These tiers describe different computing needs. They do not imply that every device can execute every task or that distributing infrastructure automatically establishes privacy or resilience.

## Data that leaves the device

What leaves a device travels fragmented and encrypted. A fragment is unreadable and useless to whoever operates the machine that stores it; only Dk interprets the fragments. [Living Cryptography](https://lc.drayker.org) is the skin that wraps the network: everything that circulates passes through it, and it keeps the operator of each machine outside the data that machine holds. Spreading data across machines does not protect it on its own; the fragmentation and the encryption do. The scheme for fragmenting, distributing and reassembling data still requires a concrete protocol and testing.

## Two interaction networks

The proposal also distinguishes an authenticated main network from a public interaction and testing network. This is a separate distinction from the three computing tiers: it concerns access and trust boundaries rather than hardware size.

The main network would carry actions requiring authenticated participation and stronger verification. The public interaction network would offer a lighter entry point for queries, discovery and experimentation. The boundary between them needs rules for admission, permissions, resource limits and escalation. Rate limits and verification mechanisms should be evaluated against abuse and their cost to legitimate participants.

## One workload across the layers

A member could ask a personal agent to help plan a community research project. Private notes would remain within the member's authorised context. A regional node could coordinate shared project material, while a separately authorised simulation runs on a cluster. The resulting evidence would return with enough provenance for the project to evaluate it. This illustrates the intended architecture; it is not a description of a deployed network.

## Carrying the veto chain

The network is also where members' constitutional authority has to survive. The [veto chain](https://uid.drayker.org) specified in UID — signed, hash-linked entries for vetoes and their grounds, revocations, ratification signatures, triage outcomes and council conclusions — is replicated across nodes rather than held by any operator. An entry is accepted by propagation: independent nodes on the route, at least three, check its signature and its link to the previous entry before relaying it. A device can sign while disconnected and propagate later, and conflicting histories are surfaced for human review instead of being settled by whoever controls more nodes. The same addressing that identifies functions and modules lets a veto point at the exact decision it contests, so any node can detect an action executed against a valid veto.

A useful experiment is small: a veto signed offline on one device, a partition, reconnection, and an execution layer that refuses the contested action once the entry arrives.

## Relationships and open work

[Dk Personal](https://personal.drayker.org) defines the personal-agent boundary. [Distributed Support](https://support.drayker.org) concerns the material capacity needed to operate devices and infrastructure. [Living Cryptography](https://lc.drayker.org) investigates authentication and security mechanisms, while [Value Unit](https://value.drayker.org) develops resource accounting.

The next specifications need to make workload placement, authorisation, result verification and recovery measurable. They also need to make three security requirements concrete: compartmentalisation, so that the network can operate with parts isolated; detection of anomalous behaviour; and fault tolerance. These sit alongside the scoped, time-limited and revocable mandates specified in [UID](https://uid.drayker.org). Useful first experiments include a disconnected local task, a regional partition followed by synchronisation, and a cluster task whose output is independently checked. Federated learning requires its own privacy analysis; exchanging model updates alone does not establish anonymity.

## Participation and sources

This repository develops a proposal through public documentation and review. Read the [contribution guide](https://github.com/draykerdk/.github/blob/master/CONTRIBUTING.md) and [current governance](https://github.com/draykerdk/.github/blob/master/GOVERNANCE.md), or find a bounded contribution on the [open-functions board](https://drayker.org/fn/).

Part of [Drayker](https://drayker.org). Content licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
