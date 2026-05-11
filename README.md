# ProteusFuzz

**Adaptive Closed-Loop Fuzzing System: Continuous Diagnosis and Repair of Fuzzer Blockers**

[![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![AFL++](https://img.shields.io/badge/Fuzzer-AFL++-orange.svg)](https://github.com/AFLplusplus/AFLplusplus)

</div>

---

## 📖 Project Overview

**ProteusFuzz** is an adaptive closed-loop fuzzing system built on the [PromeFuzz](https://github.com/pvz122/PromeFuzz) framework, focusing on continuous diagnosis and repair of runtime Fuzzer Blockers to improve code coverage and vulnerability discovery.

### Core Innovations

Unlike traditional one-shot LLM generation approaches, ProteusFuzz employs a **closed-loop feedback mechanism** combining the following key technologies:

- **🔍 Fine-grained Static Knowledge Extraction**: Extract structured knowledge from source code, documentation, and API usage patterns
- **🔄 Dynamic Fuzzing Feedback**: Real-time analysis of coverage data to identify uncovered code paths
- **🎯 Targeted Repair Strategies**: Precise repairs based on empirical taxonomy (seed-related vs harness-related)
- **🧬 Format-Compatible Seed Synthesis**: Generate high-quality test seeds conforming to input format constraints
- **🛠️ State-Aware Harness Optimization**: Dynamically adjust fuzzing harnesses based on program state

### Empirical Taxonomy

ProteusFuzz establishes a systematic Blocker classification system:

| Type | Description | Repair Strategy |
|------|-------------|-----------------|
| **Seed-related** | Insufficient or format-mismatched seed inputs | Generate format-compatible new seeds |
| **Harness-related** | Harness logic defects or state initialization issues | Optimize harness program logic |
| **Mixed** | Both seed and harness issues present | Collaborative optimization of both |
| **Uncertain** | Requires further analysis | Manual intervention or deep diagnosis |

---
