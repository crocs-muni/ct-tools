---
slug: diffuzz
title: DifFuzz
description: "DifFuzz: Differential Fuzzing for Side-Channel Analysis"
year: 2019
target: Java
technique: Dynamic
guarantees: "no"
available: true
repo: https://github.com/isstac/diffuzz
papers:
 - name: "DifFuzz: Differential Fuzzing for Side-Channel Analysis"
   link: https://doi.org/10.1109/ICSE.2019.00034
---

![GitHub last commit](https://img.shields.io/github/last-commit/isstac/diffuzz)![GitHub contributors](https://img.shields.io/github/contributors/isstac/diffuzz)![GitHub Repo stars](https://img.shields.io/github/stars/isstac/diffuzz)


## Abstract

Side-channel attacks allow an adversary to uncover secret program
data by observing the behavior of a program with respect to a resource,
such as execution time, consumed memory or response size. Side-channel
vulnerabilities are difficult to reason about as they involve analyzing
the correlations between resource usage over multiple program paths. We
present DifFuzz, a fuzzing-based approach for detecting side-channel
vulnerabilities related to time and space. DifFuzz automatically detects
these vulnerabilities by analyzing two versions of the program and using
resource-guided heuristics to find inputs that maximize the difference
in resource consumption between secret-dependent paths. The methodology
of DifFuzz is general and can be applied to programs written in any
language. For this paper, we present an implementation that targets
analysis of Java programs, and uses and extends the Kelinci and AFL
fuzzers. We evaluate DifFuzz on a large number of Java programs and
demonstrate that it can reveal unknown side-channel vulnerabilities in
popular applications. We also show that DifFuzz compares favorably against
Blazer and Themis, two state-of-the-art analysis tools for finding
side-channels in Java programs.
