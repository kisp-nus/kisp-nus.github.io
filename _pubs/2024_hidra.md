---
title: "Attacking Byzantine Robust Aggregation in High Dimensions"
authors:
 - name: Sarthak Choudhary
   url: 
 - slug: aashish
 - name: Prateek Saxena
   url: https://www.comp.nus.edu.sg/~prateeks/

publication: S&P
year: 2024
pub_url: https://arxiv.org/pdf/2312.14461
category: [ML Robustness]
abstract: "Training modern neural networks or models typically requires averaging over a sample of high-dimensional vectors. Poisoning attacks can skew or bias the average vectors used to train the model, forcing the model to learn specific patterns or avoid learning anything useful. Byzantine robust aggregation is a principled algorithmic defense against such biasing. Robust aggregators can bound the maximum bias in computing centrality statistics, such as mean, even when some fraction of inputs are arbitrarily corrupted. Designing such aggregators is challenging when dealing with high dimensions. However, the first polynomial-time algorithms with strong theoretical bounds on the bias have recently been proposed. Their bounds are independent of the number of dimensions, promising a conceptual limit on the power of poisoning attacks in their ongoing arms race against defenses.
In this paper, we show a new attack called HIDRA on practical realization of strong defenses which subverts their claim of dimension-independent bias. HIDRA highlights a novel computational bottleneck that has not been a concern of prior information-theoretic analysis. Our experimental evaluation shows that our attacks almost completely destroy the model performance, whereas existing attacks with the same goal fail to have much effect. Our findings leave the arms race between poisoning attacks and provable defenses wide open."
---