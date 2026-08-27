# ZIP Password Brute-Force — Pthreads Implementation

A parallel brute-force program that attempts to find passwords protecting ZIP files using **POSIX Threads (Pthreads)**.

This implementation extends the serial ZIP password search by distributing the password search space among multiple threads, allowing several password candidates to be tested concurrently.

## Input

The program reads the following information from standard input:

1. The set of characters that can be used in the password.
2. The maximum password length.
3. The paths of the ZIP files to process.

The number of threads is provided as a command-line argument.

### Example

```text
0123456789
5

tests/zip_05/f01.zip
tests/zip_05/f23.zip
tests/zip_05/f09.zip
```

The program can be executed with a specified number of threads:

```bash
./zippass_pthread 8 < input.txt
```

## Output

The program prints the path of each ZIP file followed by the password found.

```text
tests/zip_05/f01.zip 00112
tests/zip_05/f23.zip
tests/zip_05/f09.zip 9209
```

If a password cannot be found within the specified search space, only the ZIP file path is printed.

The output preserves the same order as the input files.

## Parallelization

The password search is parallelized using **POSIX Threads (Pthreads)**.

The search space is divided among the worker threads, allowing multiple password candidates to be evaluated concurrently.

The number of threads can be configured when executing the program, making it possible to evaluate the effect of different levels of concurrency on execution time.

## Implementation

This project is the parallel counterpart to the serial implementation of the ZIP password search.

It provides a basis for analyzing the performance impact of multithreading before introducing additional workload-distribution and optimization strategies.

## Design

The design and architecture of the application are documented in the [`design`](./design/) directory.

## Documentation

API documentation generated with Doxygen is available in the project documentation.

## Author

**Sebastián Venegas Brenes**
