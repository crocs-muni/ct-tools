---
slug: lmtest
title: LmTest
description: "Testing side-channel security of cryptographic implementations against future microarchitectures"
year: 2024
target: Binary
technique: Dynamic
guarantees: "sound with restrictions"
available: true
site: https://github.com/hw-sw-contracts/leakage-model-testing
papers:
 - name: "Testing side-channel security of cryptographic implementations against future microarchitectures"
   link: https://doi.org/10.1145/3658644.3670319
---

![GitHub last commit](https://img.shields.io/github/last-commit/hw-sw-contracts/leakage-model-testing)![GitHub contributors](https://img.shields.io/github/contributors/hw-sw-contracts/leakage-model-testing)![GitHub Repo stars](https://img.shields.io/github/stars/hw-sw-contracts/leakage-model-testing)

## Abstract

How will future microarchitectures impact the security of existing cryptographic implementations?
As we cannot keep reducing the size of transistors, chip vendors have started developing new
microarchitectural optimizations to speed up computation. A recent study (Sanchez Vicarte et al., ISCA 2021)
suggests that these optimizations might open the Pandora's box of microarchitectural attacks.
However, there is little guidance on how to evaluate the security impact of future optimization
proposals. To help chip vendors explore the impact of microarchitectural optimizations on
cryptographic implementations, we develop (i) an expressive domain-specific language, called
LmSpec, that allows them to specify the leakage model for the given optimization and (ii) a
testing framework, called LmTest, to automatically detect leaks under the specified leakage
model within the given implementation. Using this framework, we conduct an empirical study
of 18 proposed microarchitectural optimizations on 25 implementations of eight cryptographic
primitives in five popular libraries. We find that every implementation would contain
secret-dependent leaks, sometimes sufficient to recover a victim's secret key, if these
optimizations were realized. Ironically, some leaks are possible only because of coding idioms
used to prevent leaks under the standard constant-time model.
