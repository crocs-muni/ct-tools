---
slug: easywalk-ci
title: EasyWalk-CI
description: "Semi-Automated and Easily Interpretable Side-Channel Analysis for Modern JavaScript"
year: 2024
target: Binary
technique: Dynamic
guarantees: "sound with restrictions"
available: true
repo: https://github.com/EasyWalk-CI-project/EasyWalk
papers:
 - name: "Semi-Automated and Easily Interpretable Side-Channel Analysis for Modern JavaScript"
   link: https://hal.science/hal-04652991/
---

![GitHub last commit](https://img.shields.io/github/last-commit/EasyWalk-CI-project/EasyWalk)![GitHub contributors](https://img.shields.io/github/contributors/EasyWalk-CI-project/EasyWalk)![GitHub Repo stars](https://img.shields.io/github/stars/EasyWalk-CI-project/EasyWalk)

## Abstract

Over the years, developers have become increasingly reliant on web technologies to build their applications,
raising concerns about side-channel attacks, especially on cryptographic libraries. Despite the efforts of
researchers to ensure constant-time security by proposing tools and methods to find vulnerabilities,
challenges remain due to inadequate tools and integration issues in development processes.

We tackle the main limitations of state-of-the-art detection tools. While Microwalk is the first and,
to the best of our knowledge, only tool to find side-channel vulnerabilities in JavaScript libraries,
the instrumentation framework it relies on does not support modern JavaScript features. Moreover,
and common to most state-of-the-art detection tools not aimed at JavaScript, writing tests is a
tedious process due to the complexity of libraries, the lack of information about test coverage,
and the rudimentary interpretability of the report. Furthermore, recent studies show that developers
do not use these tools due to compatibility issues, poor usability, and a lack of integration into workflows.

We extend Microwalk in several directions. First, we design a generic AST-level tracing technique that is
tailored to source-based dynamic side-channel leakage analysis, providing support for the latest language
features. Second, we bring semi-automation to Microwalk analysis templates, considerably reducing the manual
effort necessary to integrate side-channel analyses into development workflows. Third, we are the first to
combine leakage reporting with coverage visualization. We evaluate the new toolchain on a set of cryptographic
libraries and show that it can quickly and comprehensively uncover more vulnerabilities while writing tests
with half as many lines of code as the previous Microwalk version. By open sourcing our new tracer and
analysis template, we hope to increase the adoption of automated side-channel leakage analyses in
cryptographic library development.
