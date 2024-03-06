---
slug: skkjh18
title: SKKJH18
description: "Unveiling Hardware-based Data Prefetcher, a Hidden Source of Information Leakage"
year: 2018
target: Binary
technique: Statistical
guarantees: "no"
available: false
papers:
 - name: "Unveiling Hardware-based Data Prefetcher, a Hidden Source of Information Leakage"
   link: https://dl.acm.org/doi/10.1145/3243734.3243736
---

## Abstract

Data prefetching is a hardware-based optimization mechanism used in most of the modern
microprocessors. It fetches data to the cache before it is needed. In this paper, we
present a novel microarchitectural attack that exploits the prefetching mechanism. Our
attack targets Instruction pointer (IP)-based stride prefetching in Intel processors.
Stride prefetcher detects memory access patterns with a regular stride, which are likely
to be found in lookup table-based cryptographic implementations. By monitoring the
prefetching activities near the lookup table, attackers can extract sensitive information
such as secret keys from victim applications. This kind of leakage from prefetching has
never been considered in the design of constant time algorithm to prevent side-channel
attacks. We show the potential of the proposed attack by applying it against the Elliptic
Curve Diffie-Hellman (ECDH) algorithm built upon the latest version of OpenSSL library.
To the best of our knowledge, this is the first microarchitectural side-channel attack
exploiting the hardware prefetching of modern microprocessors.
