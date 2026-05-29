# Evaluating Cross-Validation Reliability in Kaggle Tabular Binary Classification Competitions Using Bayesian Melding

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20444020.svg)](https://doi.org/10.5281/zenodo.20444020)

This repository contains the code, experiment outputs, figures, and final preprint report for a machine learning research project investigating the reliability of stratified cross-validation in Kaggle tabular binary classification competitions.

The study evaluates whether cross-validation AUC and public leaderboard AUC reliably predict hidden private leaderboard AUC. It uses an empirical Bayesian melding framework to model cross-validation, public leaderboard, and private leaderboard scores as noisy observations of latent true model performance.

## Research Summary

Three completed Kaggle tabular binary classification competitions were analysed:

- Santander Customer Transaction Prediction
- Porto Seguro's Safe Driver Prediction
- Homesite Quote Conversion

For each competition, 1,000 controlled model configurations were trained and evaluated using stratified 5-fold cross-validation. A representative subset of 100 models per competition was then submitted to Kaggle to collect public and private leaderboard scores.

Final experimental scale:

- 3 competitions
- 3,000 cross-validation observations
- 300 leaderboard-scored models
- 6 model families
- Bayesian melding validation analysis

## Model Families

The experiments include:

- LightGBM
- XGBoost
- CatBoost
- Random Forest
- ExtraTrees
- Logistic Regression

## Main Analysis

The project investigates:

- Cross-validation reliability
- Public leaderboard reliability
- Private leaderboard agreement
- CV-private leaderboard gaps
- Public-private leaderboard gaps
- Model-family-level validation behaviour
- Bayesian melding posterior performance estimates

## Repository Structure

```text
.
├── data/
│   └── README.md
├── figures/
│   ├── figure1_workflow.png
│   ├── figure2_cv_distribution.png
│   ├── figure3_cv_private_scatter.png
│   ├── figure4_public_private_scatter.png
│   ├── figure5_gap_by_competition.png
│   ├── figure6_gap_by_model_family.png
│   └── figure7_posterior_vs_private.png
├── notebooks/
│   ├── README.md
│   ├── 01_santander_experiments.ipynb
│   ├── 02_porto_experiments.ipynb
│   ├── 03_homesite_experiments.ipynb
│   └── 04_final_analysis_bayesian_melding.ipynb
├── reports/
│   └── final_report.pdf
├── results/
│   ├── README.md
│   ├── santander/
│   ├── porto/
│   ├── homesite/
│   └── combined/
├── submissions/
│   └── README.md
├── LICENSE
├── README.md
└── requirements.txt
````

## Key Outputs

The main final research datasets are stored in `results/combined/`:

* `combined_full_cv_population_dataset.csv`
* `combined_final_research_dataset.csv`
* `combined_bayesian_melding_output.csv`
* `correlation_analysis.csv`
* `centered_correlation_analysis.csv`
* `gap_summary_by_competition.csv`
* `gap_summary_by_model_family.csv`
* `posterior_summary_by_competition.csv`
* `posterior_summary_by_model_family.csv`

## Final Report

The polished IEEE-style preprint / technical report is available at:

```text
reports/final_report.pdf
```

## Citation

If you use or refer to this project, please cite:

```text
Gurung, K. (2026). Evaluating Cross-Validation Reliability in Kaggle Tabular Binary Classification Competitions Using Bayesian Melding (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.20444021
```

BibTeX:

```bibtex
@software{gurung_2026_cv_reliability,
  author = {Gurung, Kunal},
  title = {Evaluating Cross-Validation Reliability in Kaggle Tabular Binary Classification Competitions Using Bayesian Melding},
  version = {v1.0.0},
  year = {2026},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.20444021},
  url = {https://doi.org/10.5281/zenodo.20444021}
}
```

For the latest version of the archived repository, use the all-versions DOI:

```text
https://doi.org/10.5281/zenodo.20444020
```

## Data Access

Raw Kaggle datasets are not included in this repository due to competition data access terms and file size considerations.

To reproduce the experiments, download the original datasets directly from Kaggle and place them under the appropriate `data/` subdirectories as described in `data/README.md`.

Expected local raw data structure:

```text
data/
├── santander/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── porto/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
└── homesite/
    ├── train.csv
    ├── test.csv
    └── sample_submission.csv
```

These raw files are intentionally excluded from version control.

## Reproducibility Notes

The notebooks in this repository contain the main experiment and analysis workflows. The final CSV outputs are included to make the research results inspectable without rerunning all 3,000 model configurations.

Some Kaggle leaderboard scores were manually verified because automated submission of large batches was limited by Kaggle submission-rate constraints.

The default experiment notebooks are configured with safe run settings to avoid accidental large-scale reruns or Kaggle submissions. Reproduction requires manually setting experiment ranges and configuring Kaggle access.

## Environment

The project was developed using Python 3.11.4.

Install dependencies with:

```bash
pip install -r requirements.txt
```

## License

This project is released under the license provided in `LICENSE`.

The archived release is available through Zenodo under DOI:

```text
10.5281/zenodo.20444021
```

## Author

Kunal Gurung
Master of Data Science and Innovation
University of Technology Sydney