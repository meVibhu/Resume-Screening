# Resume Screening

A machine learning mini lab for automated resume screening.

This repository contains:

- `final-ml-fixed.ipynb` — a Jupyter notebook that loads the resume dataset, performs EDA, preprocessing, model training, evaluation, and deployment utilities.
- `resume_dataset_200k_enhanced.csv` — the dataset used by the notebook.

## Project Overview

The notebook is built to:

- load and inspect a large candidate resume dataset
- identify the target and feature columns automatically
- clean data, impute missing values, remove duplicates, and cap outliers
- encode categorical data and scale numeric features
- optionally vectorize text if a resume/text column is present
- train Logistic Regression, Decision Tree, and Random Forest models
- evaluate model performance with accuracy, precision, recall, F1 score, confusion matrices, and ROC curves
- save trained artifacts and expose a prediction helper function

## Setup

Use a virtual environment for best results.

```bash
cd /Users/vaibhavsharma/Resume-screening
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install notebook wordcloud imbalanced-learn numpy pandas matplotlib seaborn scikit-learn scipy joblib
```

If you already installed dependencies globally, you can skip the environment creation step.

## Run the Notebook

Start Jupyter Notebook from the repo root:

```bash
source .venv/bin/activate
python -m notebook
```

Then open `final-ml-fixed.ipynb` in the browser.

## Recommended VS Code Workflow

1. Open this folder in VS Code.
2. Open `final-ml-fixed.ipynb`.
3. In the notebook kernel selector, choose the `.venv` Python interpreter.
4. Run the cells from top to bottom.

## Dataset Path

The notebook expects the dataset at:

```python
FILE_PATH = "./resume_dataset_200k_enhanced.csv"
```

So keep the CSV file in the same folder as the notebook.

## Notes

- If `pip` is unavailable in your shell, use `python3 -m pip`.
- Avoid running `pip` as root; use the virtual environment instead.
- If the notebook fails due to missing packages, install them inside `.venv` and restart the kernel.

## License

This repository is provided as-is for learning and experimentation.
