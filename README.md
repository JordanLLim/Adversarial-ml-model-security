# Adversarial ML & Model Security

A coursework-based portfolio exploring adversarial robustness and deep-learning model security with PyTorch.

## Overview

This repository combines two CSIT375 coursework notebooks to study how image-classification models can be attacked and how selected model-security mechanisms can be evaluated.

**Project status:** coursework experiments organized as a portfolio. The notebooks and saved outputs are preserved as the source of truth; the repository does not claim novel attack methods or production-ready defenses.

## Experiments

### 1. Adversarial robustness

[Open Assignment 1](./assignment1-csit375.ipynb)

- Targeted grey-box adversarial examples and transferability
- Universal adversarial perturbations (UAPs)
- Randomized-crop defense and an adaptive attack
- Perturbation constraints and attack success-rate evaluation

### 2. Backdoor and model security

[Open Assignment 2](./assignment2-csit375.ipynb)

- Small module-based backdoor experiment
- Trigger reverse engineering using a Neural Cleanse-style optimization
- Data-free adaptive attack against a model-fingerprinting evaluation
- Optional image watermarking and decoder evaluation

## Recorded results

The saved notebook outputs include a **98.0%** targeted grey-box fooling rate and **93.0%** UAP fooling rate on the specified Assignment 1 batch. The saved Assignment 2 outputs report **95.66%** accuracy on the constructed module-backdoor poisoned test set and **99.90%** on the poisoned test set for the trigger task. These are task-specific results, not general robustness guarantees.

See [Experiment Summary](./EXPERIMENT_SUMMARY.md) for the saved metrics, evaluation context, limitations, and interview framing.

## Technology

- Python 3.12
- PyTorch / Torchvision
- NumPy, SciPy, Matplotlib
- Jupyter Notebook
- Kaggle GPU runtime for the recorded experiments

## Reproducing the notebooks

The current notebooks depend on course-provided code, model checkpoints, datasets, and image assets referenced through `/kaggle/input/`. These assets are not all included here, so cloning this repository alone is **not sufficient** for a clean end-to-end rerun.

1. Open the notebook in Jupyter or Kaggle.
2. Obtain the required course codebase and assets through authorized course channels.
3. Update the input paths and verify the runtime/dependency versions.
4. Run cells in order and inspect the metrics and plots.

The saved outputs are included for reference. The experiments were not re-run when this portfolio documentation was prepared.

## Responsible use

These are educational, controlled coursework experiments. Do not use attack techniques against systems without authorization. Before distributing coursework implementations, ensure publication is permitted by the course's academic-integrity and intellectual-property rules.
