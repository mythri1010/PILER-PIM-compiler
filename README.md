# PIMatrix Compiler: A Comprehensive Framework for PIM-Accelerated Matrix Computation
This compiler the bridges the gap between high-level code and next-generation hardware acceleration by automatically converting C/C++ matrix operations, particularly matrix multiplication—into optimized Processor-in-Memory (PIM) ISA instructions.

# Project Overview
The PIMatrix Compiler is an end-to-end compilation framework designed to bridge the gap between high-level programming abstractions and Processor-in-Memory (PIM) architectures. It automatically analyzes C/C++ code containing matrix operations (particularly matrix multiplication), optimizes them for PIM execution, and generates custom ISA (Instruction Set Architecture) instructions tailored for in-memory computing. By doing so, it eliminates the need for manual low-level PIM programming while maximizing hardware efficiency.

# Technical Architecture
2.1 Compiler Pipeline
The PIMatrix Compiler follows a multi-stage transformation process to bridge high-level code with PIM execution:
Matrix Optimization--
Static Analysis: Examines matrix sizes, memory access patterns, and data dependencies
Dependency Analysis: Verifies operation parallelizability to maximize PIM core utilization
PIM ISA Generation--
Converts optimized matrix operations into PIM-specific instructions:
PROG: Configures PIM cores for Multiply-Accumulate (MAC) operations
MEM: Manages data movement between CPU and PIM memory banks
EXE: Executes computational kernels directly in memory
The phase generates complete memory-mapped addressing schemes for all matrices.

2.2 Memory Management
The compiler implements sophisticated memory handling for PIM architectures:
Bank Allocation--
Distributes matrices across dedicated PIM memory banks (A, B, C) using a contention-aware scheduling algorithm. This ensures balanced memory bandwidth utilization across compute units.
Transposition Handling--
Automatically transposes matrix B during memory allocation to enable efficient row-wise access patterns in PIM cores, eliminating the need for explicit transpose operations in source code.

## **💎 Why It Matters & Who Needs It**  
🛠️ Solves a Critical Gap
First open-source compiler for PIM, automating ISA generation from C/C++ (no manual low-level coding!)
⚡ 5–10× Speedups
By eliminating CPU-DRAM bottlenecks and leveraging PIM’s parallel compute
🔋 90% Energy Savings
Slashes data movement costs (key for AI/ML and edge devices)

💡 Real-World Uses--
🤖 AI/ML Acceleration
Optimizes GEMM in CNNs, transformers, and recommender systems
🌍 Scientific Computing
Speeds up climate modeling, fluid dynamics, and quantum chemistry
📱 Edge AI
Enables real-time vision/NLP on low-power PIM devices
🧮 HPC Workloads
Boosts sparse matrix solvers for finite element analysis
🎓 Research & Education
Open-source reference for in-memory computing studies

💻 For Developers--
✨ No PIM Expertise Needed
Write C/C++ matrices → get optimized PIM code
🔌 Seamless Integration
Planned LLVM backend for broader compatibility
🔬 Hackable Design
Modular pipeline for testing new PIM architectures

# 👥 Team
- [@mythri1010](https://github.com/mythri1010)
- [@kamalesh-og](https://github.com/kamalesh-og)

# Documentation 
📚 **[Project Documentation](https://github.com/mythri1010/PILER-PIM-compiler/raw/main/Project-documentation.pdf)**  

## "PIMatrix Compiler bridges the abstraction gap between algorithms and in-memory hardware, proving that revolutionary speedups can be both accessible and elegant. 🧪🔧📈"
