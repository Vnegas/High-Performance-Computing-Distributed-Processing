# High-Performance Computing & Distributed Processing

A collection of projects and exercises exploring **parallel, concurrent, and distributed programming** using C and C++.

The repository covers multiple programming models and focuses on concurrency, workload distribution, performance optimization, and distributed computation.

## Technologies & Concepts

- **C / C++**
- **POSIX Threads (Pthreads)**
- **C++ Threads**
- **OpenMP**
- **MPI**
- **Task-based concurrency**
- **Thread synchronization**
- **Producer-Consumer architecture**
- **Socket programming**
- **Performance profiling and optimization**
- **Shared-memory and distributed-memory parallelism**

---

## Featured Projects

### Parallel ZIP Password Search

A brute-force ZIP password search implemented progressively using different parallel programming approaches.

The project started with a serial implementation and evolved through Pthreads, OpenMP, and workload-distribution optimizations. Performance was analyzed using profiling tools, speedup, and efficiency measurements.

**Implementations:**

- Serial baseline
- Optimized serial implementation
- Pthreads
- OpenMP
- Static workload distribution
- Dynamic workload distribution

**[→ View project and performance analysis](./Individual/Projects/zippass_optimized/)**

---

### Concurrent Web Server

A concurrent web server implemented in C++ using TCP sockets and a Producer-Consumer architecture.

The server handles multiple client connections and provides functionality for Goldbach's conjecture and prime factorization.

**Technologies & concepts:**

- C++
- TCP sockets
- Multithreading
- Producer-Consumer
- MVC architecture
- Singleton pattern
- Sieve of Eratosthenes

**[→ View project documentation](./Team/projects/project1/)**

---

### Parallel Heat Diffusion Simulation

A numerical simulation of heat diffusion across a rectangular grid, developed to study parallelization and performance.

The project includes profiling and an OpenMP implementation. In the reported test configuration, the parallel implementation achieved up to **3.72× speedup with 16 threads** compared with the serial implementation.

**[→ View project](./Team/projects/project2/)**  
**[→ View performance analysis](./Team/projects/project2/performance_analysis/report.md)**

---

## Repository Structure

```text
Individual/
├── Examples/
├── Exercises/
└── Projects/
    ├── zippass_serial/
    ├── zippass_pthread/
    ├── zippass_openmp/
    └── zippass_optimized/

Team/
├── common/
└── projects/
    ├── project1/
    ├── project2/
```
---
## Credits
Sebastián Venegas Brenes

Computer Science & Informatics
