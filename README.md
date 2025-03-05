# Parallel Particle Simulation (OpenMP)

This repository contains my **OpenMP-parallelized particle simulator**, developed in **C++** on the DOE-NERSC Perlmutter supercomputer. It reduces runtime from **34.36s to 2.78s** on **64 threads** for **100k particles**, achieving a **12× speedup** over the serial baseline.

## Project Structure
MAIN FILES:
-openmp.cpp -> parallel implementation of particle simulation for up to 64 threads.

-serial.cpp -> serial (no threads) implementation of simulation.

## Overview
- **Duration**: February 2025 – Present  
- **Goal**: Accelerate a particle interaction simulation using parallel computing techniques.  
- **Key Results**:  
  - Runtime: **2.78s** (down from 34.36s serial)  
  - Speedup: **12×** on 64 threads  
  - Complexity: Reduced from O(n²) to O(n) via spatial binning  

## Features
- **OpenMP Parallelization**: Distributes workload across 64 threads with per-bin locks and atomic updates for thread safety.  
- **Spatial Binning**: Uses linked lists to cut complexity from O(n²) to O(n), optimizing 100k-particle simulations.  
- **Memory Efficiency**: Pre-allocates nodes to eliminate dynamic allocation overhead.  

## Tech Stack
- **Languages**: C++  
- **Tools**: OpenMP, GCC, Git, Perlmutter Supercomputer (NERSC), Command Line  
- **Libraries**: Standard C++ (no external dependencies beyond OpenMP)  

