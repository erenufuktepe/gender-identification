# Gender Identification from Tweets

Predict an author's gender from their tweets using supervised, unsupervised, and deep learning approaches.

This repository contains a Jupyter notebook and utilities to preprocess tweet XMLs, train baseline models (TF‑IDF + Logistic Regression / Linear SVM), run K‑Means clustering, and train a simple Keras text classifier.

## Contents

- `gender_identification.ipynb` – main notebook with end-to-end experiments and visualizations.
- `en/` – directory with XML files containing tweet documents (one file per author).
- `environment.yml` – conda environment specification for reproducible setup.

## Dataset

- The project expects labeled authors in `truth.txt` (format: `id:::gender:::country` per line).
- The raw tweet content for each author is stored under `en/<id>.xml`.

## Quickstart

1. Create and activate the conda environment:

```powershell
conda env update -f environment.yml
conda activate gender-identification
```

2. Open the notebook and run cells (VS Code or Jupyter):

```powershell
code gender_identification.ipynb
# or
jupyter notebook gender_identification.ipynb
```
