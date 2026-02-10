# 🧰 DEBUGGING & PROFILING TOOL ARCHITECTURE

====================================================
I️⃣ PYTHON LEVEL (General Programming Layer)
====================================================

A. Debugging (Correctness Tools)

   1. Basic Debugging
      - print()
      - traceback module
      - logging module

   2. Interactive Debuggers (Step-by-step execution)
      - VS Code Debugger
      - PyCharm Debugger
      - pdb
      - ipdb

   3. Runtime Crash Tools
      - faulthandler


B. Testing (Prevent Bugs Before They Happen)

   - pytest


C. CPU Profiling (Speed Analysis)

   1. Simple Timing
      - timeit

   2. Function-Level Profiling
      - cProfile
      - profile

   3. Line-Level Profiling
      - line_profiler


D. Memory Profiling (RAM Usage Analysis)

   - tracemalloc
   - memory_profiler


E. Advanced Profiling / Visualization

   - py-spy
   - scalene
   - snakeviz


====================================================
II️⃣ MACHINE LEARNING LEVEL (Framework-Specific)
====================================================

A. ML Debugging

   - Tensor shape inspection
   - logging inside training loops
   - assertion checks

   (Uses Python debugging tools)


B. ML Performance Profiling

   1. PyTorch
      - PyTorch Profiler

   2. TensorFlow
      - TensorFlow Profiler


C. GPU Monitoring

   - nvidia-smi
   - PyTorch Profiler GPU mode
   - TensorFlow Profiler GPU mode


====================================================
III️⃣ SYSTEM / ENVIRONMENT LEVEL
====================================================

A. Process Monitoring

   - top
   - htop
   - ps

B. Container Monitoring (if using Docker)

   - docker logs
   - docker stats
