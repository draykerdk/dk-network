# Dk Network

> Local devices, regional nodes and shared computing clusters.

Dk Network proposes the infrastructure through which personal devices, community nodes and computing clusters cooperate. Work is placed according to its privacy requirements, urgency and hardware needs.

Personal computing and large scientific workloads need different resources. Depending on a single operator also concentrates decisions about access, continuity and cost.

## Three computing tiers

**Local devices and edge computing.** Phones, laptops and nearby devices provide the first place for personal processing. The design prioritises private context and essential functions that can continue without a network connection. The functions available offline depend on the model, memory, power and data the device can support. Sending a task elsewhere requires an explicit boundary for what may leave this context.

**Regional nodes and community hubs.** Intermediate infrastructure can relay messages, cache authorised material and coordinate local workloads. This tier is intended to improve continuity and reduce unnecessary long-distance communication. Routing during partitions, later synchronisation and protection against information leakage require concrete protocols and testing.

**Shared computing clusters.** Large training runs, simulations and other intensive workloads may need specialised servers and accelerators. The design includes this infrastructure through independent operators and public interfaces. Workload placement must account for permissions, cost, available capacity and how the result will be checked.

These tiers describe different computing needs. They do not imply that every device can execute every task or that distributing infrastructure automatically establishes privacy or resilience.

## Two interaction networks

The proposal also distinguishes an authenticated main network from a public interaction and testing network. This is a separate distinction from the three computing tiers: it concerns access and trust boundaries rather than hardware size.

The main network would carry actions requiring authenticated participation and stronger verification. The public interaction network would offer a lighter entry point for queries, discovery and experimentation. The boundary between them needs rules for admission, permissions, resource limits and escalation. Rate limits and verification mechanisms should be evaluated against abuse and their cost to legitimate participants.

## One workload across the layers

A member could ask a personal agent to help plan a community research project. Private notes would remain within the member's authorised context. A regional node could coordinate shared project material, while a separately authorised simulation runs on a cluster. The resulting evidence would return with enough provenance for the project to evaluate it. This illustrates the intended architecture; it is not a description of a deployed network.

## Relationships and open work

[Dk Personal](https://personal.drayker.org) defines the personal-agent boundary. [Distributed Support](https://support.drayker.org) concerns the material capacity needed to operate devices and infrastructure. [Living Cryptography](https://lc.drayker.org) investigates authentication and security mechanisms, while [Value Unit](https://value.drayker.org) develops resource accounting.

The next specifications need to make workload placement, authorisation, result verification and recovery measurable. Useful first experiments include a disconnected local task, a regional partition followed by synchronisation, and a cluster task whose output is independently checked. Federated learning requires its own privacy analysis; exchanging model updates alone does not establish anonymity.

## Participation and sources

This repository develops a proposal through public documentation and review. Read the [contribution guide](https://github.com/draykerdk/.github/blob/master/CONTRIBUTING.md) and [current governance](https://github.com/draykerdk/.github/blob/master/GOVERNANCE.md), or find a bounded contribution on the [open-functions board](https://drayker.org/fn/).

Part of [Drayker](https://drayker.org). Content licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
