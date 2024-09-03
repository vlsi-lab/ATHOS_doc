# ATHOS: Accelerating Post-Quantum Cryptography on RISC-V

## Overview

**ATHOS (Accelerated Technology for Hardware Optimization with RISC-V)** is a cutting-edge project aimed at enhancing cryptographic operations on RISC-V architectures. This project focuses on accelerating Post-Quantum Cryptography (PQC) algorithms, particularly the Kyber algorithm, by leveraging the innovative Core-V eXtension InterFace (CV-X-IF) of the CV32E40X core. The repository includes source code, hardware descriptions, and documentation to facilitate the replication and further exploration of the ATHOS architecture.

## Key Features

- **Core-V eXtension InterFace (CV-X-IF):** 
  - ATHOS is among the first projects to utilize the CV-X-IF, enabling seamless integration of new instructions and accelerators without requiring modifications to the toolchain.

- **Specialized Accelerator Design:** 
  - The project implements five top-level accelerators to significantly reduce the clock cycles required for critical PQC operations.

- **ASIC Implementation:** 
  - The architecture is implemented on 65μm ASIC technology, offering notable performance improvements with a 1.47× area overhead.

- **Kyber Algorithm Optimization:** 
  - ATHOS achieves up to a 7.74× improvement in the clock cycles required for the Kyber algorithm compared to baseline software implementations.

## Accelerators Overview

ATHOS introduces five specialized accelerators tailored to optimize key cryptographic operations within the Kyber algorithm:

1. **Montgomery Accelerator (`montg`):**
   - Optimizes Montgomery reduction operations, enhancing modular multiplication with secure, timing attack-resistant implementations.

2. **Barrett Accelerator (`barrett`):**
   - Accelerates Barrett reduction, a division-free method for modular reduction that leverages precomputed constants and efficient multiplication and shift operations.

3. **Matrix Generation Accelerator (`rej_uniform`):**
   - Speeds up matrix composition operations by efficiently handling intensive arithmetic and shifting operations within loops.

4. **Central Binomial Distribution Operations Accelerator (`cbd`):**
   - Enhances the performance of the Centered Binomial Distribution (CBD) sampling function, crucial for generating cryptographic noise.

5. **Polynomial Arithmetic Accelerator (`poly`):**
   - Optimizes polynomial arithmetic by consolidating bitwise operations into specialized instructions, significantly reducing loop overhead and improving overall performance.

## Repository Structure

- **`docs/`**: Includes detailed documentation on the architecture, including design and implementation details of the accelerators.