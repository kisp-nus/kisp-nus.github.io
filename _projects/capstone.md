---
layout: top_project
name: CAPSTONE
slug: capstone
description: Capability-based Foundations for Trustless Secure Memory Access
people:
  - slug: jason
display_categories: [TEEs, Memory Safety, OS Security]
---

The traditional hardware-based approach to security problems such as memory safety and
memory isolation has been individual _ad hoc_ architectural extensions.
This has created a fragmented landscape: the protection mechanisms are not universally available,
and the interactions between different extensions are unclear or confusing.
In part, this problem is due to the traditional virtual-memory-based access control model,
which imposes a rigid central and hierarchical trust model and coarse protection granularity.

The **CAPSTONE** project aims to design a computer architecture expressive enough to
cover multiple security goals with a single clean set of primitives.
We take an approach based on _capability-based security_, where the hardware
enforces security policies that are not controlled by a central trusted authority, but
collectively defined by different software components.

Topics that this project explores include:

1. **Isolation with zero software TCB (Trusted Computing Base):**
In general, compared with hardware, software is complex, buggy and easy to compromise.
The recent surge in public interests in trusted execution environments (TEEs)
and confidential computing has recognised this issue, and reducing the software TCB
has been a pressing need in various contexts ranging from cloud services to edge devices.
Prior work has attempted to extend existing virtual-memory-based architectures for such
a goal.
In CAPSTONE, we seek to provide a more principled capability-based approach.

1. **Unifying memory isolation and memory safety:**
Memory isolation and memory safety have traditionally been treated separately and
supported using disjoint sets of mechanisms.
Capabilities, which bind access permissions to resource references, provide a basis for unifying those two goals.
We seek to answer the question of how isolation semantics maps to program semantics
so both can be supported with a single mechanism, despite the apparently different threat models in the two
use cases.
In particular, we are interested in enforcing temporal memory safety and higher-level safety properties
(e.g., data race prevention) with capabilities.


1. **Bridging capabilities and traditional virtual-memory-based systems:**
Capability-based systems are very different from the ubiquitous virtual-memory-based systems,
and a naive design either compromises the strengths of capabilities, or requires
extensive changes in software.
We aim to design a capability-based system that interoperates well with existing software stacks while
maintaining the advantages of capabilities.

1. **Efficient implementation of capability-based architectures:**
We also explore the techniques to efficiently implement such next-generation architectures in hardware.

For more information, please visit the dedicate [CAPSTONE website](https://capstone.kisp-lab.org/).
