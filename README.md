# Awesome AI for Software Reverse Engineering [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated collection of learning-based reverse engineering research, focusing on recovering and understanding low-level code using machine learning, deep learning, and large language models (LLMs).

## 🎯 Overview

Reverse engineering (RE) has entered a new phase. 
While traditional RE relies heavily on handcrafted heuristics and symbolic analysis, recent advances in **learning-based methods** have fundamentally changed how we recover and understand low-level code.

This repository tracks this paradigm shift — from early machine learning approaches, to deep neural models, and most recently, **large language models (LLMs)** — highlighting how learning-based techniques enable scalable, semantic, and cross-platform reverse engineering.

### Core Focus: Learning-based Code Understanding & Recovery

This repository focuses on research whose **primary goal** is to **recover or enhance human understanding of low-level or opaque code representations** using learning-based techniques.

<details>
<summary><strong>Included topics:</strong></summary>

- Structure Recovery, e.g., function boundary identification, control flow graph recovery, and modular decomposition
- Semantic Recovery, e.g., type inference, variable naming, function naming and summarization
- Code Reconstruction, e.g., neural decompilation, decompiler output refinement
</details>

<details>
<summary><strong>Supported representations:</strong></summary>

- Native binaries (x86, ARM, MIPS)
- Bytecode (JVM, EVM, .NET, Android/Dalvik)
- WebAssembly (Wasm)
</details>

<details>
<summary><strong>Excluded topics:</strong></summary>

- Analysis performed directly on high-level source code
- Vulnerability detection, malware classification, or exploit generation unless program understanding is the primary contribution
</details>

## 📌 Table of Contents

### **📖 Top Conferences**

