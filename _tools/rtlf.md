---
slug: rtlf
title: RTLF
description: "R-Time-Leak-Finder"
year: 2024
target: Binary
technique: Statistical
guarantees: "no"
available: true
repo: https://github.com/tls-attacker/RTLF
papers:
 - name: "With Great Power Come Great Side Channels: Statistical Timing Side-Channel Analyses with Bounded Type-1 Errors"
   link: https://www.usenix.org/conference/usenixsecurity24/presentation/dunsche
---

![GitHub last commit](https://img.shields.io/github/last-commit/tls-attacker/RTLF)![GitHub contributors](https://img.shields.io/github/contributors/tls-attacker/RTLF)![GitHub Repo stars](https://img.shields.io/github/stars/tls-attacker/RTLF)

## Description

RTLF is a new tool to statistically evaluate timing measurements with a type-1 error bounded by an input parameter 
α. Details on RTLF can be found on our paper, which we published at USENIX Security 2024.

Please note: RTLF is a research tool intended for developers, pentesters, administrators and researchers. There is no GUI.

## Abstract

Constant-time implementations are essential to guarantee the security of secret-key operations.
According to Jancar et al. [[42]](https://eprint.iacr.org/2021/1650.pdf), most cryptographic developers do not use statistical tests to
evaluate their implementations for timing side-channel vulnerabilities. One of the main reasons
is their high unreliability due to potential false positives caused by noisy data. In this work,
we address this issue and present an improved statistical evaluation methodology with a
controlled type-1 error (α) that restricts false positives independently of the noise distribution.
Simultaneously, we guarantee statistical power with increasing sample size. With the bounded
type-1 error, the user can perform trade-offs between false positives and the size of the side
channels they wish to detect. We achieve this by employing an empirical bootstrap that creates
a decision rule based on the measured data.

We implement this approach in an open-source tool called RTLF and compare it with three different
competitors: Mona, dudect, and tlsfuzzer. We further compare our results to the t-test, a commonly
used statistical test for side-channel analysis. To show the applicability of our tool in real
cryptographic network scenarios, we performed a quantitative analysis with local timing measurements
for CBC Padding Oracle attacks, Bleichenbacher's attack, and the Lucky13 attack in 823 available
versions of eleven TLS libraries. Additionally, we performed a qualitative analysis of the most
recent version ofeach library. We find that most libraries were long-time vulnerable to at least
one of the considered attacks, with side channels big enough likely to be exploitable in a LAN setting.
Through the qualitative analysis based on the results of RTLF, we identified seven vulnerabilities
in recent versions.
