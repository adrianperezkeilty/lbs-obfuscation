# Software Obfuscation LAB
Development of the "Software Obfuscation" optional lab for the Language-Based Security course at Chalmers.

## 1. Motivation
Software obfuscation may be implemented to serve
- Intellectual Property Protection
- Security Enhancement
- Software Licensing Control
- Cryptographic Primitives
- Anti-Virus Evasion

## 2. Theoretical Obfuscation

### 2.1 Black box obfuscation is impossible
**Paper:** "On the (Im)possibility of Obfuscating Programs" Barak et al.

**Idea:** constructs a family of functions F, which are fundamentally resistant to obfuscation

**TODO**: small conceptual exercise

#### 2.1.1 Construction

### 2.2 Indistinguishability Obfuscation

#### 2.2.1 Background 
- $NC^1$ complexity class (problems that can be efficiently solved on a parallel computer).
- Branching programs (BPs)
- Barrington's Theorem (Any Boolean function that can be computed by a polynomial-size circuit can also be computed by a polynomial-width branching program)
- Directed Acyclic Graphs (DAGs)
- Garbling branching programs (GBPs)
- Multilinear maps 
- Multilinear Jigsaw Puzzles (MJPs)
- Fully Homomorphic Encryption (FHE)
- Hardness Assumptions

#### 2.2.2 Construction

**Paper:** "Candidate Indistinguishability Obfuscation and Functional Encryption for all circuits" — Garg et al.

**Idea:**

1. **$iO$ for $NC^1$:**
   1. Convert the circuit of the program into a Branching Program (BP)
   2. Randomize the BP applying random invertible matrices to each of the permutation matrices in the BP
   3. Obfuscate the computations of the BP using Garbled Branching Programs via Multilinear Jigsaw Puzzles (MJPs)

2. **$iO$ for $P$ (arbitrary polynomial-size circuits):**
   1. Use $iO$ for $NC^1$ with Fully Homomorphic Encryption whose decryption is in $NC^1$

**TODO**: Exercise: Obfuscate a small boolean function (use student randomness to choose a function from a list) 

## 3. Practical Obfuscation 
**Paper:** "Surreptitious Software: Obfuscation, Watermarking, and Tamperproofing for Software Protection" Collberg and Nagra.

### 3.1 Techniques:

- Lexical Transformations
- Data Obfuscation
- Control Flow Obfuscation
- Preventive Transformations

**TODO**: Exercise: combine two or more techniques to obfuscate a small program (also from a list using student randomness) 

### Reverse Engineer 

**TODO**: Given an obfuscated program using some of the above techniques, write pseudocode that reveals what the program is actually doing. 

### 3.2 International Obfuscated C Code Contest (IOCCC)
C code that is intentionally made as unreadable and confusing as possible, while remaining
functional.

Use these for inspiration.