---
layout: default
title: Benchmark of PySCF 
---

# Performance benchmark

## Platforms

|           | Platform I    | Platform II     | Platform III    | Platform IV     |
| --------- |:-------------:|:---------------:|:---------------:|:---------------:|
| CPU       | Intel E5-2670 | Intel E5-2680v4 | Intel E5-2699v4 | Intel I7-7800X  |
| Memory    | 64 GB DDR3    | 256 GB DDR4     | 128 GB DDR4     | 64 GB DDR4      |
| OS        | Redhat 6.6    | Redhat 7.2      | Redhat 7.2      | Ubuntu 18.04    |
| BLAS      | MKL 11.0      | MKL 2017        | MKL 2017        | MKL 2018        |
| Compiler  | Intel 13.0    | GCC 4.8.5       | GCC 4.8.5       | GCC 7.3.0       |

---

## CCSD
Timing for updaing CCSD amplitudes in one iteration.
`OMP_NUM_THREADS=28` on Platform II.
[test script](https://github.com/pyscf/pyscf/blob/master/examples/2-benchmark/ccsd_iteration.py)

|         | Nocc | Nvir  | threads | time       |
| :------ |:----:|:-----:|:-------:|:----------:|
| H30/DZ  | 15   | 135   | 4       | 3.34    s  |
| H30/TZ  | 15   | 405   | 12      | 62.84   s  |
| H30/QZ  | 15   | 884   | 28      | 620.82  s  |
| H30/5Z  | 15   | 1631  | 28      | 6887.41 s  |
| H50/QZ  | 25   | 1472  | 28      | 8354.81 s  |

---

## FCI
Timing for FCI matrix-vector operation in one iteration.
8 threads - 36 threads on Platform III.
[test script](https://github.com/pyscf/pyscf/blob/master/examples/2-benchmark/fci_iteration.py)

### FCI solver for singlet

| threads | (12o, 12e) | (14o, 14e) | (16o, 16e) | (18o, 18e) |
|:--------|:----------:|:----------:|:----------:|:----------:|
| 8       | 0.072 s    | 0.99 s     | 18.50 s    | 423.42 s   |  
| 16      | 0.079 s    | 0.75 s     | 11.75 s    | 242.62 s   |  
| 32      | 0.095 s    | 0.71 s     | 8.364 s    | 155.59 s   |  
| 36      | 0.104 s    | 0.73 s     | 8.298 s    | 148.39 s   |  

### FCI solver for arbitrary spin symmetry states

| threads | (12o, 12e) | (14o, 14e) | (16o, 16e) | (18o, 18e) |
|:--------|:----------:|:----------:|:----------:|:----------:|
| 8       | 0.072 s    | 1.61 s     | 33.84 s    | 803.63 s   |
| 16      | 0.045 s    | 0.95 s     | 20.07 s    | 470.32 s   |
| 32      | 0.034 s    | 0.60 s     | 11.46 s    | 275.40 s   |
| 36      | 0.036 s    | 0.57 s     | 10.97 s    | 254.40 s   |

---

## Fock build with Multigrid
Timing for computing effective potential matrix in Fock build.
`OMP_NUM_THREADS=32` on Platform III.
[test script](https://github.com/pyscf/pyscf/blob/master/examples/2-benchmark/fock_multigrid.py)

|water cluster |  nao   |  LSDA     | PBE        |
|:-------------|:-------|:---------:|:----------:|
|32x1x1x1      |  1280  | 8.04    s |  23.27   s |
|32x2x1x1      |  2560  | 19.74   s |  55.74   s |
|32x2x2x1      |  5120  | 74.08   s |  252.80  s |
|32x2x2x2      |  12800 | 276.58  s |  1201.14 s |
|64x2x2x2      |  25600 | 1278.69 s |  4823.12 s |


---

## Benzene
`OMP_NUM_THREADS=16` on Platform I.
[test script](https://github.com/pyscf/pyscf/blob/master/examples/2-benchmark/bz.py)

|---------------|---------|---------|-------------|
|Basis          | 6-31G** | cc-pVTZ | ANO-Roos-TZ |
|---------------|---------|---------|-------------|
|HF             | 0.55 s  |  5.76 s | 389.1 s     |
|density fit HF | 3.56 s  |  7.61 s |  13.8 s     |
|B3LYP          | 3.84 s  | 11.44 s | 360.2 s     |
|MP2            | 0.21 s  |  4.66 s | 115.9 s     |
|CASSCF(6,6)    | 2.88 s  | 34.73 s | 639.7 s     |
|CCSD           | 18.24 s | 477.0 s | 6721 s      |
|---------------|---------|---------|-------------|

---

## C60
`OMP_NUM_THREADS=16` on Platform I.
[test script](https://github.com/pyscf/pyscf/blob/master/examples/2-benchmark/c60.py)

|---------------|---------|---------|
|Basis          | 6-31G** | cc-pVTZ |
|---------------|---------|---------|
|HF             | 1291 s  | 189 m   |
|SOSCF          |         | 77 m    |
|density fit HF | 316.7 s | 43.3 m  |
|---------------|---------|---------|

---

## Fe(II)-porphyrin (FeC20H12N4)
`OMP_NUM_THREADS=16` on Platform I.
test script

|---------------|---------|---------|---------|
|Basis          | cc-pVDZ | cc-pVTZ | cc-pVQZ |
|---------------|---------|---------|---------|
|SOSCF          | 193.4 s | 20.1 m  | 127.1 m |
|CASSCF(10,10)  | 1808 s  | 241 m   |         |
|CASSCF(11,8)   | 763.8 s | 150.3 m | 1280 m  |
|---------------|---------|---------|---------|

