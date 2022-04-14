## Constant-timeness verification tools

 This page lists tools for testing and verification of constant-timeness of programs.

## Tools

| Name              | Year | Target  | Technique   | Guarantees              |
| ----------------- | ---- | ------- | ----------- | ----------------------- |
| ABPV13            | 2013 | C       | Formal      | sound                   |
| Binsec/Rel        | 2020 | Binary  | Symbolic    | sound with restrictions |
| Blazer            | 2017 | Java    | Formal      | sound                   |
| BPT17             | 2017 | C       | Symbolic    | sound with restrictions |
| CacheAudit        | 2013 | Binary  | Formal      | other                   |
| CacheD            | 2016 | Trace   | Symbolic    | no                      |
| CacheFix          | 2018 |         |             |                         |
| COCO-CHANNEL      | 2018 | Java    | Symbolic    | sound                   |
| Constantine       | 2021 |         |             |                         |
| ctgrind           | 2010 | Binary  | Dynamic     | sound with restrictions |
| ct-fuzz           | 2020 | LLVM IR | Dynamic     | no                      |
| ct-verif          | 2016 | LLVM IR | Formal      | sound                   |
| CT-WASM           | 2019 | WASM    | Formal      | sound                   |
| DATA              | 2018 | Binary  | Dynamic     | sound with restrictions |
| dudect            | 2017 | Binary  | Statistical | no                      |
| FaCT              | 2019 | DSL     | Formal      | sound                   |
| FlowTracker       | 2016 | LLVM IR | Formal      | sound                   |
| haybale-pitchfork | 2019 | LLVM IR | Symbolic    | sound with restrictions |
| KMO12             | 2012 | Binary  | Formal      | other                   |
| MemSan            | -    | LLVM IR | Dynamic     | sound with restrictions |
| MicroWalk         | 2018 | Binary  | Dynamic     | sound with restrictions |
| pitchfork-angr    | 2019 |         |             |                         |
| SC-Eliminator     | 2018 | LLVM IR | Formal      | sound                   |
| SideTrail         | 2018 | LLVM IR | Formal      | other                   |
| Themis            | 2017 | Java    | Formal      | sound                   |
| timecop           | -    | Binary  | Dynamic     | sound with restrictions |
| tis-ct            | -    | C       | Symbolic    | sound with restrictions |
| TriggerFlow       | 2018 |         |             |                         |
| VirtualCert       | 2014 | x86     | Formal      | sound                   |

