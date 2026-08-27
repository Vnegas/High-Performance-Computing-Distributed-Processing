# ZIP Password Brute-Force — OpenMP Implementation

A parallel brute-force program that attempts to find passwords protecting ZIP files using **OpenMP**.

This implementation explores shared-memory parallelism by distributing the password search among multiple threads managed through the OpenMP programming model.

## Input

The program reads the following information from standard input:

1. The set of characters that can be used in the password.
2. The maximum password length.
3. The paths of the ZIP files to process.

### Example

```text
0123456789
5

tests/zip_05/f01.zip
tests/zip_05/f23.zip
tests/zip_05/f09.zip
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

The password search is parallelized using **OpenMP**, taking advantage of shared-memory parallelism.

The search space is distributed among multiple OpenMP threads so that password candidates can be evaluated concurrently.

The number of threads can be configured through the OpenMP runtime environment, allowing the implementation to be evaluated under different levels of parallelism.

## Implementation

This project provides an OpenMP-based implementation of the same ZIP password search problem explored in the serial and Pthreads versions.

Using the same problem with different parallel programming models makes it possible to compare different approaches to shared-memory parallelism.

## Design

The design and architecture of the application are documented in the [`design`](./design/) directory.

## Performance Analysis

Performance-related documentation and analysis are available in the [`report`](./report/) directory.

## Documentation

API documentation generated with Doxygen is available in the project documentation.

## Author

**Sebastián Venegas Brenes**
