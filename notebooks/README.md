# Notebooks

This directory contains the main experiment and analysis notebooks used in the research project.

## Notebook Order

1. `01_santander_experiments.ipynb`

   Runs the Santander Customer Transaction Prediction experiments, including model configuration generation, stratified 5-fold cross-validation, leaderboard submission preparation, leaderboard score integration, and final Santander research dataset construction.

2. `02_porto_experiments.ipynb`

   Runs the Porto Seguro's Safe Driver Prediction experiments, including model configuration generation, stratified 5-fold cross-validation, leaderboard submission preparation, leaderboard score integration, and final Porto research dataset construction.

3. `03_homesite_experiments.ipynb`

   Runs the Homesite Quote Conversion experiments, including model configuration generation, stratified 5-fold cross-validation, leaderboard submission preparation, leaderboard score integration, and final Homesite research dataset construction.

4. `04_final_analysis_bayesian_melding.ipynb`

   Combines the final competition datasets, constructs the full 3,000-model cross-validation population, computes validation reliability metrics, performs correlation and gap analysis, and applies Bayesian melding to estimate latent model performance.

## Notes

The first three notebooks are competition-specific experiment notebooks.

The final analysis notebook reads from:

- `results/santander/`
- `results/porto/`
- `results/homesite/`

and writes final combined outputs to:

- `results/combined/`

The final CSV outputs are already included in the repository so that the analysis can be inspected without rerunning all 3,000 model configurations.