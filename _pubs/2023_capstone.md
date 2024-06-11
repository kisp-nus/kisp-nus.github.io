---
title: "Capstone: A Capability-based Foundation for Trustless Secure Memory Access"
authors:
 - slug: jason
 - name: Conrad Watt
   url: https://www.cl.cam.ac.uk/~caw77/
 - name: Aditya Badole
 - name: Trevor E. Carlson
   url: https://www.comp.nus.edu.sg/~tcarlson/
 - name: Prateek Saxena
   url: https://www.comp.nus.edu.sg/~prateeks/

category: [OS Security]
publication: USENIX Security
year: 2023
pub_url: http://www.comp.nus.edu.sg/~prateeks/papers/Capstone.pdf
abstract: "Capability-based memory isolation is a promising new architectural primitive. Software can access low-level memory only via capability handles rather than raw pointers, which provides a natural interface to enforce security restrictions. Existing architectural capability designs such as CHERI provide spatial safety, but fail to extend to other memory models that security-sensitive software designs may desire. In this paper, we propose Capstone, a more expressive architectural capability design that supports multiple existing memory isolation models in a trustless setup, i.e., without relying on trusted software components. We show how Capstone is well-suited for environments where privilege boundaries are fluid (dynamically extensible), memory sharing/delegation are desired both temporally and spatially, and where such needs are to be balanced with availability concerns. Capstone can also be implemented efficiently. We present an implementation sketch and through evaluation show that its overhead is below 50% in common use cases. We also prototype a functional emulator for Capstone and use it to demonstrate the runnable implementations of six real-world memory models without trusted software components: three types of enclave-based TEEs, a thread scheduler, a memory allocator, and Rust-style memory safety—all within the interface of Capstone."
---