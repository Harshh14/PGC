# Performance Analysis of Sequential, OpenMP, MPI, and CUDA

> A comparative study of different computing approaches for executing a common computational workload using sequential CPU execution, shared-memory parallelism, distributed-memory parallelism, and GPU-based acceleration.

---

## Table of Contents

1. [Experiment Objectives](#1-experiment-objectives)
2. [Theoretical & Architectural Comparison](#2-theoretical--architectural-comparison)
3. [Workload Specification](#3-workload-specification)
4. [Source Code References](#4-source-code-references)
5. [Experimental Results & Outputs](#5-experimental-results--outputs)
6. [Performance Comparison](#6-performance-comparison)
7. [Execution Steps](#7-execution-steps)
8. [Conclusion](#8-conclusion)

---

## Executive Summary

This experiment evaluates the performance of matrix multiplication using four different computing approaches:

1. **Sequential CPU**: Performs the complete computation using a single CPU execution thread.
2. **OpenMP**: Utilizes multiple CPU threads on a shared-memory system to execute the workload concurrently.
3. **MPI**: Distributes the computation among multiple processes communicating across separate memory spaces.
4. **CUDA**: Utilizes the parallel processing capability of a GPU to accelerate the computation.

The purpose of this experiment is to study how different parallel computing models affect execution performance and to compare them with the conventional sequential approach.

## 1. Experiment Objectives

The main objectives of this experiment are:

- **Implementation of Multiple Computing Models**: Develop and execute the same matrix multiplication workload using four approaches: Sequential, OpenMP, MPI, and CUDA.

- **Result Verification**: Use consistent input data across the implementations and verify that the computed matrix produces the expected result.

- **Performance Evaluation**: Measure and compare the execution time of sequential execution with shared-memory, distributed-memory, and GPU-based parallel execution.

- **Understanding Parallel Overheads**: Study the additional overhead associated with thread management, inter-process communication in MPI, and data transfers between the CPU and GPU in CUDA.

---

## 2. Theoretical & Architectural Comparison

### 2.1 Architectural Breakdown

The four implementations use different execution and memory models. The following table summarizes the major architectural differences:

| **Computing Model** | **Execution Model** | **Memory Space** | **Architectural Description** |
|---|---|---|---|
| **Sequential** | Single-Threaded | CPU Memory | The computation is performed sequentially by a single CPU thread using the conventional matrix multiplication approach. |
| **OpenMP** | Multi-Threaded | Shared Memory | The workload is divided among multiple CPU threads. All threads operate within the same shared memory space. |
| **MPI** | Multi-Process | Distributed Memory | The workload is divided among multiple MPI processes. Each process has its own memory space and communicates with other processes to exchange required data. |
| **CUDA** | GPU Parallel | Device Memory | The computation is transferred to the GPU and executed concurrently using a large number of GPU threads organized into blocks and grids. |

### 2.2 Computing Architecture Overview

The experiment demonstrates four different approaches to executing the same computational workload:

- **Sequential:** One CPU thread performs the entire computation.
- **OpenMP:** Multiple CPU threads share the workload and memory.
- **MPI:** Multiple processes perform distributed computation and communicate through the MPI framework.
- **CUDA:** GPU threads execute the computational workload in parallel using the GPU's device memory.

---

## 3. Workload Specification

The same matrix multiplication workload is used across the different implementations to ensure a consistent basis for execution and performance comparison.

- **Matrix Size (`N`)**: `4000 × 4000`

- **Matrix Initialization**: Both input matrices are initialized with the value `1.0` for every element:
  - `A[i][j] = 1.0`
  - `B[i][j] = 1.0`

- **Computation Performed**: Each element of the result matrix `C` is calculated by multiplying the corresponding row of `A` with the corresponding column of `B`:

  `C[i][j] = Σ(A[i][k] × B[k][j])`, where `k = 0` to `N-1`.

- **Result Verification**: Since all elements of `A` and `B` are initialized to `1.0`, the expected value of the first element of the result matrix is:

  `C[0][0] = 4000.00`

This common workload is maintained across the Sequential, OpenMP, MPI, and CUDA implementations for consistent comparison.

---

## 4. Source Code References

The program files for each computing approach are organized separately according to their respective experiment parts.

| **Computing Model** | **Part** | **Source Code** | **Implementation Description** |
|---|---|---|---|
| **Sequential CPU** | Part A | [View Program](./Part-A-Sequential/program/) | Sequential matrix multiplication executed using a single CPU thread. |
| **OpenMP** | Part B | [View Program](./Part-B-OpenMP/program/) | Matrix multiplication using multiple CPU threads with shared memory. |
| **MPI Distributed** | Part C | [View Program](./Part-C-MPI/program/) | Distributed matrix multiplication using multiple MPI processes and inter-process communication. |
| **CUDA GPU** | Part D | [View Program](./Part-D-CUDA/program/) | Matrix multiplication accelerated using parallel GPU execution with CUDA. |

### Source Code Organization

Each implementation is maintained inside its respective experiment-part directory. The corresponding program files can be accessed through the links provided above.

---
