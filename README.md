# The mixed-dimensional quantum MacWilliams identity

This repository contains the source code for the paper: **"The mixed-dimensional quantum MacWilliams identity: bounds for codes and absolutely maximally entangled states in heterogeneous systems"** by David González-Lociga and Simeon Ball.

Any comments on the code, write me at davidgonzalezlociga@gmail.com.

## Overview
As emerging quantum architectures evolve into heterogeneous networks, traditional scalar metrics of quantum error correction become insufficient. This repository provides a mathematical framework based on dimension multisets to characterize quantum error-correcting codes (QECC) and absolutely maximally entangled (AME) states in mixed-dimensional Hilbert spaces.

## Code Structure
The provided Jupyter Notebook (`mixed-dimensional_MacWilliams.ipynb`) contains the Python implementations used to compute enumerators, verify linear programming bounds and evaluate mixed-dimensional AME states. 

Key components include:
* **`MixedDimensionalErrorBasis`**: A core class for generating the basis and calculating Shor-Laflamme, unitary, calligraphic and shadow enumerators for mixed-dimensional systems.
* **`LP_mixed_code` & `pure_LP_mixed_code`**: Linear program formulations that test the existence of general and pure mixed-dimensional codes using dimensional distance.
* **`TripartiteAMEGrid`**: A Z3-based combinatorial solver for explicitly generating and verifying tripartite AME states.
* **Heatmap Generation**: Functions to generate visual existence landscapes of AME states (e.g., qubits/qutrits and qutrits/ququarts) based on shadow enumerator positivity.

## Dependencies
To run the notebook, you will need Python 3 installed along with the following libraries:
* `numpy`
* `scipy`
* `cvxpy`
* `z3-solver`
* `matplotlib`
* `seaborn`

## Usage and Scalability Note
Simply open the Jupyter Notebook to view the mathematical functions and run the pre-configured examples. 

The code constructs the full Hilbert space and iterates over the complete error basis using tensor products. I believe this is not the most optimal approach so any comment on this or else are welcome !!! :)))

## Citation
If you use this code or framework in your research, please consider citing our paper:
> *https://arxiv.org/abs/2604.25790*
