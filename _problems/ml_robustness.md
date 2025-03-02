---
title: "ML Robustness"
description: "Poisoning Attacks & Robust Aggregation"
problem_statement: "Give theoretical guarantees for ML robustness"
contribution: "We designed a HiDra attack to show current robust aggregators are impractical. And ..."
---

Data poisoning is an integrity attack on ML model training, wherein data certain corrupted samples force the trained model to surreptitiously contain backdoors,
misclassify certain inputs, and more. We were the first to show the practical impact of these attacks in
federated learning in 2016 [2]. A generic defense for various poisoning attacks is based on bounding
the adversarial bias introduced when computing a mean of vectors, assuming a small fraction of which
may be arbitrarily corrupted. This problem is called the Byzantine robust aggregation. It accurately
captures the averaging of gradient vectors when training with the de-facto stochastic gradient descent
mechanism. In the last decade, algorithmic advances in Byzantine robust aggregation have achieved
optimal limits on the bias, i.e., they can severely limit the maximum skew the adversary can induce
on the learnt model at each training step by filtering outliers [12]. In our recent work [3], however, we
show that these optimal solutions have intractable running time for practical ML models. Specifically,
we show that the problem of robust aggregation reduces from that of determining the *largest eigenvector*
of the sample covariance. The best deterministic algorithms for the latter have cubic running time in the
dimensions, which is intractable. We are working on a randomized defense that is quasi-linear in the
dimensions and the training dataset size, with the hope of having the first practical generic defense.
