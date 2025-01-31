---
title: "Memory Safety"
description: "Unifying memory isolation and memory safety"
problem_statement: 
contribution: 
---

Memory isolation and memory safety have traditionally been treated separately and
supported using disjoint sets of mechanisms.
Capabilities, which bind access permissions to resource references, provide a basis for unifying those two goals.
We seek to answer the question of how isolation semantics maps to program semantics
so both can be supported with a single mechanism, despite the apparently different threat models in the two
use cases.
In particular, we are interested in enforcing temporal memory safety and higher-level safety properties
(e.g., data race prevention) with capabilities.