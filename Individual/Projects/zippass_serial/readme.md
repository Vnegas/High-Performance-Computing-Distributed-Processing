# ZIP Password Brute-Force — Serial Implementation

A serial brute-force program that attempts to find passwords protecting ZIP files.

The program receives a set of ZIP files, a password alphabet, and a maximum password length, then exhaustively searches the resulting password space.

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

## Implementation

This project provides the serial baseline for the subsequent parallel implementations of the ZIP password search.

The same problem is later explored using Pthreads, OpenMP, and additional optimization techniques.

## Design

The design of the application is documented in the [`design`](./design/) directory.

## Related Implementations

- [`zippass_pthread`](../zippass_pthread/) — Pthreads implementation
- [`zippass_openmp`](../zippass_openmp/) — OpenMP implementation
- [`zippass_optimized`](../zippass_optimized/) — optimized implementations and performance analysis

## Author

**Sebastián Venegas Brenes**
