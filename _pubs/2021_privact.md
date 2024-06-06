---
title: "Private Hierarchical Clustering in Federated Networks"
authors:
 - slug: aashish
 - slug: teo
 - name: Prateek Saxena
   url: https://www.comp.nus.edu.sg/~prateeks/

publication: CCS
year: 2021
pub_url: https://www.comp.nus.edu.sg/~prateeks/papers/Privact.pdf
category: [ML Privacy]
abstract: "Analyzing structural properties of social networks, such as identifying their clusters or finding their most central nodes, has many applications. However, these applications are not supported by federated social networks that allow users to store their social links locally on their end devices. In the federated regime, users want access to personalized services while also keeping their social links private. In this paper, we take a step towards enabling analytics on federated networks with differential privacy guarantees about protecting the user links or contacts in the network. Specifically, we present the first work to compute hierarchical cluster trees using local differential privacy. Our algorithms for computing them are novel and come with theoretical bounds on the quality of the trees learned. The private hierarchical cluster trees enable a service provider to query the community structure around a user at various granularities without the users having to share their raw contacts with the provider. We demonstrate the utility of such queries by redesigning the state-of-the-art social recommendation algorithms for the federated setup. Our recommendation algorithms significantly outperform the baselines which do not use social contacts and are on par with the non-private algorithms that use contacts."
---