# Adversarial ML & Model Security

A coursework-based portfolio exploring adversarial robustness and deep-learning model security with PyTorch.

## Overview

This repository brings together two CSIT375 coursework notebooks under one theme: how machine-learning models can be attacked, how robustness and security techniques can be evaluated, and what their limitations look like in controlled experiments.

> **Scope:** These are educational coursework experiments, not a claim of novel attack methods or production-ready security guarantees. Method names below describe the areas covered; consult each notebook for the exact implementation and experimental assumptions.

## Notebooks

### 1. Adversarial Robustness

[Open the Assignment 1 notebook](./assignment1-csit375.ipynb)

Topics explored include adversarial examples, constrained perturbations, transferability, universal perturbations, and adaptive attacks. The notebook contains the implementation details and experimental setup.

### 2. Backdoor & Model Security

[Open the Assignment 2 notebook](./assignment2-csit375.ipynb)

Topics explored include backdoor analysis, trigger reverse engineering, and model fingerprinting or watermarking-related security experiments. Refer to the notebook for the exact methods implemented and the assumptions used.

## Technology

- Python
- PyTorch
- Jupyter Notebook
- NumPy
- Matplotlib

## How to Explore

1. Open the relevant notebook in GitHub, Jupyter Notebook, or Google Colab.
2. Review its setup cells before running any experiment.
3. Check the dataset, model checkpoint, device, and random-seed requirements.
4. Run cells in order and compare the outputs under the documented settings.

The two notebooks may have different dependencies and compute requirements. This repository does not yet provide a single, fully automated environment for reproducing every experiment.

## Interpreting Results

Attack effectiveness and defense performance depend on the threat model, model architecture, data, perturbation constraints, and evaluation procedure. Results should only be compared when the experimental settings are compatible. Review the notebook outputs and code before drawing conclusions.

## Academic & Responsible Use

This repository is intended for learning and defensive model-security research in controlled settings. Before redistributing coursework code or materials, ensure that doing so is permitted by the course's academic-integrity and intellectual-property rules. Do not use these techniques to attack systems without authorization.
