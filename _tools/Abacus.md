---
slug: abacus
title: Abacus
description: "Abacus: A Tool for Precise Side-Channel Analysis"
year: 2021
target: Binary
technique: Dynamic
guarantees: "sound with restrictions"
available: true
repo: https://github.com/s3team/Abacus
papers:
 - name: "Abacus: A Tool for Precise Side-Channel Analysis"
   link: https://doi.org/10.1109/ICSE43902.2021.00078
 - name: "Abacus: A Tool for Precise Side-Channel Analysis (companion tutorial)"
   link: https://doi.org/10.1109/ICSE-Companion52605.2021.00110
---

![GitHub last commit](https://img.shields.io/github/last-commit/s3team/Abacus)![GitHub contributors](https://img.shields.io/github/contributors/s3team/Abacus)![GitHub Repo stars](https://img.shields.io/github/stars/s3team/Abacus)

## Abstract

Side-channel vulnerabilities can leak sensitive information unconsciously.
In this paper, we introduce the usage of Abacus. Abacus is a tool that
can analyze secret-dependent control-flow and secret-dependent data-access
leakages in binary programs. Unlike previous tools that can only identify
leakages, it can also estimate the amount of leaked information for each
leakage site. Severe vulnerabilities usually leak more information, allowing
developers to triage the patching effort for side-channel vulnerabilities.
This paper is to help users make use of Abacus and reproduce our previous results.
Abacus is available at <https://github.com/s3team/Abacus>.
