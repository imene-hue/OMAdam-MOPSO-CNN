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
## Dataset

Experiments are performed on a reduced version of the MNIST dataset:

- 3,000 training samples
- 600 test samples
- Images normalized to [0,1]
- One-hot encoded labels

## CNN Architecture

The CNN architecture is fixed during the optimization process:

```text
Conv2D(8, 3x3, ReLU)
→ MaxPooling2D
→ Flatten
→ Dense(16, ReLU)
→ Dense(10, Softmax)
Only the trainable parameters of the network are optimized.
Main Experimental Parameters :
Population size: 200
Number of iterations: 30
Batch size: 64
Local training epochs: 1
Behavior deduplication batch: 128
Behavior deduplication threshold: 1e-3
Mutation standard deviation: 0.005
OBL local radius: 0.15
The experiments use the following random seeds:
[0, 7, 21, 42, 99]
Evaluation Metrics
The algorithms are evaluated using:
- Hypervolume (HV)
- Hypervolume at 1000 seconds
- Inverted Generational Distance (IGD)
- Spread
- Runtime
- Wilcoxon signed-rank test
Installation
Install the required Python packages using:
pip install -r requirements.txt
Run the main experiment using:
python main_experiment.py
Results
The results/ directory contains the generated numerical results, Pareto fronts, statistical summaries, and figures.
Reproducibility
The same random seeds are used across the compared methods to support fair paired comparisons.
The code also supports resume-after-crash execution by saving intermediate checkpoints.
