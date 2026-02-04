---
slug: dudect
title: dudect
description: "Dude, is my code constant time?"
year: 2017
target: Binary
technique: Statistical
guarantees: "no"
available: true
repo: https://github.com/oreparaz/dudect
papers:
 - name: "Dude, is my code constant time?"
   link: https://doi.org/10.23919/DATE.2017.7927267
---

![GitHub last commit](https://img.shields.io/github/last-commit/oreparaz/dudect)![GitHub contributors](https://img.shields.io/github/contributors/oreparaz/dudect)![GitHub Repo stars](https://img.shields.io/github/stars/oreparaz/dudect)

## Description

**dudect** is a dynamic tool that uses leakage assessment techniques from physical (power and EM) side-channel analysis, namely test-vector leakage assessment (TVLA). It first runs the target using two classes of secret input data with varying public input data and measures the duration of execution for each run. It then applies a Welch t-test for equality of means to the two distributions of the duration of execution for the two classes, and if the t-test comes back larger than some preset threshold, leakage is reported. This is analogous to how leakage assessment is used in power side-channel attacks, in that instead of comparing distributions of power consumption at points during the execution of the target, the runtime distributions are compared.

## Abstract

This paper introduces dudect: a tool to assess whether a piece of code runs in constant time or not on a given platform. We base our approach on leakage detection techniques, resulting in a very compact, easy to use and easy to maintain tool. Our methodology fits in around 300 lines of C and runs on the target platform. The approach is substantially different from previous solutions. Contrary to others, our solution requires no modeling of hardware behavior. Our solution can be used in black-box testing, yet benefits from implementation details if available. We show the effectiveness of our approach by detecting several variable-time cryptographic implementations. We place a prototype implementation of dudect in the public domain.