This table is based mostly on the work in [*“They’re not that hard to mitigate”: What Cryptographic Library Developers Think About Timing Attacks*](https://crocs.fi.muni.cz/public/papers/usablect_sp22) with manual addition of more tools. 

### ABPV13

- Introduced in “Formal verification of side-channel countermeasures using self-composition” by J. B. Almeida, M. Barbosa, J. S. Pinto, and B. Vieira; https://doi.org/10.1016/j.scico.2011.10.008
- **Tool not available**

### Binsec/Rel

- Introduced in “Binsec/rel: Efficient relational symbolic execution for constant-time at binary-level” by L. Daniel, S. Bardin, and T. Rezk; https://doi.org/10.1109/SP40000.2020.00074
- **Tool available:** https://github.com/binsec/Rel ![GitHub last commit](https://img.shields.io/github/last-commit/binsec/Rel) ![GitHub contributors](https://img.shields.io/github/contributors/binsec/Rel)![GitHub Repo stars](https://img.shields.io/github/stars/binsec/Rel)
- **Tests available:** https://github.com/binsec/rel_bench ![GitHub last commit](https://img.shields.io/github/last-commit/binsec/rel_bench)![GitHub contributors](https://img.shields.io/github/contributors/binsec/rel_bench)![GitHub Repo stars](https://img.shields.io/github/stars/binsec/rel_bench)
- **Binsec/Rel** is a static analysis tool that works on the binary level, thereby overcoming issues of compilers inserting non-constant-time code or turning constant-time code into non-constant-time one.

### Blazer

- Introduced in “Decomposition instead of self-composition for proving the absence of timing channels” by T. Antonopoulos, P. Gazzillo, M. Hicks, E. Koskinen, T. Terauchi, and S. Wei; https://doi.org/10.1145/3062341.3062378
- **Tool not available**

### BPT17

- Introduced in “Verifying constant-time implementations by abstract interpretation” by S. Blazy, D. Pichardie, and A. Trieu; https://doi.org/10.1007/978-3-319-66402-6_16
- **Tool not available**

### CacheAudit

- Introduced in “CacheAudit: A tool for the static analysis of cache side channels” by G. Doychev, D. Feld, B. Köpf, L. Mauborgne, and J. Reineke; https://www.usenix.org/conference/usenixsecurity13/technical-sessions/paper/doychev
- **Tool available:** https://github.com/cacheaudit/cacheaudit  ![GitHub last commit](https://img.shields.io/github/last-commit/cacheaudit/cacheaudit) ![GitHub contributors](https://img.shields.io/github/contributors/cacheaudit/cacheaudit)![GitHub Repo stars](https://img.shields.io/github/stars/cacheaudit/cacheaudit)
- **Website:**  https://software.imdea.org/projects/cacheaudit/

### CacheD

- Introduced in “Cached: Identifying cache-based timing channels in production software” by S. Wang, P. Wang, X. Liu, D. Zhang, and D. Wu; https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/wang-shuai
- **Tool not available**

### CacheFix

- Introduced in “Symbolic verification of cache side-channel freedom” by S. Chattopadhyay and A. Roychoudhury; https://doi.org/10.1109/TCAD.2018.2858402
- **Tool available:** https://bitbucket.org/sudiptac/cachefix/src/master/ ![](https://img.shields.io/badge/last%20commit-may%202018-red)

### COCO-CHANNEL

- Introduced in “Symbolic path cost analysis for side-channel detection” by T. Brennan, S. Saha, T. Bultan, and C. S. Pasareanu; https://doi.org/10.1145/3213846.3213867
- **Tool not available**

### Constantine

- Introduced in “Constantine: Automatic side-channel resistance using efficient control and data flow linearization” by P. Borrello, D. C. D’Elia, L. Querzoni, and C. Giuffrida; https://arxiv.org/abs/2104.10749
- **Tool available:** https://github.com/pietroborrello/constantine  ![GitHub last commit](https://img.shields.io/github/last-commit/pietroborrello/constantine) ![GitHub contributors](https://img.shields.io/github/contributors/pietroborrello/constantine)![GitHub Repo stars](https://img.shields.io/github/stars/pietroborrello/constantine)

### ctgrind

- Introduced in https://github.com/agl/ctgrind and https://www.imperialviolet.org/2010/04/01/ctgrind.html.
- **ctgrind** is a patch available for the Valgrind (memcheck) tool, which adds functionality to mark areas of memory as uninitialized. This is to be used on secrets. At runtime, the memcheck tool then checks that the secret(uninitialized) memory is not used in branches or for memory access. As Valgrind's memcheck supports the `VALGRIND_MAKE_MEM_UNDEFINED` and `VALGRIND_MAKE_MEM_DEFINED` client requests, it is now possible to implement a ctgrind-like approach without patches to Valgrind.
- **Tool available:** Use Valgrind directly.

### ct-fuzz

- Introduced in “ct-fuzz: Fuzzing for timing leaks” by S. He, M. Emmi, and G. F. Ciocarlie; https://doi.org/10.1109/ICST46399.2020.00063
- **ct-fuzz** takes inspiration from **ct-verif** in its method but diverges significantly. It first constructs a product program using self-composition of the target with itself, where it asserts that at each point that the memory address accessed by the two programs, whether through control from or indexing, is the same. It then uses a fuzzer against this product program, which splits its fuzzing input equally into the secret inputs for the two instances or the original program in the product program. If the fuzzer detects a failed assert, leakage is detected, as it found two runs through the target, which differ only in secret inputs yet access different offsets in memory.
- **Tool available:** https://github.com/michael-emmi/ct-fuzz  ![GitHub last commit](https://img.shields.io/github/last-commit/michael-emmi/ct-fuzz) ![GitHub contributors](https://img.shields.io/github/contributors/michael-emmi/ct-fuzz)![GitHub Repo stars](https://img.shields.io/github/stars/michael-emmi/ct-fuzz)

### ct-verif

- Introduced in “Verifying Constant-Time Implementations” by J. B. Almeida, M. Barbosa, G. Barthe, F. Dupressoir and M. Emmi; https://www.usenix.org/system/files/conference/usenixsecurity16/sec16_paper_almeida.pdf
- The **ct-verif** tool is a static analysis tool verifying constant-time properties of code, working on the level of LLVM IR, with source code annotations. It uses the [SMACK](http://smackers.github.io/) modular software verification toolchain, [Bam-Bam-Boogieman](https://github.com/michael-emmi/bam-bam-boogieman) for Boogie source transformation, [Boogie](https://github.com/boogie-org/boogie) intermediate verification language as well as the [Corral](https://github.com/boogie-org/corral) and [Z3](https://github.com/Z3Prover/z3) solvers. 
- The tool is actively deployed in the CI of Amazon's **s2n** library at [link](https://github.com/awslabs/s2n/tree/main/tests/ctverif). However, even there, it is only used to verify two functions that together have less than 100 lines of code.
- **Tool available:** https://github.com/imdea-software/verifying-constant-time  ![GitHub last commit](https://img.shields.io/github/last-commit/imdea-software/verifying-constant-time) ![GitHub contributors](https://img.shields.io/github/contributors/imdea-software/verifying-constant-time)![GitHub Repo stars](https://img.shields.io/github/stars/imdea-software/verifying-constant-time)

### CT-WASM

- Introduced in “CT-WASM: type-driven secure cryptography for the web ecosystem” by C. Watt, J. Renner, N. Popescu, S. Cauligi, and D. Stefan; https://doi.org/10.1145/3290390
- **Tool available:** https://github.com/PLSysSec/ct-wasm ![GitHub last commit](https://img.shields.io/github/last-commit/PLSysSec/ct-wasm) ![GitHub contributors](https://img.shields.io/github/contributors/PLSysSec/ct-wasm)![GitHub Repo stars](https://img.shields.io/github/stars/PLSysSec/ct-wasm)

### DATA

- Introduced in “DATA - differential address trace analysis: Finding address-based side-channels in binaries” by S. Weiser, A. Zankl, R. Spreitzer, K. Miller, S. Mangard, and G. Sigl; https://www.usenix.org/conference/usenixsecurity18/presentation/weise
- Used in “Big numbers - big troubles: Systematically analyzing nonce leakage in (EC)DSA implementations” by S. Weiser, D. Schrammel, L. Bodner, and R. Spreitzer;  https://www.usenix.org/conference/usenixsecurity20/presentation/weiser
- **DATA** (Differential Address Trace Analysis) is a tool quite similar to the **Microwalk** framework in that it is a dynamic tool that records memory-accesses of the target into address traces as it processes random secret inputs. The traces are then aligned and analyzed using generic and specific leakage tests. The tool reports the location of leakage and even offers a graphical user interface for analysis.
- **Tool available:** https://github.com/Fraunhofer-AISEC/DATA ![GitHub last commit](https://img.shields.io/github/last-commit/Fraunhofer-AISEC/DATA) ![GitHub contributors](https://img.shields.io/github/contributors/Fraunhofer-AISEC/DATA)![GitHub Repo stars](https://img.shields.io/github/stars/Fraunhofer-AISEC/DATA)

### dudect

- Introduced in “Dude, is my code constant time?” by O. Reparaz, J. Balasch, and I. Verbauwhede; https://doi.org/10.23919/DATE.2017.7927267
- **dudect** is a dynamic tool that uses leakage assessment techniques from physical (power and EM) side-channel analysis, namely test-vector leakage assessment (TVLA). It first runs the target using two classes of secret input data with varying public input data and measures the duration of execution for each run. It then applies a test to the two distributions of the duration of execution for the two classes (either Welch's t-test for equality of means or Kolmogorov-Smirnov test for equality of distributions), and if the distributions differ, leakage is reported. This is analogous to how leakage assessment is used in power side-channel attacks, in that instead of comparing distributions of power consumption at points during the execution of the target, the runtime distributions are compared.
- **Tool available:** https://github.com/oreparaz/dudect ![GitHub last commit](https://img.shields.io/github/last-commit/oreparaz/dudect) ![GitHub contributors](https://img.shields.io/github/contributors/oreparaz/dudect)![GitHub Repo stars](https://img.shields.io/github/stars/oreparaz/dudect)

### ENCoVer

- Introduced in “ENCoVer: Symbolic exploration for information flow security” by M. Balliu, M. Dam, and G. L. Guernic; https://doi.org/10.1109/CSF.2012.24
- **Tool not available:**  http://www.nada.kth.se/~musard/encover

### FaCT

- Introduced in “FaCT: a DSL for timing-sensitive computation” by S. Cauligi, G. Soeller, B. Johannesmeyer, F. Brown, R. S. Wahby,
  J. Renner, B. Grégoire, G. Barthe, R. Jhala, and D. Stefan; https://doi.org/10.1145/3314221.3314605
- The **FaCT** tool is less of a tool for analysis of implementations for timing leakage and more of a domain-specific language for writing constant-time implementations that automatically removes leakage during compilation. The language is C-like, compiles into LLVM IR, and offers the `secret` keyword, which is used to mark certain variables as secret, which then triggers the compiler to generate constant-time code with regards to their values.
- **Tool available:** https://github.com/plsyssec/fact ![GitHub last commit](https://img.shields.io/github/last-commit/plsyssec/fact) ![GitHub contributors](https://img.shields.io/github/contributors/plsyssec/fact)![GitHub Repo stars](https://img.shields.io/github/stars/plsyssec/fact)

### FlowTracker

- Introduced in “Sparse representation of implicit flows with applications to side-channel detection” by B. Rodrigues, F. M. Q. Pereira, and D. F. Aranha; https://doi.org/10.1145/2892208.2892230
- The **FlowTracker** tool is a static tool that works by analyzing the Program Dependence Graph (PDG) of the target in LLVM IR form.
- **Tool not available:** http://cuda.dcc.ufmg.br/flowtracker/

### haybale-pitchfork

- Introduced in https://github.com/PLSysSec/haybale-pitchfork
- **Tool available:** https://github.com/PLSysSec/haybale-pitchfork ![GitHub last commit](https://img.shields.io/github/last-commit/PLSysSec/haybale-pitchfork) ![GitHub contributors](https://img.shields.io/github/contributors/PLSysSec/haybale-pitchfork)![GitHub Repo stars](https://img.shields.io/github/stars/PLSysSec/haybale-pitchfork)

### KMO12

- Introduced in “Automatic quantification of cache side-channels” by B. Köpf, L. Mauborgne, and M. Ochoa; https://doi.org/10.1007/978-3-642-31424-7_40
- **Tool not available**

### MemSan

- Introduced in https://clang.llvm.org/docs/MemorySanitizer.html
- **Tool available:** Use MemorySanitizer.

### MicroWalk

- Introduced in “Microwalk: A framework for finding side channels in binaries” by J. Wichelmann, A. Moghimi, T. Eisenbarth, and B. Sunar; https://doi.org/10.1145/3274694.3274741
- The **MicroWalk** framework is a dynamic tool that uses Dynamic Binary Instrumentation (DBI) and Mutual Information Analysis (MIA). As a dynamic tool, it runs the target with random inputs and uses dynamic binary instrumentation to log events such as memory allocations, branches, calls, returns, memory reads/writes as well as stack operations into an execution trace. It then processes these traces by applying the chosen leakage model, i.e., in the branching model, it only keeps the control flow events in the execution traces. After collection of traces, it offers several analysis options, either directly comparing the traces or using mutual information analysis either on the whole trace or a specific offset in the execution traces (a specific instruction).
- **Tool available:** https://github.com/UzL-ITS/Microwalk ![GitHub last commit](https://img.shields.io/github/last-commit/UzL-ITS/Microwalk) ![GitHub contributors](https://img.shields.io/github/contributors/UzL-ITS/Microwalk)![GitHub Repo stars](https://img.shields.io/github/stars/UzL-ITS/Microwalk)

### pitchfork-angr

- Introduced in https://github.com/PLSysSec/pitchfork-angr
- **Tool available:** https://github.com/PLSysSec/pitchfork-angr ![GitHub last commit](https://img.shields.io/github/last-commit/PLSysSec/pitchfork-angr) ![GitHub contributors](https://img.shields.io/github/contributors/PLSysSec/pitchfork-angr)![GitHub Repo stars](https://img.shields.io/github/stars/PLSysSec/pitchfork-angr)

### SC-Eliminator

- Introduced in “Eliminating timing side-channel leaks using program repair” by M. Wu, S. Guo, P. Schaumont, and C. Wang; https://doi.org/10.1145/3213846.3213851
- **Tool not available**

### SideTrail

- Introduced in “Sidetrail: Verifying time-balancing of cryptosystems” by K. Athanasiou, B. Cook, M. Emmi, C. MacCárthaigh, D. Schwartz-Narbonne, and S. Tasiran; https://doi.org/10.1007/978-3-030-03592-1_12
- **SideTrail** (at one point called SideWinder) is a tool for verifying time-balanced implementations. The notion of time-balance is a weakening of the constant-time notion that allows for the presence of leakage that is provably under some bound $\delta$ (execution time is negligibly influenced by secrets). For $\delta = 0$ this notion fits well with the notion of constant-time. The tool uses a cross-product technique similar to that of **ct-verif**. However, instead of asserting the equality of memory accesses and program counter, it asserts the equality of an instruction counter. Its leakage model and technique are well suited against remote (non-cache) attackers.
- The tool is deployed in the CI of Amazon's **s2n** library at [link](https://github.com/awslabs/s2n/tree/main/tests/sidetrail), where it is used to verify the time-balancedness of several parts of the codebase, handling the CBC decryption, HMAC padding, and AEAD decryption.
- **Tool not available**

### Themis

- Introduced in “Precise detection of side-channel vulnerabilities using quantitative cartesian hoare logic” by J. Chen, Y. Feng, and I. Dillig; https://doi.org/10.1145/3133956.3134058
- **Tool not available**

### timecop

- Introduced in https://www.post-apocalyptic-crypto.org/timecop/
- The **TIMECOP** tool is a tool that uses Valgrind's memcheck client requests `VALGRIND_MAKE_MEM_{UN}DEFINED`  to essentially implement a method like **ctgrind**. It is a part of the [SUPERCOP](https://bench.cr.yp.to/supercop.html) toolkit (**S**ystem for **U**nified **P**erformance **E**valuation **R**elated to **C**ryptographic **O**perations and **P**rimitives) and is used to evaluate the constant-time properties of implementations in SUPERCOP.
- **Tool available:** https://www.post-apocalyptic-crypto.org/timecop/

### tis-ct

- http://web.archive.org/web/20200810074547/http://trust-in-soft.com/tis-ct/
- **Tool not available**

### TriggerFlow

- Introduced in “Triggerflow: Regression Testing by Advanced Execution Path Inspection” by I. Gridin, C. P. García, N. Tuveri and B. B. Brumley; https://doi.org/10.1007/978-3-030-22038-9_16
- **Tool available:** https://gitlab.com/nisec/triggerflow

### VirtualCert

- Introduced in “System-level non-interference for constant-time cryptography” by G. Barthe, G. Betarte, J. D. Campo, C. D. Luna, and D. Pichardie; https://doi.org/10.1145/2660267.2660283
- **Tool available:** https://www.fing.edu.uy/inco/grupos/gsi/project/virtualcert/

## Resources

- https://neuromancer.sk/article/26
- https://crocs.fi.muni.cz/public/papers/usablect_sp22
