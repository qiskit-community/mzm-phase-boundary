# mzm-phase-boundary
This repository contains the code and data from the manuscript "Simulating spectroscopic detection of Majorana zero modes with a superconducting quantum computer."

## Code
The code herein was run using the development branch of Qiskit Terra, in particular the branch of [Pull Request #6899](https://github.com/Qiskit/qiskit-terra/pull/6899) that makes it possible to run `Parameter`s and `ParameterExpression`s through the `TemplateOptimization` transpiler pass. Some further changes in the main branch occured that caused problems transpiling the circuit resulting from `PauliTrotterEvolution`, hence the `mods-for-mzm-phase` [branch](https://github.com/nbronn/qiskit-terra/tree/mods-for-mzm-phase) is the reliable branch for reproducing results. We are working to include these corrections into the main branch of Qiskit Terra.

## Data
The data for the manuscript was taken with `./code/se_2site_opflow_param_sweep.ipynb` for various parameter sweeps, with some data in the Supplementary Material taken for the 3-site model with `./code/se_3site_opflow_param_sweep.ipynb`. While some attempt was made at error mitigation techniques such as dynamical decoupling (as in `se_2site_opflow_param_sweep.ipynb`) and Pauli twirling (as in `se_2site_pauli_twirl.ipynb`), the authors had trouble interpreting the data and so is not included in the manuscript, but is provided in this repository. We are still working to understand the impact of these error mitigation techniques on quantum simulation.

All data was exported using the `numpy` routines found at the bottom of each notebook. The data were analyzed using notebooks represented by `Analyze_Data_Example.ipynb`.
