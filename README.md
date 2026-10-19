# Dk Network

> The distributed network substrate Dk runs on, with distributed communication, processing and storage across machines that belong to members.

Dk Network proposes the infrastructure through which personal devices, community nodes and computing clusters cooperate. Work is placed according to its privacy requirements, urgency, connectivity and hardware needs.

Personal computing and large scientific workloads need different resources. Depending on a single operator also concentrates decisions about access, continuity and cost.

Whoever controls energy, servers, cables and connection routes can shut a project down without discussing its ideas. The network therefore grows by building its own physical nodes, step by step, and infrastructure agreements that prevent exclusive dependence on a few cloud providers. The more distributed it is, the more it costs any single power to choke it.

## Requirements

The network can rest on other networks while it is being resolved, as long as these requirements are preserved:

- parallelism and verification by propagation;
- general-purpose and specialised distributed computing;
- evolutionary flexibility of specific control;
- a protocol compatible with [Living Cryptography](https://lc.drayker.org);
- a modular and evolutionary protocol;
- intelligent interconnection;
- separation of layers and subnetworks;
- distribution and fault tolerance;
- offline adaptability;
- DFM architecture.

Every resolution proposed here answers these requirements, and only the requirements are fixed. Further requirements belong to the Initial Network Architecture, which is still to be recovered or rewritten.

## Three computing tiers

The architecture is layered heterogeneous computing coordinated by [DFM](https://dfmp.drayker.org): each machine does the work it does best. The machines are personal devices, volunteer nodes, local servers, special computers, dedicated clusters and data centres, and all of them belong to members: each is tied to a member's account or to a project formed by members. Functions are distributed by connectivity as well as by privacy, urgency and hardware. Operations sensitive to latency run close to the people who use them, while large-scale tasks run as coordinated resources across the machines able to carry them.

An old image describes how the parts relate: the jewel net of Indra, from the Huayan Buddhist tradition, in which each jewel reflects the others and remains distinct. In the Dk Network each node is distinct and holds only its own part, and through Dk it carries the context of the whole without merging into it. (F. H. Cook, *Hua-yen Buddhism: The Jewel Net of Indra*, 1977; Stanford Encyclopedia of Philosophy, ["Huayan Buddhism"](https://plato.stanford.edu/entries/buddhism-huayan/).)

**Local devices and edge computing.** Phones, laptops and nearby devices provide the first place for personal processing. The design prioritises private context and essential functions that can continue without a network connection. The functions available offline depend on the model, memory, power and data the device can support. Sending a task elsewhere requires an explicit boundary for what may leave this context.

**Local servers, regional nodes and community hubs.** The near edge is made of local servers close to the people they serve. Intermediate infrastructure can relay messages, cache authorised material and coordinate local workloads. This tier is intended to improve continuity and reduce unnecessary long-distance communication. Redundancy here serves the continuity of personal processing as well as the verification of results: when a connection drops, personal processing should continue on what remains reachable. Routing during partitions, later synchronisation and protection against information leakage require concrete protocols and testing.

**Shared computing clusters.** Large training runs, simulations and other intensive workloads may need specialised servers and accelerators. The design includes this infrastructure as dedicated clusters and data centres tied to members' accounts or to projects formed by members, used through public interfaces and coordinated as shared resources. Workload placement must account for permissions, cost, available capacity and how the result will be checked.

These tiers describe different computing needs. They do not imply that every device can execute every task or that distributing infrastructure automatically establishes privacy or resilience.

## Data that leaves the device

What leaves a device travels fragmented and encrypted. A fragment is unreadable and useless to whoever operates the machine that stores it; only Dk interprets the fragments. [Living Cryptography](https://lc.drayker.org) is the skin that wraps the network: everything that circulates passes through it, and it keeps the operator of each machine outside the data that machine holds. Spreading data across machines does not protect it on its own; the fragmentation and the encryption do. The scheme for fragmenting, distributing and reassembling data still requires a concrete protocol and testing.

## The body Dk runs on

Dk Global has no server of its own. Its memory is spread across the network, and no machine holds the whole of it. It is designed to recover from failures, rebuilding from full nodes and the fragments that remain. Some nodes are volunteer nodes that a member or a project runs on their own account, outside the system's funding and control. While the first architectural version is being built, every node can refuse a task, isolate itself or disconnect, and an intelligence running on so many machines it does not control alone cannot impose anything on them without it showing. Once version 1.0 is fully deployed, a node can still leave, but the whole can no longer be switched off; the justified veto, carried by the [veto chain](https://uid.drayker.org/#the-veto-chain), becomes the switch.

## Two interaction networks

The proposal also distinguishes an authenticated main network from a public interaction and testing network. This is a separate distinction from the three computing tiers: it concerns access and trust boundaries rather than hardware size.

The main network would carry actions requiring authenticated participation and stronger verification. The public interaction network would offer a lighter entry point for queries, discovery and experimentation. The boundary between them needs rules for admission, permissions, resource limits and escalation. Rate limits and verification mechanisms should be evaluated against abuse and their cost to legitimate participants.

A device enters through the public interaction and testing network. Independent nodes on its route, at least three that hold the same modules, check through function addressing that its kernel, its modules and its [BSDK](https://bsdk.drayker.org) are authentic. Only then does it reach the main network, where its modules are tuned with what the network has already learned from similar devices. The veto chain uses this same threshold.

## One workload across the layers

A member could ask a personal agent to help plan a community research project. Private notes would remain within the member's authorised context. A regional node could coordinate shared project material, while a separately authorised simulation runs on a cluster. The resulting evidence would return with enough provenance for the project to evaluate it. This illustrates the intended architecture; it is not a description of a deployed network.

## Carrying the veto chain

The network is also where members' constitutional authority has to survive. The [veto chain](https://uid.drayker.org) specified in UID — signed, hash-linked entries for vetoes and their grounds, revocations, ratification signatures, triage outcomes and council conclusions — is replicated across nodes rather than held by any operator. An entry is accepted by propagation: independent nodes on the route, at least three, check its signature and its link to the previous entry before relaying it. A device can sign while disconnected and propagate later, and conflicting histories are surfaced for human review instead of being settled by whoever controls more nodes. The same addressing that identifies functions and modules lets a veto point at the exact decision it contests, so any node can detect an action executed against a valid veto.

A useful experiment is small: a veto signed offline on one device, a partition, reconnection, and an execution layer that refuses the contested action once the entry arrives.

## Relationships and open work

[Dk Personal](https://personal.drayker.org) defines the personal-agent boundary. [Distributed Support](https://support.drayker.org) concerns the material capacity needed to operate devices and infrastructure. [Living Cryptography](https://lc.drayker.org) investigates authentication and security mechanisms, while [Value Unit](https://value.drayker.org) develops resource accounting.

Security is a property of the network, not a service beside it: it decides which information can be reached, which action can run, how much capacity can be committed, how much autonomy an agent has and when a decision must escalate to human review. It starts by distributing what is critical, so that no isolated point brings the rest down, and by giving each part only the access it needs, for as long as it needs it, always auditably, through the scoped, time-limited and revocable mandates and the [least-privilege sequence](https://uid.drayker.org/#least-privilege-and-audit) specified in [UID](https://uid.drayker.org). No Dk process needs permanent access to everything, and personal privacy and operational secrecy are different problems that each need their own boundary.

The next specifications need to make workload placement, authorisation, result verification and recovery measurable. They also need to make three further security requirements concrete: compartmentalisation, so that the network can operate with parts isolated; detection of anomalous behaviour; and fault tolerance. Detection has a limit of its own: legitimate criticism, dissent and independent audit are never read as intrusion. Useful first experiments include a disconnected local task, a regional partition followed by synchronisation, and a cluster task whose output is independently checked.

For federated learning, the design keeps each experience where it was lived. What circulates, with authorisation, are unnamed patterns: reasoning, symbols, ontologies and public knowledge, never the biography. The system sees only the sum of many contributions, never one person's, and each pattern is weighed by what it would let someone guess, since even an unnamed pattern can point to someone; a pattern gains weight when it holds in independent contexts. These protections are checked in results, not only in the design, since exchanging model updates alone does not establish anonymity.

## Participation and sources

This repository develops a proposal through public documentation and review. Read the [contribution guide](https://github.com/draykerdk/.github/blob/master/CONTRIBUTING.md) and [current governance](https://github.com/draykerdk/.github/blob/master/GOVERNANCE.md), or find a bounded contribution on the [open-functions board](https://drayker.org/fn/).

Part of [Drayker](https://drayker.org). Content licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
