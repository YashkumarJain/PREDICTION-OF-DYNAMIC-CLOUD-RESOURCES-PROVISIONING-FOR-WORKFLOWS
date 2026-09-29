# Prediction of Dynamic Cloud Resource Provisioning for Workflows

An internship machine learning project exploring resource demand in virtual machine workflows. The notebook uses a dataset of CPU, memory, and network measurements to compare several classification models for resource provisioning analysis.

[Watch the project explanation and results](https://youtu.be/tFYqvblrS0w)

## Repository contents

| File | Purpose |
| --- | --- |
| `Cloud model (Ensemble).ipynb` | Data preparation, model training, and comparison |
| `Dataset.csv` | Dataset read by the notebook |
| `Internship Final Report.pdf` | Project report and methodological context |
| `Poster_Template.pptx`, `Ppt_template.pptx` | Presentation materials |

The project considers factors described in the original work, including CPU cores, CPU capacity and usage, memory capacity and usage, and network throughput. The models discussed in the repository are multilayer perceptron (MLP), gradient boosting, AdaBoost, bagging, and random forest classifiers. Consult the notebook and report for the precise target definition, preprocessing, model settings, and results; a classifier output should not be read as a direct numerical prediction of future CPU or memory units without verifying that target.

## Run the analysis

1. Clone the repository:

   ```bash
   git clone https://github.com/YashkumarJain/PREDICTION-OF-DYNAMIC-CLOUD-RESOURCES-PROVISIONING-FOR-WORKFLOWS.git
   cd PREDICTION-OF-DYNAMIC-CLOUD-RESOURCES-PROVISIONING-FOR-WORKFLOWS
   ```

2. Set up an isolated Python environment with Jupyter and the usual data science dependencies:

   ```bash
   python -m venv .venv
   # macOS / Linux
   source .venv/bin/activate
   # Windows PowerShell: .venv\Scripts\Activate.ps1
   python -m pip install jupyter numpy pandas matplotlib seaborn scikit-learn
   ```

3. Run `jupyter notebook`, open `Cloud model (Ensemble).ipynb`, and execute its cells in order. `Dataset.csv` should remain in the repository root. If the notebook refers to a machine-specific file path, change that reference to `Dataset.csv`.

The repository does not include a pinned environment file. If a notebook cell imports another package, install that package in the same environment before continuing.

## Approach

The notebook explores the dataset, prepares the measurements for learning, fits several classifiers, and compares their outputs. The accompanying report and video explain the project's motivation and displayed results. Reported performance should be interpreted in the context of the notebook's split and evaluation method; it is not evidence of a production autoscaler.

## Scope

This repository is a research and demonstration workflow. It does not provision virtual machines or connect to a cloud account. Applying a model to live scheduling would require a clearly defined target, time-aware validation, capacity constraints, and integration with an orchestration system.

## Author

[Yashkumar Jain](https://github.com/YashkumarJain)
