# Gender Identification from Tweets

Predict an author's gender from their tweets using supervised, unsupervised, and deep learning approaches.

This repository contains a Jupyter notebook and utilities to preprocess tweet XMLs, train baseline models (TF‑IDF + Logistic Regression / Linear SVM), run K‑Means clustering, and train a simple Keras text classifier.

## Contents

- `gender_tweets_ml.ipynb` – main notebook with end-to-end experiments and visualizations.
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

2. Install the spaCy English model (required only if you enable lemmatization in the notebook):

```powershell
python -m spacy download en_core_web_sm
```

3. Open the notebook and run cells (VS Code or Jupyter):

```powershell
code gender_tweets_ml.ipynb
# or
jupyter notebook gender_tweets_ml.ipynb
```

## Notes

- The `environment.yml` installs `spacy` but not language models; the `python -m spacy download ...` step is required once per environment.
- If you have a small dataset, some sections (Deep Learning / evaluation splits) will be skipped; see the notebook's safety checks.
- Use a fixed `RANDOM_STATE` (default `42`) for reproducible splits and clustering.

## Reproducing results

- Ensure `truth.txt` is present at the repo root and `en/` contains XMLs for the same author ids.
- Run the notebook cells in order. The notebook includes pre-processing, baseline training, unsupervised clustering, and an optional Keras model.

## License & Contact

This project is provided as-is for demonstration and research. For issues or questions, open an issue in the repository.
