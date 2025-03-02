---
layout: main_project
title: MAPS
slug: maps
description: Machine learning and Algorithms for Practical Security
people:
  - slug: teo
  - slug: aashish
  - slug: kareem
  - slug: ivica
  - slug: louise
  - slug: mallika
atomic_problems:
  - ML Robustness
  - Watermark
  - ML Inversion
  - ML Privacy
  - Others
---

Machine learning tools have become widely accessible over the past decade, but their security remains an ongoing
challenge. OWASP has summarized the [‘Top 10’ practical problems in machine learning (ML)
security](https://owasp.org/www-project-machine-learning-security-top-10/). However, research in each sub-problem is
an
ongoing race between attacks and defenses. Does this cat-and-mouse race have an end? Are there optimal defense
strategies such that all attacks bounded by certain costs become impractical?

The **MAPS** project aims to answer these questions in a principled manner by identifying the inherent limitations
of
current schemes and drawing from cryptographically hard problems to establish robust security guarantees.
Specifically,
we study four main areas: 1) the practical impact of data poisoning attacks in federated settings and the
computational
limitations of robust aggregation defenses against such attacks; 2) watermarking schemes for AI-generated content
that
is provably secure against all possible attacks; 3) defenses against model inversion attacks, including a
cryptographic
primitive that prevents the recovery of sensitive inputs; 4) we investigate verification of desired properties of ML
systems and practical differential privacy in federated networks and GNNs.

---