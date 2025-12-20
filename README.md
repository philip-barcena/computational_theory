# Computational Theory Assignment

## Overview

 This assignment implements core components of the SHA-256 hashing algorithim. It demonstrates how unsalted SHA-256 is not suitable for password storage by performing a dictionary attack.

 ---

## Problems
### Binary Words and Bitwise Operations
Implemented the SHA-256 logical functions Ch, Maj, parity (XOR), and the
bitwise rotation and shift functions (Sigma0, Sigma1, sigma0, sigma1) using Python
and NumPy.

---

### Fractional Parts of Cube Roots
Generated the SHA-256 round constants by computing the fractional parts of
the cube roots of the first 64 prime numbers, matching the constants
published in the standard.

---

### Padding
Implemented message padding according to Sections 5.1.1 and 5.2.1 of the
standard. Messages are padded, length-encoded, and split into 512-bit
blocks.

### Hash
Implemented the SHA-256 compression function (hash(current, block)) as
defined in Section 6.2.2. The function processes one 512-bit block and
updates the current hash value using 64 rounds of modular arithmetic.

---

### Password Hash Analysis
A dictionary attack was performed on three given SHA-256 password hashes.
Common passwords were hashed using SHA-256 and compared against the given
hashes. The attack succeeded because the hashes were unsalted and generated
using a single fast SHA-256 iteration.

---

## Improving Password Hashing

Password hashing can be improved by:
- Adding a unique random salt to each password
- Using a slow, purpose-built password hashing algorithm
- Applying key stretching to increase the computational cost of each guess

These measures prevent dictionary attacks.
