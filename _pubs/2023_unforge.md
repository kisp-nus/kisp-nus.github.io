---
title: "Unforgeability in Stochastic Gradient Descent"
authors:
 - slug: teo
 - slug: ivica
 - name: Racchit Jain
   url: 
 - name: Divesh Aggarwal
   url: https://sites.google.com/site/diveshhomepage
 - name: Prateek Saxena
   url: https://www.comp.nus.edu.sg/~prateeks/

publication: CCS
year: 2023
pub_url: https://dl.acm.org/doi/10.1145/3576915.3623093
github: "https://github.com/teobaluta/unforgeability-SGD"
category: Others
abstract: "Stochastic Gradient Descent (SGD) is a popular training algorithm, a cornerstone of modern machine learning systems. Several security applications benefit from determining if SGD executions are
forgeable, i.e., whether the model parameters seen at a given step
are obtainable by more than one distinct set of data samples. In
this paper, we present the first attempt at proving impossibility of
such forgery. We furnish a set of conditions, which are efficiently
checkable on concrete checkpoints seen during training runs, under
which checkpoints are provably unforgeable at that step. Our experiments show that the conditions are somewhat mild and hence
always satisfied at checkpoints sampled in our experiments. Our
results sharply contrast prior findings at a high level: We show that
checkpoints we find to be provably unforgeable have been deemed
to be forgeable using the same methodology and experimental setup
suggested in prior work. This discrepancy arises because of unspecified subtleties in definitions. We experimentally confirm that the
distinction matters, i.e., small errors amplify during training to produce significantly observable difference in final models trained. We
hope our results serve as a cautionary note on the role of algebraic
precision in forgery definitions and related security arguments."
desc: "We show that execution traces of SGD, under mild conditions, can be unforgeable."
---