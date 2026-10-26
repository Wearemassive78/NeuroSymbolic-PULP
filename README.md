# NeuroSymbolic-PULP
**The Hardware Cost of Explainability: Benchmarking and Optimizing Symbolic XAI Trees vs. Sub-Symbolic Neural Models for Autonomous Agents on RISC-V PULP**

*Research Project for the Intelligent Systems Engineering (ISE) Course — Alma Mater Studiorum - Università di Bologna*

## Overview
This repository hosts the software artifacts, compilation/simulation pipelines, and scientific documentation for **NeuroSymbolic-PULP**, investigating the microarchitectural, latency, and energy trade-offs between symbolic/interpretable XAI models (Decision Trees/Random Forests) and sub-symbolic quantized neural networks (`int8` MLPs/CNNs with `ReLU` and `Integer-GELU`) on a multi-core RISC-V PULP architecture (simulated via GVSoC).

## Repository Structure
- `docs/`: LaTeX sources and figures for the final scientific paper.
- `python_xai/`: Python pipelines for dataset preparation, model training, symbolic knowledge extraction (`Scikit-learn` / `PSyKE`), `int8` quantization, and C99 header generation.
- `riscv_pulp/`: Bare-metal C99 implementations (naive vs. branchless XAI trees, `PULP-NN` kernels, LUT vs. polynomial `Integer-GELU`), `pulp-riscv-gcc` Makefiles, and GVSoC profiling scripts.
- `agent_bridge/`: Proof-of-Concept perceptual wrapper feeding extracted symbolic percepts and XAI rule traces into a cognitive agent cycle.
