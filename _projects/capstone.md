---
layout: top_project
name: CAPSTONE
slug: capstone
description: Capability-based Foundations for Trustless Secure Memory Access
people:
  - slug: jason
display_categories: [TEEs, Memory Safety, OS Security]
atomic_problems: [TEEs, Memory Safety, OS Security,TBD]
tldr: The **CAPSTONE** project aims to design a computer architecture expressive enough to cover multiple security goals with a single clean set of primitives. We take an approach based on _capability-based security_, where the hardware enforces security policies that are not controlled by a central trusted authority, but collectively defined by different software components.
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

Topics that this project explores include: Isolation with zero software TCB (Trusted Computing Base), Unifying memory isolation and memory safety, Bridging capabilities and traditional virtual-memory-based systems, Efficient implementation of capability-based architectures. 


For more information, please visit the dedicate [CAPSTONE website](https://capstone.kisp-lab.org/).
