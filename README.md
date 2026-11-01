# Deep Learning Projects

A collection of PyTorch mini projects covering artificial neural networks (ANN) and convolutional neural networks (CNN).

## Projects

| Folder | Notebook | Description |
| --- | --- | --- |
| ANN | [ANN_Classification.ipynb](ANN/ANN_Classification.ipynb) | Date fruit classification using scaling, PCA, and a neural network. |
| ANN | [ANN_Regression.ipynb](ANN/ANN_Regression.ipynb) | Power plant energy output prediction. |
| ANN | [Concrete_Strength_Prediction.ipynb](ANN/Concrete_Strength_Prediction.ipynb) | Concrete compressive strength prediction. |
| ANN | [Neuron.ipynb](ANN/Neuron.ipynb) | A basic PyTorch linear neuron demonstration. |
| CNN | [CNN_For_CIFAR10.ipynb](CNN/CNN_For_CIFAR10.ipynb) | CIFAR-10 image classification with a convolutional neural network. |

## Getting started

Use Python 3.10 or newer in a virtual environment:

```bash
python -m venv .venv
```

Activate on Windows with `.venv\Scripts\activate`, or on macOS/Linux with `source .venv/bin/activate`.

```bash
pip install -r requirements.txt
jupyter lab
```

Open a notebook from its ANN or CNN folder and run its cells in order. Relative data paths assume the notebook's own folder is the working directory.

ANN tabular datasets are included alongside the notebooks. The CNN notebook automatically downloads CIFAR-10 into `CNN/data` on first run; an internet connection is required. Downloaded image data, Jupyter backups, and future generated checkpoints are ignored by Git.

The original `ANN/best_model.pt` checkpoint is included. Both ANN regression notebooks write `best_model.pt` in the ANN folder, so rerunning them can replace that checkpoint. Run the relevant model definition and training cells before loading a checkpoint.

## Dependencies and validation

Dependencies are listed in `requirements.txt` without version pins because the original projects did not include an environment lockfile. Notebook JSON and Python cell syntax were checked during import; training was not rerun and saved metrics are historical notebook output.
