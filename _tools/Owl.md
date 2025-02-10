---
slug: owl
title: Owl
description: "Owl: Differential-based Side-Channel Leakage Detection for CUDA Applications"
year: 2024
target: GPU
technique: Dynamic
guarantees: sound with restrictions
available: true
repo: https://github.com/OwlCudaSCDetector/Owl
papers:
 - name: "Owl: Differential-based Side-Channel Leakage Detection for CUDA Applications"
   link: https://doi.org/10.1109/DSN58291.2024.00044
---

![GitHub last commit](https://img.shields.io/github/last-commit/OwlCudaSCDetector/Owl)![GitHub contributors](https://img.shields.io/github/contributors/OwlCudaSCDetector/Owl)![GitHub Repo stars](https://img.shields.io/github/stars/OwlCudaSCDetector/Owl)

## Abstract

Over the past decade, various methods for detecting side-channel leakage have been
proposed and proven to be effective against CPU side-channel attacks. These methods
are valuable in assisting developers to identify and patch side-channel vulnerabilities.
Nevertheless, recent research has revealed the feasibility of exploiting side-channel
vulnerabilities to steal sensitive information from GPU applications, which are
beyond the reach of previous side-channel detection methods. Therefore, in this
paper, we conduct an in-depth examination of various GPU features and present Owl,
a novel side-channel detection tool targeting CUDA applications on NVIDIA GPUs.
Owl is designed to detect and locate side-channel leakage in various types of CUDA
applications. When tracking the execution of CUDA applications, we design a
hierarchical tracing scheme and extend the A-DCFG (Attributed Dynamic Control
Flow Graph) to address the massively parallel execution in CUDA, ensuring Owl's
detection scalability. After completing the initial assessment and filtering, we
conduct statistical tests on the differences in program traces to determine whether
they are indeed caused by input variations, subsequently facilitating the positioning
of side-channel leaks. We evaluate Owl's capability to detect side-channel leaks by
testing it on Libgpucrypto, PyTorch, and nvJPEG. Meanwhile, we verify that our
solution effectively handles a large number of threads. Owl has successfully
identified hundreds of leaks within these applications. To the best of our knowledge,
we are the first to implement side-channel leakage detection for general CUDA applications.
