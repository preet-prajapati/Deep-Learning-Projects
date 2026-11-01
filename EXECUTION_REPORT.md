# Execution Report

Run date: **1 November 2026**. All four notebooks completed their training and evaluation cells on the full datasets, with outputs and plots saved in the notebooks.

## Measured results

| Project | Training | Held-out test result |
| --- | --- | --- |
| Date Fruit Classification | 100 epochs; 718 training rows | Accuracy **92.78%** (167/180) |
| Power Plant Regression | 100 epochs; 6,123 training / 1,531 validation rows | MAE **3.5050**, RMSE **4.3862**, R² **0.9328** on 1,914 test rows |
| Concrete Strength Prediction | 100 epochs; 659 training / 165 validation rows | MAE **8.7591**, RMSE **10.9266**, R² **0.5367** on 206 test rows |
| CIFAR-10 Image Classification | 10 epochs; all 50,000 training images | Accuracy **74.46%** on all 10,000 test images |

These results describe this run, not guaranteed performance. The concrete model has substantial remaining prediction error. Its original two six-unit hidden layers and 100 epochs were deliberately retained; model tuning is separate from completing and correcting the workflow.

## Targeted changes

- Preserved all four original model class definitions, Adam optimizers, batch sizes, and epoch counts.
- Added seed initialization and retained the existing data preparation and training approach.
- Regression: split the original training partition into training and validation data (64/16/20 overall). Fit scaling only on training data. Select checkpoints on validation data and reserve the test set for final evaluation.
- Concrete: restore the best validation checkpoint before reporting test results.
- Regression: report R² as a score rather than a percentage; add MAE, RMSE, prediction scatter plots, and residual plots.
- Classification: add training curves, per-class precision/recall/F1, and confusion matrices. CNN also shows sample test images with predicted and true labels.
- CNN: explicitly enable training mode at each epoch and call `model(images)` so PyTorch module hooks work normally.
- Report epoch losses weighted by sample count, including the final partial batch.

## Environment and reproduction

The checked run used Python 3.14.6, PyTorch 2.14.1+cu130, torchvision 0.29.1+cu130, and an NVIDIA GeForce RTX 5060 Ti. ANN training ran on CPU; CNN training used CUDA. See [execution-environment.json](execution-environment.json) for package versions.

Follow the [setup guide](README.md#getting-started), open a project notebook with that project folder as its working directory, restart the kernel, and run all cells. GPU support requires a compatible PyTorch installation and driver. Results can vary with library versions and hardware despite fixed seeds.

## Verification

- All code cells have execution counts, with no notebook error outputs.
- Full training schedules completed: 100 epochs for each ANN and ten epochs for CNN.
- Notebook structures and Python syntax validated; data paths and README links checked.
- Original model class definitions compared structurally and confirmed unchanged.
- Plots checked for readable labels and valid rendered output.
- Datasets, generated checkpoints, and cached runtime files are not added to this change.
