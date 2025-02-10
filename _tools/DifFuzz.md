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
 - name: "Automatic Repair of Java Code with Timing Side-Channel Vulnerabilities"
   link: https://doi.org/10.1109/ASEW52652.2021.00014
---

![GitHub last commit](https://img.shields.io/github/last-commit/isstac/diffuzz)![GitHub contributors](https://img.shields.io/github/contributors/isstac/diffuzz)![GitHub Repo stars](https://img.shields.io/github/stars/isstac/diffuzz)

There are two tools merged here:
 - [DifFuzz](https://github.com/isstac/diffuzz) that checks for timing leaks, and
 - [DifFuzzAR](https://github.com/RuiDTLima/DifFuzzAR) that fixes timing leaks.

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


### DifFuzzAR

Vulnerability detection and repair is a demanding and expensive part of
the software development process. As such, there has been an effort to
develop new and better ways to automatically detect and repair vulnerabilities.
DifFuzz is a state-of-the-art tool for automatic detection of timing
side-channel vulnerabilities, a type of vulnerability that is particularly
difficult to detect and correct. Despite recent progress made with tools
such as DifFuzz, work on tools capable of automatically repairing timing
side-channel vulnerabilities is scarce. In this paper, we propose DifFuzzAR,
a new tool for automatic repair of timing side-channel vulnerabilities in
Java code. The tool works in conjunction with DifFuzz and it is able to repair
56% of the vulnerabilities identified in DifFuzz's dataset. The results show
that the tool can indeed automatically correct timing side-channel vulnerabilities,
being more effective with those that are control-flow based.
