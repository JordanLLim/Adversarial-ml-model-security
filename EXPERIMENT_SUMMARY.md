# Experiment Summary

This report records the outputs already saved in the two coursework notebooks. It is a summary of those notebook runs, not an independently reproduced benchmark.

## Environment and scope

- Dataset/model family: CIFAR-10 with VGG11-BN target models and course-provided code/checkpoints.
- Recorded runtime: Kaggle, Python 3.12.12, CUDA 12.6; the saved sessions report a Tesla P100 GPU.
- The notebooks use course-provided assets and paths under `/kaggle/input/`. They will not run end-to-end from this repository alone until those assets and the course codebase are obtained and the paths are configured.
- Assignment 1 and Assignment 2 show different PyTorch versions in their saved outputs (2.8.0+cu126 and 2.9.0+cu126 respectively).

## Assignment 1 — Adversarial robustness

| Experiment | Saved notebook output | Interpretation |
|---|---:|---|
| Target model accuracy on the selected clean input batch | 100.0% | The attack batch was filtered to images correctly classified by the target model. This is not the model's full test accuracy. |
| Targeted grey-box adversarial examples, maximum (L_\infty\) perturbation 0.04 | 98.0% fooling rate | High targeted attack success on the selected 100-image batch. |
| Universal adversarial perturbation, maximum (L_\infty\) perturbation 0.06 | 93.0% fooling rate | A shared perturbation reached the target label on the selected batch. |
| Grey-box examples evaluated against the randomized-crop robust model | 17.0% fooling rate | The saved evaluation shows a lower attack success rate under this defense wrapper. |
| Adaptive attack against the randomized-crop defense, maximum (L_\infty\) perturbation 0.04 | 94.0% fooling rate on 50 images | The adaptive attack recovered high targeted success on a smaller batch; this is not directly comparable to the 100-image results. |

The notebook's recorded coding marks are 11/11 for the main grey-box and UAP tasks, with the adaptive task recorded as 1 bonus mark.

## Assignment 2 — Backdoor and model-security experiments

| Experiment | Saved notebook output | Interpretation |
|---|---:|---|
| Clean task-1 model test accuracy | 87.22% | Baseline recorded before applying the module backdoor. |
| Module backdoor parameter count | 22,282 vs. 28,149,514 target-model parameters (0.08%) | The added module is much smaller than the target model in this setup. |
| Module-backdoor poisoned-set accuracy | 95.66% | The notebook's evaluation reports high accuracy on its constructed poisoned test set; interpret with the task's label and dataset construction in mind. |
| Task-2 poisoned model: clean test accuracy | 86.58% | Clean performance before trigger insertion. |
| Task-2 poisoned model: poisoned test accuracy | 99.90% | High trigger-associated target behavior in the supplied evaluation. |
| Trigger reverse-engineering run | 10 optimization epochs; final recorded mask norm 442.36 | The notebook shows the optimization trace; the mask norm alone does not establish trigger-recovery quality. |
| DeepJudge adaptive attack evaluation | Accuracy 89.80%; Rob 0.396; JSD 0.233 | These are the values printed by the saved notebook evaluation; their meaning depends on the course's metric definitions. |
| Optional image watermark task | TPR 100.0%, FPR 0.0%, TNR 100.0% | Recorded for the notebook's evaluation setup only; not evidence of general watermark robustness. |

The notebook records 15/15 for the main coding tasks and 2/2 for the optional watermark coding task.

## Limitations and reproducibility

1. These metrics are copied from saved notebook outputs. The notebooks were not re-run as part of preparing this summary.
2. Results use course-provided datasets, model checkpoints, utility code, and a Kaggle GPU runtime. Those dependencies are not all included in this repository.
3. The attack success rates are tied to specific batches, labels, perturbation limits, defenses, and evaluation wrappers. They should not be presented as general-purpose robustness scores.
4. Assignment 2 includes a task-specific adaptive preprocessing transformation described in the notebook as a final micro-adjustment. Treat this as an assignment experiment, not a general model-security technique.
5. Before presenting this repository publicly or in interviews, verify that publishing the course notebooks and any associated implementation is allowed by the course's academic-integrity and intellectual-property rules.

## Suggested interview framing

Describe this as a coursework-based study of adversarial robustness, backdoor analysis, trigger reverse engineering, model fingerprinting, and image watermarking. Explain the threat model, what was implemented versus supplied by the course, the evaluation setup, and the limits of each result. Do not describe these experiments as novel research or production-ready defenses.
