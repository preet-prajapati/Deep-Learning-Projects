# Power Plant Energy Prediction

Predict power plant energy output (PE) from temperature (AT), exhaust vacuum (V), pressure (AP), and humidity (RH).

## Files

- [power_plant_regression.ipynb](power_plant_regression.ipynb): complete data preparation, model, training, and evaluation workflow.
- [power_plant.csv](power_plant.csv): input dataset.

## Setup and execution

1. Create and activate a Python environment using the [repository setup guide](../../README.md#getting-started).
2. Install dependencies from the repository root: `pip install -r requirements.txt`.
3. Start `jupyter lab`, open this project's notebook, and use this project folder as the notebook working directory.
4. Run all cells from top to bottom. Restart the kernel before switching experiments.

## Data

`power_plant.csv` is included beside the notebook. Keep it in this folder so the relative file path resolves.

## Workflow

- **Preparation:** An 80/20 train/test split (random_state=42) and standardization fitted on training data.
- **Architecture:** A feedforward ANN with two six-unit ReLU hidden layers and one regression output.
- **Training:** Mean squared error loss, Adam, 100 epochs, batch size 32. The notebook uses the held-out split for validation and checkpoint selection.
- **Evaluation:** MSE, R-squared, loss curves, and predicted versus actual values.

## Reproducibility and limitations

These are learning projects. Training has not been rerun as part of repository organization; no new performance claims are made. Outputs are cleared so a fresh run produces its own results. The current validation split also serves as the evaluation split, so reported metrics are not an independent final test estimate. For a rigorous experiment, add a separate validation split for model selection. Training writes `best_model.pt` inside this project folder; checkpoints are generated artifacts and are excluded from Git.

Dependencies are shared in the root `requirements.txt`; versions are not pinned because the source projects had no recorded environment. Training is stochastic and results may vary. Included tabular files retain their original contents; dataset provenance and redistribution terms were not supplied with the source projects.
