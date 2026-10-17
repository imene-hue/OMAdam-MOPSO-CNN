# OMAdam-MOPSO-CNN
Multi-objective CNN optimization using OMAdam inspired initialization, MOPSO, OBL, MGDA and NSGA-II.
# OMAdam-MOPSO-CNN

This repository contains the source code and experimental results associated with our work on multi-objective optimization for Convolutional Neural Network (CNN) training.

The proposed framework combines gradient-based optimization and population-based search mechanisms, including OMAdam, MOPSO, Opposition-Based Learning (OBL), and local Adam refinement.

## Methods

The following methods are evaluated:

- Run A
- Run B
- Run C
- MGDA
- NSGA-II
- MOPSO

## Optimization Objectives

The CNN training problem is formulated as a bi-objective optimization problem using:

- Mean Absolute Error (MAE)
- L1-based model complexity

The reference point used for Hypervolume computation is:

```text
[1.5, 1.0]
