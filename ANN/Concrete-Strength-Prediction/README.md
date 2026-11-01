# Concrete Strength Prediction

Predict concrete compressive strength from eight mixture and age features.

## Files

- [concrete_strength_prediction.ipynb](concrete_strength_prediction.ipynb): complete data preparation, model, training, and evaluation workflow.
- [concrete_data.xls](concrete_data.xls): input dataset.

## Setup and execution

1. Create and activate a Python environment using the [repository setup guide](../../README.md#getting-started).
2. Install dependencies from the repository root: `pip install -r requirements.txt`.
3. Start `jupyter lab`, open this project's notebook, and use this project folder as the notebook working directory.
4. Run all cells from top to bottom. Restart the kernel before switching experiments.

## Data

`concrete_data.xls` is included beside the notebook. Keep it in this folder so the relative file path resolves.

## Workflow

- **Preparation:** A 64/16/20 train/validation/test split (random_state=42) and standardization fitted only on training data.
- **Architecture:** A feedforward ANN with two six-unit ReLU hidden layers and one regression output.
- **Training:** Mean squared error loss, Adam, 100 epochs, batch size 32. A separate validation split selects the best checkpoint; the test set is reserved for final evaluation.
- **Evaluation:** MSE, MAE, RMSE, R-squared, loss curves, predicted versus actual values, and residual plots.

## Reproducibility and limitations

These are learning projects. All training and evaluation cells were executed on 1 November 2026; the notebook includes the resulting outputs and plots. See the [execution report](../../EXECUTION_REPORT.md) for measured results and environment details. The best validation checkpoint is loaded before final evaluation on the independent test set. Training writes `best_model.pt` inside this project folder; checkpoints are generated artifacts and are excluded from Git.

Dependencies are shared in the root `requirements.txt`. The exact environment used for the checked run is recorded in `execution-environment.json` at the repository root. Training is stochastic and results may vary. Included tabular files retain their original contents; dataset provenance and redistribution terms were not supplied with the source projects.
