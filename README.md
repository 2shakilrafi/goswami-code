# Autoencoder Proof of Concept for Genomic Analysis

A research prototype exploring whether nonlinear dimensionality reduction can preserve useful cluster structure for a future genomic-analysis workflow.

## What the notebook does

[`goswami-code.ipynb`](goswami-code.ipynb) creates a synthetic dataset with 30,000 observations, compares principal component analysis with an autoencoder, and evaluates the resulting low-dimensional representations with clustering metrics. The notebook uses synthetic proxy data; it does **not** establish performance on genomic or clinical data.

The rendered [`goswami-code.pdf`](goswami-code.pdf) provides a static view of the analysis. Diagrams and fitted artifacts are retained to document the experiment.

## Run locally

The notebook metadata records Python 3.12. Create an isolated environment and install the supplied environment snapshot:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab goswami-code.ipynb
```

`requirements.txt` is a historical full-environment export and includes platform-specific package references. If installation fails, start with the notebook's direct dependencies: Jupyter, NumPy, pandas, scikit-learn, TensorFlow/Keras, Matplotlib, and Seaborn.

## Generated artifacts

Running the notebook may regenerate `feat.csv`, Keras model files, `pca_model.pkl`, and rendered figures. Review model provenance and file sizes before committing replacements.

## Scope

This repository is a proof of concept, not a validated biomedical model. Any future work with real data requires appropriate access, de-identification, validation, and domain review.
