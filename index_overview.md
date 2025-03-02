Our research directions are summarized in the following themes.

For more information about our work, please visit our [projects](#projects), and [recent publications](#publications).

### Theme 1: Capstone

The traditional hardware-based approach to security problems such as memory safety and
memory isolation has been individual _ad hoc_ architectural extensions.
This has created a fragmented landscape: the protection mechanisms are not universally available,
and the interactions between different extensions are unclear or confusing.
In part, this problem is due to the traditional virtual-memory-based access control model,
which imposes a rigid central and hierarchical trust model and coarse protection granularity.

The [**CAPSTONE**](https://capstone.kisp-lab.org) project aims to design a computer architecture expressive enough to
cover multiple security goals with a single clean set of primitives.
We take an approach based on _capability-based security_, where the hardware
enforces security policies that are not controlled by a central trusted authority, but
collectively defined by different software components.

### Theme 2: Automated Program Translation

Translating programs between different programming languages is essential for various reasons, such as achieving memory safety, adapting to new ecosystems, and migrating legacy code. Our project aims to automate this process while achieving the following three goals:

(a) **Correctness**: The translated code should maintain the same or equivalent functionality. \\
(b) **Scalability**: The translator should handle large, real-world codebases effectively. \\
(c) **Maintainability**: The output should be easy to read, modify, and maintain. 

Achieving these goals is challenging due to differences in coding conventions, type systems, external APIs, and language-specific constructs. Our long-term mission is to overcome these challenges and develop automated translation techniques that work effectively for real-world programs.

We are translating C to Rust for improved memory safety and have also explored translating Python to JavaScript. For more information, please visit the [project website](https://kisp.comp.nus.edu.sg/projects/apt).

### Theme 3: Machine learning and Algorithms for Practical Security

Machine learning tools have become widely accessible over the past decade, but their security remains an ongoing challenge. OWASP has summarized the [‘Top 10’ practical problems in machine learning (ML) security](https://owasp.org/www-project-machine-learning-security-top-10/). However, research in each sub-problem is an ongoing race between attacks and defenses. Does this cat-and-mouse race have an end? Are there optimal defense strategies such that all attacks bounded by certain costs become impractical? 

The **MAPS** project aims to answer these questions in a principled manner by identifying the inherent limitations of current schemes and drawing from cryptographically hard problems to establish robust security guarantees. Specifically, we study four main areas: 1) the practical impact of data poisoning attacks in federated settings and the computational limitations of robust aggregation defenses against such attacks; 2) watermarking schemes for AI-generated content that is provably secure against all possible attacks; 3) defenses against model inversion attacks, including a cryptographic primitive that prevents the recovery of sensitive inputs; 4) we investigate verification of desired properties of ML systems and practical differential privacy in federated networks and GNNs. 