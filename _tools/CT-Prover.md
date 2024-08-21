---
slug: ct-prover
title: CT-Prover
description: "Towards Efficient Verification of Constant-Time Cryptographic Implementations"
year: 2024
target: LLVM IR
technique: Formal
guarantees: sound
available: true
repo: https://github.com/S3L-official/CT_Prover
papers:
 - name: "Towards Efficient Verification of Constant-Time Cryptographic Implementations"
   link: https://dl.acm.org/doi/10.1145/3643772
---

![GitHub last commit](https://img.shields.io/github/last-commit/S3L-official/CT_Prover)![GitHub contributors](https://img.shields.io/github/contributors/S3L-official/CT_Prover)![GitHub Repo stars](https://img.shields.io/github/stars/S3L-official/CT_Prover)

## Abstract

Timing side-channel attacks exploit secret-dependent execution time to fully or partially
recover secrets of cryptographic implementations, posing a severe threat to software security.
Constant-time programming discipline is an effective software-based countermeasure against
timing side-channel attacks, but developing constant-time implementations turns out to be
challenging and error-prone. Current verification approaches/tools suffer from scalability
and precision issues when applied to production software in practice. In this paper, we put
forward practical verification approaches based on a novel synergy of taint analysis and
safety verification of self-composed programs. Specifically, we first use an IFDS-based
lightweight taint analysis to prove that a large number of potential (timing) side-channel
sources do not actually leak secrets. We then resort to a precise taint analysis and a safety
verification approach to determine whether the remaining potential side-channel sources can
actually leak secrets. These include novel constructions of taint-directed semi-cross-product
of the original program and its Boolean abstraction, and a taint-directed self-composition of
the program. Our approach is implemented as a cross-platform and fully automated tool **CT-Prover**.
The experiments confirm its efficiency and effectiveness in verifying real-world benchmarks
from modern cryptographic and SSL/TLS libraries. In particular, **CT-Prover** identify new,
confirmed vulnerabilities of open-source SSL libraries (e.g., Mbed SSL, BearSSL) and significantly
outperforms the state-of-the-art tools.
