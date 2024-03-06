---
slug: cacheaudit2
title: CacheAudit2
description: "Rigorous analysis of software countermeasures against cache attacks"
year: 2017
target: Binary
technique: Formal
guarantees: other
available: true
repo: https://github.com/cacheaudit/cacheaudit/tree/fine-trace
site: https://software.imdea.org/projects/cacheaudit/memory-trace/
papers:
 - name: "Rigorous analysis of software countermeasures against cache attacks"
   link: https://dl.acm.org/doi/10.1145/3062341.3062388
---

## Abstract

CPU caches introduce variations into the execution time of programs that can be 
xploited by adversaries to recover private information about users or cryptographic keys.

Establishing the security of countermeasures against this threat often requires
intricate reasoning about the interactions of program code, memory layout, and
hardware architecture and has so far only been done for restricted cases.

In this paper we devise novel techniques that provide support for bit-level and
arithmetic reasoning about memory accesses in the presence of dynamic memory
allocation. These techniques enable us to perform the first rigorous analysis of
widely deployed software countermeasures against cache attacks on modular exponentiation,
based on executable code.
