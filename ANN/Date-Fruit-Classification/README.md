# Date Fruit Classification

Classify date fruit varieties from numerical measurements.

## Files

- [date_fruit_classification.ipynb](date_fruit_classification.ipynb): complete data preparation, model, training, and evaluation workflow.
- [date_fruit.csv](date_fruit.csv): input dataset.

## Setup and execution

1. Create and activate a Python environment using the [repository setup guide](../../README.md#getting-started).
2. Install dependencies from the repository root: `pip install -r requirements.txt`.
3. Start `jupyter lab`, open this project's notebook, and use this project folder as the notebook working directory.
4. Run all cells from top to bottom. Restart the kernel before switching experiments.

## Data

`date_fruit.csv` is included beside the notebook. Keep it in this folder so the relative file path resolves.

## Workflow

- **Preparation:** StandardScaler fitted on training data, label encoding, PCA retaining 95% variance, and a 34-feature input dataset.
- **Architecture:** A feedforward ANN with two 64-unit ReLU hidden layers and seven output classes.
- **Training:** Cross-entropy loss, Adam, 100 epochs, batch size 32; stratified 80/20 train/test split (random_state=42).
- **Evaluation:** Test-set accuracy.

## Reproducibility and limitations

These are learning projects. Training has not been rerun as part of repository organization; no new performance claims are made. Outputs are cleared so a fresh run produces its own results.

Dependencies are shared in the root `requirements.txt`; versions are not pinned because the source projects had no recorded environment. Training is stochastic and results may vary. Included tabular files retain their original contents; dataset provenance and redistribution terms were not supplied with the source projects.
