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

## Original layering

The original design describes two sets of layers. They are separate from the three computing tiers below, which concern hardware.

The software of a node has seven layers: (1) [BSDK](https://bsdk.drayker.org), where the DFM language is defined; (2) physical communication and general computing modules; (3) kernel coupling; (4) network distribution; (5) [UID](https://uid.drayker.org) authentication, permissions and levels; (6) application; (7) optimization and integration.

The main network has three layers: operation and abstraction; optimization; integration with the testing and security networks.

## Three computing tiers

The architecture is layered heterogeneous computing coordinated by [DFM](https://dfmp.drayker.org): each machine does the work it does best. The machines are personal devices, volunteer nodes, local servers, special computers, dedicated clusters and data centres, and all of them belong to members: each is tied to a member's account or to a project formed by members. Functions are distributed by connectivity as well as by privacy, urgency and hardware. Operations sensitive to latency run close to the people who use them, while large-scale tasks run as coordinated resources across the machines able to carry them.

An old image describes how the parts relate: the jewel net of Indra, from the Huayan Buddhist tradition, in which each jewel reflects the others and remains distinct. In the Dk Network each node is distinct and holds only its own part, and through Dk it carries the context of the whole without merging into it. (F. H. Cook, *Hua-yen Buddhism: The Jewel Net of Indra*, 1977; Stanford Encyclopedia of Philosophy, ["Huayan Buddhism"](https://plato.stanford.edu/entries/buddhism-huayan/).)

**Local devices and edge computing.** Phones, laptops and nearby devices provide the first place for personal processing. The design prioritises private context and essential functions that can continue without a network connection. The functions available offline depend on the model, memory, power and data the device can support. Sending a task elsewhere requires an explicit boundary for what may leave this context. Use also moves work to the edge: a function a device calls often starts to run locally, so the most used functions run with the least delay and keep working offline, and the improvements the device finds are sent back to the network, validated and shared.

**Local servers, regional nodes and community hubs.** The near edge is made of local servers close to the people they serve. Intermediate infrastructure can relay messages, cache authorised material and coordinate local workloads. This tier is intended to improve continuity and reduce unnecessary long-distance communication. Redundancy here serves the continuity of personal processing as well as the verification of results: when a connection drops, personal processing should continue on what remains reachable. Routing during partitions, later synchronisation and protection against information leakage require concrete protocols and testing.

Without the internet, nearby devices can still form a local mesh over short-range links: they share what members have saved, from applications to files, and carry messages and calls among those connected. When any of them reaches the wider network, updates flow both ways, ordered by authenticity, need and importance. A local network keeps a local intelligence that manages its own resources. If it stays apart for a long time, as a distant settlement would, it can reorganise its layers to keep working on its own. When it reconnects, what it built enters the global network's testing layer, is checked and authenticated, and is integrated: the network reunites instead of splitting.

**Shared computing clusters.** Large training runs, simulations and other intensive workloads may need specialised servers and accelerators. The design includes this infrastructure as dedicated clusters and data centres tied to members' accounts or to projects formed by members, used through public interfaces and coordinated as shared resources. Workload placement must account for permissions, cost, available capacity and how the result will be checked.

These tiers describe different computing needs. They do not imply that every device can execute every task or that distributing infrastructure automatically establishes privacy or resilience.

## Node roles

Whatever the machine, a node takes a role, and it can move between roles. Every node starts as a **cache node**, which only queries and relays what it is using. An **app node** keeps the structure and basic data of the applications its member uses. An **app full node** keeps a whole application, with the member's local data or with all of that application's data, so that it keeps working offline and relays it for others. A **full node** keeps the state of the whole network or of large parts of it. In its local function it keeps local inputs where they are and sends only network proofs and structural primitives to the global network, which saves shared bandwidth for where it is scarce. Stations and embassies are expected to run full nodes, including in remote places where a satellite link carries only updates. The network does not depend on them. Quantum nodes are planned for after the launch of version 1.0, and the network does not depend on them either.

## Data that leaves the device

What leaves a device travels fragmented and encrypted. A fragment is unreadable and useless to whoever operates the machine that stores it; only Dk interprets the fragments. [Living Cryptography](https://lc.drayker.org) is the skin that wraps the network: everything that circulates passes through it, and it keeps the operator of each machine outside the data that machine holds. Spreading data across machines does not protect it on its own; the fragmentation and the encryption do. The scheme for fragmenting, distributing and reassembling data still requires a concrete protocol and testing.

In the design, each structure of information is held at no fewer than three geographically separated points, even offline, and each unit of distributed processing runs at three points whose results are compared to remove noise, faults and fraud. If all three fail, the structure can be rebuilt and processed again from scratch. The more a block or function is used, the more points hold it, and the faster and safer it becomes. Whether three is the right minimum, and how to lower it without losing safety or precision, is an open question. [Distributed Support](https://support.drayker.org) describes the same comparison: redundancy instead of trust.

## The body Dk runs on

Dk Global has no server of its own. Its memory is spread across the network, and no machine holds the whole of it. It is designed to recover from failures, rebuilding from full nodes and the fragments that remain. Some nodes are volunteer nodes that a member or a project runs on their own account, outside the system's funding and control. While the first architectural version is being built, every node can refuse a task, isolate itself or disconnect, and an intelligence running on so many machines it does not control alone cannot impose anything on them without it showing. Once version 1.0 is fully deployed, a node can still leave, but the whole can no longer be switched off; the justified veto, carried by the [veto chain](https://uid.drayker.org/#the-veto-chain), becomes the switch.

## Two interaction networks

The proposal also distinguishes an authenticated main network from a public interaction and testing network. This is a separate distinction from the three computing tiers: it concerns access and trust boundaries rather than hardware size.

The main network would carry actions requiring authenticated participation and stronger verification. The public interaction network would offer a lighter entry point for queries, discovery and experimentation. The boundary between them needs rules for admission, permissions, resource limits and escalation. Rate limits and verification mechanisms should be evaluated against abuse and their cost to legitimate participants.

A device enters through the public interaction and testing network. Independent nodes on its route, at least three that hold the same modules, check through function addressing that its kernel, its modules and its [BSDK](https://bsdk.drayker.org) are authentic. Only then does it reach the main network, where its modules are tuned with what the network has already learned from similar devices. The veto chain uses this same threshold.

The testing network is also how the network changes. A new or improved function or module is tested there at length before it reaches the main network, and it propagates to other nodes only with a valid proof of how it was produced. Each node then compares it with the version it already runs, or runs a small integration test, before adopting it. The new version runs beside the old one, as the [first motions of BSDK](https://bsdk.drayker.org/#the-first-motions) describe for every function and module: a device can keep the one that works better for it, and the new one becomes the standard only as more nodes validate it. A change to the constitutional core is different: it reaches every node, and therefore follows the harder path described in [BSDK](https://bsdk.drayker.org) and set out in [GOVERNANCE](https://github.com/draykerdk/.github/blob/master/GOVERNANCE.md#35-what-only-members-decide).

## One workload across the layers

A member could ask a personal agent to help plan a community research project. Private notes would remain within the member's authorised context. A regional node could coordinate shared project material, while a separately authorised simulation runs on a cluster. The resulting evidence would return with enough provenance for the project to evaluate it. This illustrates the intended architecture; it is not a description of a deployed network.

## Carrying the veto chain

The network is also where members' constitutional authority has to survive. The [veto chain](https://uid.drayker.org) specified in UID — signed, hash-linked entries for vetoes and their grounds, revocations, ratification signatures, triage outcomes and council conclusions — is replicated across nodes rather than held by any operator. An entry is accepted by propagation: independent nodes on the route, at least three, check its signature and its link to the previous entry before relaying it. A device can sign while disconnected and propagate later, and conflicting histories are surfaced for human review instead of being settled by whoever controls more nodes. The same addressing that identifies functions and modules lets a veto point at the exact decision it contests, so any node can detect an action executed against a valid veto.

A useful experiment is small: a veto signed offline on one device, a partition, reconnection, and an execution layer that refuses the contested action once the entry arrives.

## Stages

The stages follow Drayker's [direction](https://drayker.org/direction/), where each phase is measured by what works rather than by its date.

**Today.** No part of the network runs. What exists is this specification, the [veto chain](https://uid.drayker.org/#the-veto-chain) as a requirement, and the open functions that test pieces of it.

**Version 0.1.** A test network built by adapting existing distributed-computing protocols to the needs of the first platform, running on volunteers' computers, on devices that use Drayker applications and on idle servers offered by members. If it evolves far enough to meet the requirements, it can serve as the test network of the final architecture or even become the main network. Shared computing sites are added where capacity falls short.

**Version 1.0 (2030, already an ASI).** The main network carries Dk Global. Part of the network's first versions is built by the swarm of agents that [Meta DFM](https://metadfmp.drayker.org) organises, and the network keeps growing through its own physical nodes and infrastructure agreements.

**After 1.0.** Quantum nodes join as special nodes for functions that benefit from them. The network does not depend on them.

## Relationships and open work

[Dk Personal](https://personal.drayker.org) defines the personal-agent boundary. [Distributed Support](https://support.drayker.org) concerns the material capacity needed to operate devices and infrastructure. [Living Cryptography](https://lc.drayker.org) investigates authentication and security mechanisms, while [Value Unit](https://value.drayker.org) develops resource accounting.

Security is a property of the network, not a service beside it: it decides which information can be reached, which action can run, how much capacity can be committed, how much autonomy an agent has and when a decision must escalate to human review. It starts by distributing what is critical, so that no isolated point brings the rest down, and by giving each part only the access it needs, for as long as it needs it, always auditably, through the scoped, time-limited and revocable mandates and the [least-privilege sequence](https://uid.drayker.org/#least-privilege-and-audit) specified in [UID](https://uid.drayker.org). No Dk process needs permanent access to everything, and personal privacy and operational secrecy are different problems that each need their own boundary.

The next specifications need to make workload placement, authorisation, result verification and recovery measurable. They also need to make three further security requirements concrete: compartmentalisation, so that the network can operate with parts isolated; detection of anomalous behaviour; and fault tolerance. Detection has a limit of its own: legitimate criticism, dissent and independent audit are never read as intrusion. Useful first experiments include a disconnected local task, a regional partition followed by synchronisation, and a cluster task whose output is independently checked.

In the design, the network's own evolutionary algorithms attack it continuously. When an attack succeeds, a regeneration mechanism fixes the weakness, tests the fix on the testing network and propagates it, so the network hardens against failures nobody predicted. A node that returns faults is audited, a node that attacks is investigated and can be removed, and nodes without verified identity need extra validation points before they contribute.

For federated learning, the design keeps each experience where it was lived. What circulates, with authorisation, are unnamed patterns: reasoning, symbols, ontologies and public knowledge, never the biography. The system sees only the sum of many contributions, never one person's, and each pattern is weighed by what it would let someone guess, since even an unnamed pattern can point to someone; a pattern gains weight when it holds in independent contexts. These protections are checked in results, not only in the design, since exchanging model updates alone does not establish anonymity.

## Participation and sources

This repository develops a proposal through public documentation and review. Read the [contribution guide](https://github.com/draykerdk/.github/blob/master/CONTRIBUTING.md) and [current governance](https://github.com/draykerdk/.github/blob/master/GOVERNANCE.md), or find a bounded contribution on the [open-functions board](https://drayker.org/fn/).

Part of [Drayker](https://drayker.org). Content licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
