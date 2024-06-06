---
title: "Scalable Quantitative Verification For Deep Neural Networks"
authors:
 - slug: teo
 - name: Zheng Leong Chua
   url: 
 - name: Kuldeep S. Meel
   url: https://www.cs.toronto.edu/~meel/
 - name: Prateek Saxena
   url: https://www.comp.nus.edu.sg/~prateeks/

publication: ICSE
year: 2021
pub_url: https://www.comp.nus.edu.sg/~prateeks/papers/Provero-icse21.pdf
category: [ML Robustness]
img: /images/projects/provero.png
preview: /images/projects/provero.png
github: https://github.com/teobaluta/provero
abstract: "Despite the functional success of deep neural networks (DNNs), their trustworthiness remains a crucial open challenge. To address this challenge, both testing and verification techniques have been proposed. But these existing techniques provide either scalability to large networks or formal guarantees, not both. In this paper, we propose a scalable quantitative verification framework for deep neural networks, i.e., a test-driven approach that comes with formal guarantees that a desired probabilistic property is satisfied. Our technique performs enough tests until soundness of a formal probabilistic property can be proven. It can be used to certify properties of both deterministic and randomized DNNs. We implement our approach in a tool called PROVERO and apply it in the context of certifying adversarial robustness of DNNs. In this context, we first show a new attack-agnostic measure of robustness which offers an alternative to purely attack-based methodology of evaluating robustness being reported today. Second, PROVERO provides certificates of robustness for large DNNs, where existing state-of-the-art verification tools fail to produce conclusive results. Our work paves the way forward for verifying properties of distributions captured by real-world deep neural networks, with provable guarantees, even where testers only have black-box access to the neural network."
video: "https://www.youtube.com/embed/Hc-Xjdf2LNc"
---
