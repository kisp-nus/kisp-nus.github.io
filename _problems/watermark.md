---
layout: page
title: "Watermarking AI"
weight: 2
tag: "watermark"
after-content: publications-rel.html
---

How can one verify whether a data sample (text/image/sound) comes from a generative AI model? One way is to insert "watermarks" into AI-generated content at source, which can later be verified using a secret key by the end user’s device. Doing so has many security applications:
Limiting nefarious use of public ML models, protecting intellectual property, combating spread of
misinformation, and more. Watermarking of AI-generated content has been extensively explored in
the last few years, but a perfect watermarking scheme remains elusive. A key practical requirement
for watermarking is that it should not impact any downstream functionality or be easily detectable. In
other words, we want watermarking to be imperceptible to humans and invisible to all downstream
processing, including determined adversaries that want to detect the presence of a watermark. In our
recent work [1], we provide a novel approach to watermarking high-dimensional distributions, such that
telling apart watermarked from unwatermakred data can be cryptographically hard. 

Specifically, we show how to do this for image distributions generated from modern generative models based on diffusion processes, by embedding secrets along random directions in the latent input vector space. We then show a reduction from a lattice problem (CLWE) to that of detecting our watermarks. The former is cryptographically hard to break under certain parameter choices. Thus, our construction has quantifiable security against all possible attacks, which contrasts many recent schemes that are detectable with new steganographic attacks. Our watermark is also robust to minor perturbations such as image compression.