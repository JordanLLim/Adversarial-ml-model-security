# Adversarial ML & Model Security

A hands-on study of adversarial robustness and deep learning model security using PyTorch.

## Overview

This project consolidates two coursework-based experiments into a single portfolio covering adversarial attacks, model robustness, backdoor analysis, and model protection techniques.

The objective is to understand how trained models can be manipulated, how security mechanisms can be evaluated, and where existing defenses may fail.

## Research Areas

### 1. Adversarial Robustness

* Projected Gradient Descent (PGD)
* Transferability of adversarial examples
* Universal Adversarial Perturbations (UAP)
* Adaptive attacks and Expectation Over Transformation (EOT)
* Evaluation under constrained perturbation budgets

### 2. Backdoor & Model Security

* Backdoor attack analysis
* Trigger reverse engineering using Neural Cleanse-style methods
* Model fingerprinting and watermarking experiments
* Evaluation of model security mechanisms

## Experimental Workflow

1. Configure the target model and experimental setting.
2. Implement or adapt the attack method.
3. Evaluate attack effectiveness and relevant model metrics.
4. Compare results across experimental conditions.
5. Document limitations and reproducibility requirements.

## Tech Stack

* Python
* PyTorch
* Jupyter Notebook
* NumPy
* Matplotlib

## Reproducibility

See the individual notebooks for experiment-specific configurations, dependencies, and evaluation procedures.

Dataset access, model checkpoints, random seeds, and hardware requirements may vary by experiment.

## Scope & Limitations

This repository documents coursework-based implementations and experiments. It does not claim novel attack algorithms or production-grade security guarantees.

All reported results should be interpreted within their documented experimental settings.
