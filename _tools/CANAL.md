---
slug: canal
title: CANAL
description: "CANAL: a cache timing analysis framework via LLVM transformation"
year: 2018
target: LLVM IR
technique: Formal
guarantees: sound
available: true
repo: https://github.com/canalcache/canal
papers:
 - name: "CANAL: a cache timing analysis framework via LLVM transformation"
   link: https://dl.acm.org/doi/10.1145/3238147.3240485
---

![GitHub last commit](https://img.shields.io/github/last-commit/canalcache/canal)![GitHub contributors](https://img.shields.io/github/contributors/canalcache/canal)![GitHub Repo stars](https://img.shields.io/github/stars/canalcache/canal)

## Abstract

A unified modeling framework for non-functional properties of a program is
essential for research in software analysis and verification, since it reduces
burdens on individual researchers to implement new approaches and compare
existing approaches. We present CANAL, a framework that models the cache
behaviors of a program by transforming its intermediate representation in the
LLVM compiler. CANAL inserts auxiliary variables and instructions over these
variables, to allow standard verification tools to handle a new class of cache
related properties, e.g., for computing the worst-case execution time and
detecting side-channel leaks.

We demonstrate the effectiveness of using three verification tools: KLEE,
SMACK and Crab-llvm. We confirm the accuracy of our cache model by comparing
with CPU cycle-accurate simulation results of GEM5.

CANAL is available on [GitHub](https://github.com/canalcache/canal) and
[YouTube](https://youtu.be/JDou3F1j2nY).
