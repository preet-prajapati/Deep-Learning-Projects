# Deep Learning Projects

PyTorch mini projects covering tabular classification, regression, and image classification. Each project has its own notebook, data instructions, and documentation.

## Project catalog

| Category | Project | Objective |
| --- | --- | --- |
| ANN | [Date Fruit Classification](ANN/Date-Fruit-Classification/) | Predict seven date fruit varieties |
| ANN | [Power Plant Regression](ANN/Power-Plant-Regression/) | Predict power plant energy output |
| ANN | [Concrete Strength Prediction](ANN/Concrete-Strength-Prediction/) | Predict concrete compressive strength |
| CNN | [CIFAR-10 Image Classification](CNN/CIFAR10-Image-Classification/) | Classify images into ten categories |

## Repository structure

```text
ANN/
  Date-Fruit-Classification/
    README.md
    date_fruit_classification.ipynb
    date_fruit.csv
  Power-Plant-Regression/
    README.md
    power_plant_regression.ipynb
    power_plant.csv
  Concrete-Strength-Prediction/
    README.md
    concrete_strength_prediction.ipynb
    concrete_data.xls
CNN/
  CIFAR10-Image-Classification/
    README.md
    cifar10_image_classification.ipynb
requirements.txt
```

## Getting started

Use Python 3.10 or newer. From the repository root:

```bash
git clone https://github.com/preet-prajapati/Deep-Learning-Projects.git
cd Deep-Learning-Projects
python -m venv .venv
```

Activate the environment:

- Windows PowerShell: `.venv\Scripts\Activate.ps1`
- Windows Command Prompt: `.venv\Scripts\activate.bat`
- macOS/Linux: `source .venv/bin/activate`

```bash
pip install -r requirements.txt
jupyter lab
```

Open the desired project notebook and run cells in order. The notebook working directory must be its project folder; data and checkpoint paths are relative to that folder. Project READMEs explain the dataset, model, training settings, and evaluation.

## Data and generated files

The three small ANN datasets are included next to their notebooks. CIFAR-10 downloads automatically on the first CNN run. Downloaded datasets, generated model checkpoints, environments, caches, and Jupyter backups are excluded through `.gitignore`.

## Validation and scope

Notebook JSON, code-cell syntax, relative dataset paths, and documentation links are checked during organization. Model training has not been rerun. Stored notebook outputs are cleared; rerun the notebooks to generate results. Dependencies are unpinned because the original environment was not recorded. These are educational experiments; see individual READMEs for evaluation limitations.
