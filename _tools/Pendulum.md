---
slug: pendulum
title: Pendulum
description: "Timing Side-Channel Mitigation via Automated Program Repair"
year: 2024
target: Java
technique: Dynamic
guarantees: "no"
available: true
repo: https://doi.org/10.6084/m9.figshare.20731846
papers:
 - name: "Timing Side-Channel Mitigation via Automated Program Repair"
   link: https://dl.acm.org/doi/10.1145/3678169
---

## Abstract

Side-channel vulnerability detection has gained prominence recently due to Spectre
and Meltdown attacks. Techniques for side-channel detection range from fuzz
testing to program analysis and program composition. Existing side-channel
mitigation techniques repair the vulnerability at the IR/binary level or use
runtime monitoring solutions. In both cases, the source code itself is not
modified, can evolve while keeping the vulnerability, and the developer would
get no feedback on how to develop secure applications in the first place. Thus,
these solutions do not help the developer understand the side-channel risks in
her code and do not provide guidance to avoid code patterns with side-channel risks.
In this paper, we present Pendulum, the first approach for automatically locating
and repairing side-channel vulnerabilities in the source code, specifically for
timing side channels. Our approach uses a quantitative estimation of found
vulnerabilities to guide the fix localization, which goes hand-in-hand with a
pattern-guided repair. Our evaluation shows that Pendulum can repair a large number
of side-channel vulnerabilities in real-world applications. Overall, our approach
integrates vulnerability detection, quantization, localization, and repair into one
unified process. This also enhances the possibility of our side-channel mitigation
approach being adopted into programming environments.
