---
layout: top_project
name: MAPS
slug: maps
description: Machine learning and Algorithms for Practical Security
people:
  - slug: teo
  - slug: aashish
  - slug: kareem
  - slug: ivica
display_categories: [ML Privacy, ML Robustness, ML Applications]
---

<h3>Research Overview</h3>
---

Security of machine learning (ML) systems is a relatively new topic in computer security with many concerns highlighted in the last decade through attack procedures and defenses.
However, fundamental questions in this space such as distinguishing between the intended vs. unintended (malicious) behavior or developing algorithms to test and verify desirable properties with guarantees remain open.
This is because, among others, ML models are learned through complex stochastic procedures from data coming from an unknown distribution, we often do not have ground truth of what they should be learning, and it is difficult to perfectly capture the highly non-linear and high-dimensional internals of the models.
On top of all this, the adversaries can be adaptive or employ their own ML strategies.

It is thus imperative to analyze security in a *systematic* way when considering machine learning systems in *practical* setups.

The **MAPS** (**M**achine learning and **A**lgorithms for **P**ractical **S**ecurity) project aims to design and develop (1) novel machine learning algorithms that come with strong security & privacy guarantees and (2) rigorous analysis of security properties of off-the-shelf machine learning systems.

At a technical level, we work on three directions:
1. **Developing Algorithms with Guarantees**
  - Learning in federated setups enables more control over their data for users. Despite this advantage, it is difficult to ensure that the privacy of users is preserved with strong guarantees while learning something useful from the users' data. In this line of works, we focus on the question if there exist algorithms that show a good trade-off between utility and privacy. We show several key technical contributions that build on top of the principled framework of **differential privacy** to answer positively. Relevant projects are in [ML Privacy].

2. **Verifying Properties of Machine Learning**
- How can we know if a ML model is robust, biased or susceptible to a poisoning attack? Can we derive statistically sound answers to such questions? We show that we can do so with two approaches for several security applications. What about properties of the training process (i.e., stochastic gradient descent) such as being able to obtain the same model update from two different sets of samples?  
3. **Learning Algorithms for Programs**
- Can we learn from observations rules that are useful for security analysis such as taint analysis rules? In this line of work, we use ML to power analyses useful for security analysis.

---