* [S&P](#sp), [CCS](#ccs), [USENIX Security](#sec), [NDSS](#ndss), [ICSE](#icse), [FSE](#fse), [ASE](#ase), [ISSTA](#issta), [PLDI](#pldi)

### **📜 Top Journals**
* [TOSEM](#tosem), [TSE](#tse), [TIFS](#tifs), [TDSC](#tdsc)

### **📌 Other Papers**
* [ICLR](#iclr), [ICML](#icml), [NeurIPS](#neurips), [ACL](#acl), [EMNLP](#emnlp), [ACSAC](#acsac), [ASIACCS](#asiaccs), [ICSME](#icsme), [SANER](#saner), [arXiv](#arxiv), [other](#other)

### **📊 Benchmarks、Study & SoKs**
* [benchmark-dataset](#-benchmarksstudy--soks-1)

### **🛠️ Collected Tools**
* [collected-tools](#🛠️-collected-tools-1)

---
## 📚 Top Conferences

### S&P
([26](#sp2026), [25](#sp2025), [24](#sp2024), [23](#sp2023))

#### sp2026

- [Decompilation] [Oxidizer: Toward Concise and High-fidelity Rust Decompilation](https://adamdoupe.com/publications/oxidizer-oakland2026.pdf). [[repo](https://github.com/sefcom/oxidizer)]

#### sp2025

- [Data-Code Separation] [You Can't Judge a Binary by Its Header: Data-Code Separation for Non-Standard ARM Binaries Using Pseudo Labels](https://ieeexplore.ieee.org/document/11023308/).
- [Decompilation] [PyLingual: Toward Perfect Decompilation of Evolving High-Level Languages](https://kangkookjee.io/wp-content/uploads/2025/09/pylingual-blackhat24-1.pdf). [[repo](https://github.com/syssec-utd/pylingual)].
- [Composite Type Inference] [TypeForge: Synthesizing and Selecting Best-Fit Composite Data Types for Stripped Binaries](https://noobone123.github.io/papers/typeforge-sp25.pdf).

#### sp2024

- [Variable Naming] [Len or index or count, anything but v1": Predicting Variable Names in Decompilation Output with Transfer Learning](https://ieeexplore.ieee.org/document/10646727/). [[repo](https://github.com/sefcom/VarBERT)].

#### sp2023

- [Control Flow Recovery] [Callee: Recovering Call Graphs for Binaries with Transfer and Contrastive Learning](https://arxiv.org/abs/2111.01415). [[repo](https://github.com/vul337/Callee)].
- [Function Naming] [XFL: Naming Functions in Binaries with Extreme Multi-label Learning](https://doi.ieeecomputersociety.org/10.1109/SP46215.2023.10179439). [[repo](https://github.com/lmu-plai/xfl)].

---

### CCS
([26](#ccs2026), ([25](#ccs2025), [24](#ccs2024), [22](#ccs2022), [21](#ccs2021))

#### ccs2026

- [Function Naming] [Hieronym: Leveraging Hierarchical Multi-Source Information for Function Renaming in Stripped Binary](https://arxiv.org/abs/2609.12457).

#### ccs2025

- [Instruction Recovery, Function Recovery, Control Flow Recovery] [Disa: Accurate Learning-based Static Disassembly with Attentions](https://doi.org/10.1145/3719027.3744828). [[repo](https://github.com/peicwang/Disa)].

#### ccs2024

- [Variable Naming, Type Inference] [ReSym: Harnessing LLMs to Recover Variable and Data Structure Symbols from Stripped Binaries](https://doi.org/10.1145/3658644.3670340). [[repo](https://github.com/lt-asset/resym/)].

#### ccs2022

- [Function Naming] [SymLM: Predicting Function Names in Stripped Binaries via Context-Sensitive Execution-Aware Code Embeddings](https://dl.acm.org/doi/10.1145/3548606.3560612). [[repo](https://github.com/OSUSecLab/SymLM)].

#### ccs2021

- [Pretrained-model] [PalmTree: Learning an Assembly Language Model for Instruction Embedding](https://dl.acm.org/doi/10.1145/3460120.3484587). [[repo](https://github.com/palmtreemodel/PalmTree)].


---

### USENIX Security
([25](#sec2025), [24](#sec2024), [22](#sec2022))

#### sec2025

- [Function Naming] [BLens: contrastive captioning of binary functions using ensemble embedding](https://www.usenix.org/system/files/conference/usenixsecurity25/sec25cycle1-prepub-271-benoit.pdf). [[zenodo](https://doi.org/10.5281/zenodo.14732394)].
- [Instruction Recovery] [Tady: A Neural Disassembler without Structural Constraint Violations](https://www.usenix.org/conference/usenixsecurity25/presentation/qin). [[repo](https://github.com/5c4lar/tady)].

#### sec2024

- [Type Inference] [TYGR: type inference on stripped binaries using graph neural networks](https://www.usenix.org/conference/usenixsecurity24/presentation/zhu-chang). [[repo](https://github.com/sefcom/TYGR)].

#### sec2022

- [Variable Naming, Type Inference] [Augmenting Decompiler Output with Learned Variable Names and Types](https://www.usenix.org/conference/usenixsecurity22/presentation/chen-qibin). [[repo](https://github.com/CMUSTRUDEL/DIRTY)].
- [Instruction Recovery, Function Recovery] [DeepDi: Learning a Relational Graph Convolutional Network Model on Instructions for Fast and Accurate Disassembly](https://www.usenix.org/conference/usenixsecurity22/presentation/yu-sheng). [[repo](https://github.com/DeepBitsTechnology/DeepDi)].

---

### NDSS
([26](#ndss2026), [25](#ndss2025), [24](#ndss2024), [21](#ndss2021))

#### ndss2026

- [Code Refinement] [FidelityGPT: Correcting Decompilation Distortions with Retrieval Augmented Generation](http://arxiv.org/abs/2510.19615). [[repo](https://github.com/ZhouZhiping045/FidelityGPT)].
- [Decompilation, Composite type inference, Variable Naming] [Idioms: Neural Decompilation With Joint Code and Type Definition Prediction](https://www.ndss-symposium.org/wp-content/uploads/2026-f795-paper.pdf). [[repo](https://github.com/squaresLab/idioms)].

#### ndss2025

- [Variable Naming] [Unleashing the Power of Generative Model in Recovering Variable Names from Stripped Binary](https://www.ndss-symposium.org/ndss-paper/unleashing-the-power-of-generative-model-in-recovering-variable-names-from-stripped-binary/). [[repo](https://doi.org/10.5281/zenodo.14220042)].
- [Function Naming] [Beyond Classification: Inferring Function Names in Stripped Binaries via Domain Adapted LLMs](https://www.ndss-symposium.org/ndss-paper/beyond-classification-inferring-function-names-in-stripped-binaries-via-domain-adapted-llms/). [[repo](https://github.com/OSUSecLab/SymGen)].

#### ndss2024

- [Variable Naming, Binary Summarization, Code Refinement] [DeGPT: Optimizing Decompiler Output with LLM](https://www.ndss-symposium.org/ndss-paper/degpt-optimizing-decompiler-output-with-llm/). [[repo](https://github.com/PeiweiHu/DeGPT)].

#### ndss2021

- [Instruction Recovery, Function Recovery] [XDA: Accurate, Robust Disassembly with Transfer Learning](https://www.ndss-symposium.org/wp-content/uploads/ndss2021_1B-3_23112_paper.pdf). [[repo](https://github.com/CUMLSec/XDA)].


---

### ICSE
([22](#icse2022))

#### icse2022

- [Binary Structure Recovery] [Modx: Binary Level Partial Imported Third-Party Library Detection through Program Modularization and Semantic Matching](http://arxiv.org/abs/2204.08237).


---

### FSE
([25](#fse2025), [24](#fse2024), [23](#fse2023), [22](#fse2022), [21](#fse2021))

#### fse2025

- [Variable Naming, Decompilation] [DiSCo: Towards Decompiling EVM Bytecode to Source Code using Large Language Models](https://doi.org/10.1145/3729373). [[online](https://suxnju.github.io/disco/)].
- [Binary Summarization] [MiSum: Multi-modality Heterogeneous Code Graph Learning for Multi-intent Binary Code Summarization](https://doi.org/10.1145/3715780). [[repo](https://github.com/Kobe-Zed/MiSum)].
- [Type Inference] [Recasting Type Hints from WebAssembly Contracts](https://doi.org/10.1145/3729388). [[repo](https://github.com/sepine/WasmHint)].

#### fse2024

- [Function Naming] [Enhancing Function Name Prediction using Votes-Based Name Tokenization and Multi-task Learning](https://doi.org/10.1145/3660782). [[repo](https://github.com/Xiaolinger-Z/Epitome)].

#### fse2023

- [Type Inference] [DeepInfer: Deep Type Inference from Smart Contract Bytecode](https://doi.org/10.1145/3611643.3616343). [[repo](https://github.com/sepine/DeepInfer)].
- [Function Recovery] [FunProbe: Probing Functions from Binary Code through Probabilistic Analysis](https://dl.acm.org/doi/10.1145/3611643.3616366). [[repo](https://github.com/sepine/FunProbe)].

#### fse2022

- [Memory Dependence Analysis] [NeuDep: neural binary memory dependence analysis](https://dl.acm.org/doi/10.1145/3540250.3549147).

#### fse2021

- [Type Inference] [StateFormer: fine-grained type recovery from binaries using generative state modeling](https://doi.org/10.1145/3468264.3468607). [[repo](https://github.com/CUMLSec/stateformer)].


---

### ASE
([26](#ase2026), [25](#ase2025), [24](#ase2024), [23](#ase2023))

#### ase2026

- [Evaluation] [Beyond Text Matching: Towards Reference-Free Evaluation for  Human-Oriented Binary Reverse Engineering](http://arxiv.org/abs/2608.07038). [[artifacts](https://doi.org/10.5281/zenodo.19247812)]

#### ase2025

- [Binary Structure Recovery] [BinStruct: Binary Structure Recovery Combining Static Analysis and Semantics](https://ieeexplore.ieee.org/document/11334428). [[online](https://sites.google.com/view/binstruct/home)].
- [Code Refinement] [PseudoFix: Refactoring Distorted Structures in Decompiled C Pseudocode](https://ieeexplore.ieee.org/document/11334626). [[repo](https://github.com/giles-one/PseudoFix)].

#### ase2024

- [Type Inference] [TypeFSL: Type Prediction from Binaries via Inter-procedural Data-flow Analysis and Few-shot Learning](https://doi.org/10.1145/3691620.3695502). [[repo](https://github.com/CupCupRay/TypeFSL)].
- [Decompilation] [WaDec: Decompiling WebAssembly Using Large Language Model](https://doi.org/10.1145/3691620.3695020). [[repo](https://github.com/XinyuShe/WaDec)].

#### ase2023

- [Pretrained-model, Binary Summarization, Function Naming, Variable Naming, etc] [HexT5: Unified Pre-Training for Stripped Binary Code Information Inference](https://ieeexplore.ieee.org/document/10298504/). [[repo](https://github.com/USTC-TTCN/HexT5)].


---

### ISSTA
([25](#issta2025), [24](#issta2024), [21](#issta2021))

#### issta2025

- [Code Refinement] [DecLLM: LLM-Augmented Recompilable Decompilation for Enabling Programmatic Use of Decompiled Code](https://doi.org/10.1145/3728958). [[online](https://sites.google.com/view/decllm)].

#### issta2024

- [Pretrained-model, Binary Summarization] [CLAP: Learning Transferable Binary Code Representations with Natural Language Supervision](https://dl.acm.org/doi/10.1145/3650212.3652145). [[repo](https://github.com/Hustcw/CLAP)].
- [Binary Structure Recovery] [DeLink: Source File Information Recovery in Binaries](https://doi.org/10.1145/3650212.3680338).
- [Type Inference, Binary Summarization] [Multi-modal Learning for WebAssembly Reverse Engineering](https://doi.org/10.1145/3650212.3652141).

#### issta2021

- [Function Naming] [A lightweight framework for function name reassignment based on large-scale stripped binaries](https://doi.org/10.1145/3460319.3464804). [[repo](https://github.com/USTC-TTCN/NFRE)].


---

### PLDI
([22](#pldi2022))

#### pldi2022

- [Type Inference] [Finding the Dwarf: Recovering Precise Types from WebAssembly Binaries](https://doi.org/10.1145/3519939.3523449). [[repo](https://github.com/sola-st/wasm-type-prediction)].


---

## 📜 Top Journals

### TOSEM
([26](#tosem2026), [25](#tosem2025), [23](#tosem2023))

#### tosem2026

- [Type Inference, Variable Naming] [HyRES: Recovering Data Structures in Binaries via Semantic Enhanced Hybrid Reasoning](https://dl.acm.org/doi/10.1145/3736719). [[repo](https://github.com/Sandspeare/HyRES)].

#### tosem2025

- [Binary Summarization] [ByteCue: enhancing bytecode comment generation with API information](https://dl.acm.org/doi/10.1145/3772717). [[repo](https://github.com/kaykayhard/ByteCue)].
- [Type Inference] [Beyond the Edge of Function: Unraveling the Patterns of Type Recovery in Binary Code](http://arxiv.org/abs/2503.07243). [[repo](https://github.com/giles-one/ByteTR)].
- [Binary Summarization] [Automating Comment Generation for Smart Contract from Bytecode](https://dl.acm.org/doi/10.1145/3699597). [[figshare](https://figshare.com/s/e5f3f9371ca67a63c122)].
- [Function Naming] [llasm: Naming Functions in Binaries by Fusing Encoder-only and Decoder-only LLMs](https://dl.acm.org/doi/10.1145/3702988). [[repo](https://github.com/Sandspeare/llasm)].

#### tosem2023

- [Variable Naming] [DIRE and its Data: Neural Decompiled Variable Renamings with Respect to Software Class](https://doi.org/10.1145/3546946).


---

### TSE
([25](#tse2025), [22](#tse2022))

#### tse2025

- [Function Recovery, Type Inference, Code Refinement] [Augmenting Smart Contract Decompiler Output Through Fine-Grained Dependency Analysis and LLM-Facilitated Semantic Recovery](https://doi.ieeecomputersociety.org/10.1109/TSE.2025.3623325). [[code](https://github.com/Janelinux/SmartHalo)].

#### tse2022

- [Inline Function Recovery] [Learning to Find Usages of Library Functions in Optimized Binaries](https://doi.ieeecomputersociety.org/10.1109/TSE.2021.3106572).


---

### TIFS
([25](#tifs2025))

#### tifs2025

- [Binary Summarization] [Malsight: Exploring Malicious Source Code and Benign Pseudocode for Iterative Binary Malware Summarization](https://ieeexplore.ieee.org/document/11052730/).


---

## 📌 Other Papers

---

### ICLR
([26](#iclr2026), [25](#iclr2025))

#### iclr2026

- [Function Naming, Variable Naming, Decompilation] [SK2Decompile: LLM-based Two-Phase Binary Decompilation from Skeleton to Skin](http://arxiv.org/abs/2509.22114). [[repo](https://github.com/albertan017/LLM4Decompile)].

#### iclr2025

- [Decompilation] [Nova: Generative Language Models for Assembly Code with Hierarchical Attention and Contrastive Learning](http://arxiv.org/abs/2311.13721). [[repo](https://github.com/lt-asset/nova)].


---

### ICML
([24](#icml2024))

#### icml2024

- [Decompilation, Variable Naming, Binary Summarization] [StackSight: Unveiling WebAssembly through Large Language Models and Neurosymbolic Chain-of-Thought Decompilation](http://arxiv.org/abs/2406.04568).


---

### EMNLP
([24](#emnlp2024), [23](#emnlp2023))

#### emnlp2024

- [Decompilation] [LLM4Decompile: Decompiling Binary Code with Large Language Models](http://arxiv.org/abs/2403.05286). [[repo](https://github.com/albertan017/LLM4Decompile)].

#### emnlp2023

- [Binary Summarization] [CP-BCS: binary code summarization guided by control flow graph and pseudo code](https://arxiv.org/abs/2310.16853). [[repo](https://github.com/tongye98/BinaryCodeSummary)].


---

### ACSAC
([25](#acsac2025), [22](#acsac2022))

#### acsac2025

- [Binary Summarization] [AndroByte: LLM-Driven Privacy Analysis through Bytecode Summarization and Dynamic Dataflow Call Graph Generation](http://arxiv.org/abs/2510.15112). [[repo](https://github.com/Eshita66/AndroByte)].

#### acsac2022

- [Decompilation] [Boosting neural networks to decompile optimized binaries](http://arxiv.org/abs/2301.00969). [[repo](https://github.com/zijiancogito/neur-dp-data.git)].


---

### ASIACCS
([24](#asiaccs2024), [23](#asiaccs2023))

#### asiaccs2024

- [Function Naming] [BinAdapter: Leveraging Continual Learning for Inferring Function Symbol Names in a Binary](https://dl.acm.org/doi/10.1145/3634737.3645006). [[repo](https://github.com/SecAI-Lab/BinAdapter)].

#### asiaccs2023

- [Function Naming] [A Transformer-based Function Symbol Name Inference Model from an Assembly Language for Binary Reversing](https://dl.acm.org/doi/10.1145/3579856.3582823). [[repo](https://github.com/agwaBom/AsmDepictor)].


---

### SANER
([23](#saner2023))

#### saner2023

- [Binary Summarization] [Extending Source Code Pre-Trained Language Models to Summarise Decompiled Binaries](https://ieeexplore.ieee.org/document/10123452/). [[zenodo](https://doi.org/10.5281/zenodo.7229809)].

---

### arXiv
([26](#arxiv2026), [25](#arxiv2025), [24](#arxiv2024), [23](#arxiv2023), [22](#arxiv2022))

#### arxiv2026

- [Type inference] [InterType: Breaking the Single-Function Barrier in Neural Binary Type Inference](https://arxiv.org/abs/2610.26906).
- [Decompilation] [Binary Decompilation LLM with Feedback-Driven Multi-Turn Refinement](http://arxiv.org/abs/2606.16162). [[hugging face](https://huggingface.co/AutoDecompiler)]
- [Code Refinement] [PCodeTrans: Translate Decompiled Pseudocode to Compilable and Executable Equivalent](https://arxiv.org/abs/2603.14855).
- [Code Refinement] [From Transactions to Exploits: Automated PoC Synthesis for Real-World DeFi Attacks](http://arxiv.org/abs/2601.16681).
- [Control Flow Recovery] [iResolveX: Multi-Layered Indirect Call Resolution via Static Reasoning and Learning-Augmented Refinement](https://arxiv.org/pdf/2601.17888v1).

#### arxiv2025

- [Function Naming] [AGNOMIN -- Architecture Agnostic Multi-Label Function Name Prediction](https://arxiv.org/abs/2509.25514). [[repo](https://github.com/Xiaolinger-Z/Epitome)].
- [Decompilation] [Beyond C/C++: Probabilistic and LLM Methods for Next-Generation Software Reverse Engineering](https://arxiv.org/abs/2506.03504).
- [Decompilation] [The CodeInverter Suite: Control-Flow and Data-Mapping Augmented Binary Decompilation with LLMs](http://arxiv.org/abs/2503.07215). [[repo](https://github.com/LiuPeiP-CS/CodeInverter)].
- [Control Flow Recovery] [Resolving Indirect Calls in Binary Code via Cross-Reference  Augmented Graph Neural Networks](http://arxiv.org/abs/2507.18801). [[zenodo](https://zenodo.org/records/12364897)].
- [Pretrained-model, Decompilation, Function Naming, Variable Naming, Type Inference, Binary Summarization] [ReCopilot: Reverse Engineering Copilot in Binary Analysis](https://arxiv.org/abs/2505.16366). [[online](https://tqgpt.qianxin.com/recopilot)].
- [Decompilation] [ReF Decompile: Relabeling and Function Call Enhanced Decompile](https://arxiv.org/abs/2502.12221). [[repo](https://github.com/AlongWY/ReF-Dec)].
- [Decompilation] [SALT4Decompile: Inferring Source-level Abstract Logic Tree for LLM-Based Binary Decompilation](http://arxiv.org/abs/2509.14646). [[repo](https://anonymous.4open.science/r/SALT4Decompile-0758)].
- [Decompilation] [Context-Guided Decompilation: A Step Towards Re-executability](https://arxiv.org/abs/2511.01763).
- [Decompilation] [Decompiling Smart Contracts with a Large Language Model](https://arxiv.org/pdf/2506.19624).

#### arxiv2024

- [Instruction Recovery] [Disassembling Obfuscated Executables with LLM](http://arxiv.org/abs/2407.08924).
- [Type Inference, Variable Naming] [STRIDE: Simple Type Recognition In Decompiled Executables](http://arxiv.org/abs/2407.02733).
- [Function Naming, Variable Naming, Code Refinement] [Exploring the Efficacy of Large Language Models (GPT-4) in Binary Reverse Engineering](https://arxiv.org/abs/2406.06637). [[repo](https://github.com/sinapordanesh/ENEL-592-Project)].

### Other
- [CNSSE-2026] [From Heuristics to Transformers: A Comprehensive Survey of  Type Inference from Stripped Binaries](http://arxiv.org/abs/2606.23692).
- [BAR-2022] [Beyond the C: Retargetable Decompilation using  Neural Machine Translation](http://arxiv.org/abs/2212.08950). [[repo](https://figshare.com/s/2c68b9c181e80f4e3b06)].
- [CGO-2024] [SLaDe: A Portable Small Language Model Decompiler for Optimized Assembly](https://ieeexplore.ieee.org/abstract/document/10497336). [[zenodo](https://doi.org/10.5281/zenodo.10205121)].
- [CODASPY-2026] [Practical Type Inference: High-Throughput Recovery of Real-World Structures and Function Signatures](http://arxiv.org/abs/2603.08225).
- [DTRP-2024] [Asm2Seq: Explainable Assembly Code Functional Summary Generation for Reverse Engineering and Vulnerability Analysis](https://dl.acm.org/doi/10.1145/3592623). [[repo](https://github.com/L1NNA/Juliet-NDSS18-BinaryCodeSum)].
- [ESORICS-2023] [AttnCall: Refining Indirect Call Targets in Binaries with Attention](https://link.springer.com/10.1007/978-3-031-51482-1_20). [[repo](https://github.com/anonmai/AttnCall)].
- [ICSME-2024] [Optimizing Decompiler Output by Eliminating Redundant Data Flow in Self-Recursive Inlining](https://ieeexplore.ieee.org/abstract/document/10795101). [[repo](https://figshare.com/s/35290b4ad2e11824c3ef)].
- [ICSME-2024] [How Far Have We Gone in Binary Code Understanding Using Large Language Models](https://arxiv.org/abs/2404.09836).
- [IJCAI-2025] [BinMetric: A Comprehensive Binary Code Analysis Benchmark for Large Language Models](https://arxiv.org/abs/2505.07360).
- [ISC-2025] [LLM-DAS: An LLM-Powered Deobfuscation System for ARM Binary Code](https://link.springer.com/10.1007/978-981-95-6209-1_17).
- [ISC-2024] [Attention-Based Decompilation Through Neural Machine Translation](https://link.springer.com/10.1007/978-981-96-4731-6_16).
- [NLP4Prog-2021] [DIRECT: A Transformer-based Model for  Decompiled Variable Name Recovery](https://aclanthology.org/2021.nlp4prog-1.6/). [[repo](https://github.com/DIRECT-team/DIRECT-nlp4prog)].
- [PST-2023] [Investigating Neural-based Function Name Reassignment from the Perspective of Binary Code Representation](https://ieeexplore.ieee.org/abstract/document/10320193). [[repo](https://github.com/USTC-TTCN/NER)].
- [SmartSP-2024] [RustBound: Function Boundary Detection over Rust Stripped Binaries](). [[code](https://github.com/UCdasec/RustBound)].
- [TrustCom-2024] [SBCM: Semantic-Driven Reverse Engineering Framework for Binary Code Modularization](https://ieeexplore.ieee.org/document/10944919).
- [WWW-2025] [SuiGPT MAD: Move AI Decompiler to Improve Transparency and Auditability on Non-Open-Source Blockchain Smart Contract](https://dl.acm.org/doi/abs/10.1145/3696410.3714790). [[code](https://github.com/EasonC13/MAD_WWW)].
- [WWW-2023] [Automated WebAssembly Function Purpose Identification With Semantics-Aware Analysis](https://dl.acm.org/doi/10.1145/3543507.3583235).


---

## 📊 Benchmarks、Study & SoKs
- [Github-2026] [Blindsight: A regression harness for LLM-assisted binary triage with GhidraMCP; single-model, two-fixture pilot](https://github.com/AlicanAkyol/blindsight).
- [CSUR-2026] [A Survey of Symbol Name Recovery in Sotware Reverse Engineering](https://dl.acm.org/doi/pdf/10.1145/3844948).
- [Arxiv-2026] [SoK: AI-Augmented Binary Reversing](http://arxiv.org/abs/2606.17398).
- [Github-2026] [DecBench: An experimental living benchmark to measure how close we are to perfect decompilation on binaries.](https://github.com/Noelo-Lab/decbench). [[repo](https://github.com/Noelo-Lab/decbench)]
- [NDSS-2026] [Decompiling the Synergy: An Empirical Study of Human–LLM Teaming in Software Reverse Engineering](https://www.ndss-symposium.org/ndss-paper/decompiling-the-synergy-an-empirical-study-of-human-llm-teaming-in-software-reverse-engineering/).
- [arXiv-2026] [REBENCH: A Procedural, Fair-by-Construction Benchmark for  LLMs on Stripped-Binary Types and Names](https://arxiv.org/abs/2604.27319). [[zenodo](https://zenodo.org/records/19899116)].
- [arXiv-2025] [An Empirical Study on the Effectiveness of Large Language Models for Binary Code Understanding](http://arxiv.org/abs/2504.21803). [[repo](https://github.com/Sxxxw/BinaryLLMs-Eval)]
- [arXiv-2025] [BuildBench: Benchmarking LLM Agents on Compiling Real-World Open-Source Software](https://arxiv.org/abs/2509.25248).
- [arXiv-2025] [Decompile-Bench: Million-Scale Binary-Source Function Pairs for Real-World Binary Decompilation](http://arxiv.org/abs/2505.12668). [[repo](https://github.com/albertan017/LLM4Decompile)].
- [arXiv-2025] [Benchmarking Binary Type Inference Techniques in Decompilers](https://dl.acm.org/doi/10.1145/3733822.3764675). [[repo](https://github.com/sefcom/decompiler-types-benchmark)].
- [IJCAI-2025] [BinMetric: A Comprehensive Binary Code Analysis Benchmark for Large Language Models](https://arxiv.org/abs/2505.07360).
- [ASE-2025] [R3-Bench: Reproducible Real-world Reverse Engineering Dataset for Symbol Recovery](https://ieeexplore.ieee.org/document/11334366). [[repo](https://github.com/aur3l14no/R3-Bench)].
- [arXiv-2025] [SoK: Potentials and Challenges of Large Language Models for Reverse Engineering](http://arxiv.org/abs/2509.21821).
- [arXiv-2025] [An Empirical Study on the Effectiveness of Large Language Models for Binary Code Understanding](http://arxiv.org/abs/2504.21803).
- [ICSME-2024] [How Far Have We Gone in Binary Code Understanding Using Large Language Models](https://arxiv.org/abs/2404.09836).
- [ISSTA-2024] [Evaluating the Effectiveness of Decompilers](https://dl.acm.org/doi/10.1145/3650212.3652144).
- [Security-2024] [A taxonomy of C decompiler fidelity issues](https://www.usenix.org/conference/usenixsecurity24/presentation/dramko).
- [arXiv-2023] [Binary Code Summarization: Benchmarking ChatGPT/GPT-4 and Other Large Language Models](https://arxiv.org/abs/2312.09601). [[repo](https://github.com/xinjin95/BinSum)].
- [Security-2022] [RE-Mind: a First Look Inside the Mind of a Reverse Engineer](https://www.usenix.org/conference/usenixsecurity22/presentation/mantovani).
- [Security-2022] [Decomperson: How Humans Decompile and What We Can Learn From It](https://www.usenix.org/conference/usenixsecurity22/presentation/burk).
- [arXiv-2022] [Pop Quiz! Can a Large Language Model Help With Reverse Engineering?](https://arxiv.org/abs/2202.01142). [[repo](https://doi.org/10.5281/zenodo.5949075)].
- [SP-2021] [SoK: All You Ever Wanted to Know About x86/x64 Binary Disassembly But Were Afraid to Ask](https://arxiv.org/abs/2007.14266). [[repo](https://github.com/junxzm1990/x86-sok)].

## 🛠️ Collected Tools

| Tool | Last Commit | Stars |
| :--- | :--- | :---: |
| [Noelo-Lab/kuna](https://github.com/Noelo-Lab/kuna) | ![Last Commit](https://img.shields.io/github/last-commit/Noelo-Lab/kuna) | [![Stars](https://img.shields.io/github/stars/Noelo-Lab/kuna?style=social)](https://img.shields.io/github/last-commit/Noelo-Lab/kuna) |
| [cyberkaida/reverse-engineering-assistant](https://github.com/cyberkaida/reverse-engineering-assistant) | ![Last Commit](https://img.shields.io/github/last-commit/cyberkaida/reverse-engineering-assistant) | [![Stars](https://img.shields.io/github/stars/cyberkaida/reverse-engineering-assistant?style=social)](https://github.com/cyberkaida/reverse-engineering-assistant) |
| [mrexodia/ida-pro-mcp](https://github.com/mrexodia/ida-pro-mcp) | ![Last Commit](https://img.shields.io/github/last-commit/mrexodia/ida-pro-mcp) | [![Stars](https://img.shields.io/github/stars/mrexodia/ida-pro-mcp?style=social)](https://github.com/mrexodia/ida-pro-mcp) |
| [fosdickio/binary_ninja_mcp](https://github.com/fosdickio/binary_ninja_mcp) | ![Last Commit](https://img.shields.io/github/last-commit/fosdickio/binary_ninja_mcp) | [![Stars](https://img.shields.io/github/stars/fosdickio/binary_ninja_mcp?style=social)](https://github.com/fosdickio/binary_ninja_mcp) |
| [mooncat-greenpy/KinGAidra](https://github.com/mooncat-greenpy/KinGAidra) | ![Last Commit](https://img.shields.io/github/last-commit/mooncat-greenpy/KinGAidra) | [![Stars](https://img.shields.io/github/stars/mooncat-greenpy/KinGAidra?style=social)](https://github.com/mooncat-greenpy/KinGAidra) |
| [Forsworns/GhidrAI](https://github.com/Forsworns/GhidrAI) | ![Last Commit](https://img.shields.io/github/last-commit/Forsworns/GhidrAI) | [![Stars](https://img.shields.io/github/stars/Forsworns/GhidrAI?style=social)](https://github.com/Forsworns/GhidrAI) |
| [mahaloz/DAILA](https://github.com/mahaloz/DAILA) | ![Last Commit](https://img.shields.io/github/last-commit/mahaloz/DAILA) | [![Stars](https://img.shields.io/github/stars/mahaloz/DAILA?style=social)](https://github.com/mahaloz/DAILA) |
| [symgraph/BinAssist](https://github.com/symgraph/BinAssist) | ![Last Commit](https://img.shields.io/github/last-commit/symgraph/BinAssist) | [![Stars](https://img.shields.io/github/stars/symgraph/BinAssist?style=social)](https://github.com/symgraph/BinAssist) |
| [radareorg/r2ai](https://github.com/radareorg/r2ai) | ![Last Commit](https://img.shields.io/github/last-commit/radareorg/r2ai) | [![Stars](https://img.shields.io/github/stars/radareorg/r2ai?style=social)](https://github.com/radareorg/r2ai) |
| [r0ysue/r0idamcp](https://github.com/r0ysue/r0idamcp) | ![Last Commit](https://img.shields.io/github/last-commit/r0ysue/r0idamcp) | [![Stars](https://img.shields.io/github/stars/r0ysue/r0idamcp?style=social)](https://github.com/r0ysue/r0idamcp) |
| [fdrechsler/mcp-server-idapro](https://github.com/fdrechsler/mcp-server-idapro) | ![Last Commit](https://img.shields.io/github/last-commit/fdrechsler/mcp-server-idapro) | [![Stars](https://img.shields.io/github/stars/fdrechsler/mcp-server-idapro?style=social)](https://github.com/fdrechsler/mcp-server-idapro) |
| [ccq1/awsome_kali_mcpservers](https://github.com/ccq1/awsome_kali_mcpservers) | ![Last Commit](https://img.shields.io/github/last-commit/ccq1/awsome_kali_mcpservers) | [![Stars](https://img.shields.io/github/stars/ccq1/awsome_kali_mcpservers?style=social)](https://github.com/ccq1/awsome_kali_mcpservers) |
| [zinja-coder/apktool-mcp-server](https://github.com/zinja-coder/apktool-mcp-server) | ![Last Commit](https://img.shields.io/github/last-commit/zinja-coder/apktool-mcp-server) | [![Stars](https://img.shields.io/github/stars/zinja-coder/apktool-mcp-server?style=social)](https://github.com/zinja-coder/apktool-mcp-server) |
| [WPeace-HcH/WPeChatGPT](https://github.com/WPeace-HcH/WPeChatGPT) | ![Last Commit](https://img.shields.io/github/last-commit/WPeace-HcH/WPeChatGPT) | [![Stars](https://img.shields.io/github/stars/WPeace-HcH/WPeChatGPT?style=social)](https://github.com/WPeace-HcH/WPeChatGPT) |
| [zyings/ReverseLLM](https://github.com/zyings/ReverseLLM) | ![Last Commit](https://img.shields.io/github/last-commit/zyings/ReverseLLM) | [![Stars](https://img.shields.io/github/stars/zyings/ReverseLLM?style=social)](https://github.com/zyings/ReverseLLM) |
| [jtang613/GhidrAssistMCP](https://github.com/jtang613/GhidrAssistMCP) | ![Last Commit](https://img.shields.io/github/last-commit/jtang613/GhidrAssistMCP) | [![Stars](https://img.shields.io/github/stars/jtang613/GhidrAssistMCP?style=social)](https://github.com/jtang613/GhidrAssistMCP) | ![Last Commit](https://img.shields.io/github/last-commit/jtang613/GhidrAssist) | [![Stars](https://img.shields.io/github/stars/jtang613/GhidrAssist?style=social)](https://github.com/jtang613/GhidrAssist) |
| [APiTJLillo/GhAIdra](https://github.com/APiTJLillo/GhAIdra) | ![Last Commit](https://img.shields.io/github/last-commit/APiTJLillo/GhAIdra) | [![Stars](https://img.shields.io/github/stars/APiTJLillo/GhAIdra?style=social)](https://github.com/APiTJLillo/GhAIdra) |
| [JusticeRage/Gepetto](https://github.com/JusticeRage/Gepetto) | ![Last Commit](https://img.shields.io/github/last-commit/JusticeRage/Gepetto) | [![Stars](https://img.shields.io/github/stars/JusticeRage/Gepetto?style=social)](https://github.com/JusticeRage/Gepetto) |
| [atredispartners/aidapal](https://github.com/atredispartners/aidapal) | ![Last Commit](https://img.shields.io/github/last-commit/atredispartners/aidapal) | [![Stars](https://img.shields.io/github/stars/atredispartners/aidapal?style=social)](https://github.com/atredispartners/aidapal) |
| [likvidera/GhidraChatGPT](https://github.com/likvidera/GhidraChatGPT) | ![Last Commit](https://img.shields.io/github/last-commit/likvidera/GhidraChatGPT) | [![Stars](https://img.shields.io/github/stars/likvidera/GhidraChatGPT?style=social)](https://github.com/likvidera/GhidraChatGPT) |
| [lr-m/GhidrOllama](https://github.com/lr-m/GhidrOllama) | ![Last Commit](https://img.shields.io/github/last-commit/lr-m/GhidrOllama) | [![Stars](https://img.shields.io/github/stars/lr-m/GhidrOllama?style=social)](https://github.com/lr-m/GhidrOllama) |
| [cyberark/ByteCodeLLM](https://github.com/cyberark/ByteCodeLLM) | ![Last Commit](https://img.shields.io/github/last-commit/cyberark/ByteCodeLLM) | [![Stars](https://img.shields.io/github/stars/cyberark/ByteCodeLLM?style=social)](https://github.com/cyberark/ByteCodeLLM) |
| [evyatar9/GptHidra](https://github.com/evyatar9/GptHidra) | ![Last Commit](https://img.shields.io/github/last-commit/evyatar9/GptHidra) | [![Stars](https://img.shields.io/github/stars/evyatar9/GptHidra?style=social)](https://github.com/evyatar9/GptHidra) |
| [moyix/gpt-wpre](https://github.com/moyix/gpt-wpre) | ![Last Commit](https://img.shields.io/github/last-commit/moyix/gpt-wpre) | [![Stars](https://img.shields.io/github/stars/moyix/gpt-wpre?style=social)](https://github.com/moyix/gpt-wpre) |
| [symgraph/GhidrAssist](https://github.com/symgraph/GhidrAssist) | ![Last Commit](https://img.shields.io/github/last-commit/symgraph/GhidrAssist) | [![Stars](https://img.shields.io/github/stars/symgraph/GhidrAssist)](https://github.com/symgraph/GhidrAssist) |

## 🔗 Contributing

This is a living repository. Contributions are welcome!

- Found a relevant paper? Submit a PR
- Disagree with the paper tag? Open an issue
- Have feedback? Create a discussion

## ⭐ License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released into the public domain.
