# CIFAR-10 Image Classification

Classify 32 x 32 RGB images into ten CIFAR-10 categories.

## Files

- [cifar10_image_classification.ipynb](cifar10_image_classification.ipynb): complete data preparation, model, training, and evaluation workflow.

## Setup and execution

1. Create and activate a Python environment using the [repository setup guide](../../README.md#getting-started).
2. Install dependencies from the repository root: `pip install -r requirements.txt`.
3. Start `jupyter lab`, open this project's notebook, and use this project folder as the notebook working directory.
4. Run all cells from top to bottom. Restart the kernel before switching experiments.

## Data

CIFAR-10 downloads automatically through torchvision into `./data` on first run. Internet access is required for the initial download. Downloaded data is excluded from Git.

## Workflow

- **Preparation:** torchvision CIFAR10 with tensor conversion and per-channel normalization using mean 0.5 and standard deviation 0.5.
- **Architecture:** Three convolution/ReLU/max-pooling blocks (32, 64, 128 channels), followed by a 256-unit ReLU layer and ten class logits.
- **Training:** Cross-entropy loss, Adam, ten epochs, batch size 64; official training and test splits. Uses CUDA when available, otherwise CPU.
- **Evaluation:** Test-set accuracy.

## Reproducibility and limitations

These are learning projects. Training has not been rerun as part of repository organization; no new performance claims are made. Outputs are cleared so a fresh run produces its own results.

Dependencies are shared in the root `requirements.txt`; versions are not pinned because the source projects had no recorded environment. Training is stochastic and results may vary. Included tabular files retain their original contents; dataset provenance and redistribution terms were not supplied with the source projects.
