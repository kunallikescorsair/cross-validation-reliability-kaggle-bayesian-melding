# Results

This directory contains experiment outputs and final research datasets used in the analysis.

## Directory Structure

- `santander/`: Santander Customer Transaction Prediction experiment outputs
- `porto/`: Porto Seguro's Safe Driver Prediction experiment outputs
- `homesite/`: Homesite Quote Conversion experiment outputs
- `combined/`: Final combined datasets and summary outputs used in the research report

## Per-Competition Outputs

Each competition directory contains files such as:

- `*_1000_model_configs.csv`: Generated model configurations
- `*_1000_model_results.csv`: Stratified 5-fold cross-validation results for 1,000 model configurations
- `*_leaderboard_scores.csv`: Public and private leaderboard scores for the selected representative models
- `*_final_research_dataset.csv`: Final leaderboard-scored dataset used for validation reliability analysis
- `manual_submission_plan_100.csv`: Representative 100-model leaderboard submission plan

## Combined Outputs

The `combined/` directory contains the final datasets used in the research report:

- `combined_full_cv_population_dataset.csv`: Full 3,000-model cross-validation population
- `combined_final_research_dataset.csv`: 300 leaderboard-scored models with cross-validation, public leaderboard, and private leaderboard scores
- `combined_bayesian_melding_output.csv`: Bayesian melding posterior output
- `full_cv_population_summary.csv`: Full cross-validation population summary by competition and model family
- `leaderboard_scored_summary.csv`: Leaderboard-scored summary by competition
- `leaderboard_scored_summary_by_family.csv`: Leaderboard-scored summary by model family
- `correlation_analysis.csv`: Pearson and Spearman correlation analysis
- `centered_correlation_analysis.csv`: Within-competition centred correlation analysis
- `gap_summary_by_competition.csv`: Validation gap summary by competition
- `gap_summary_by_model_family.csv`: Validation gap summary by model family
- `posterior_summary_by_competition.csv`: Bayesian posterior summary by competition
- `posterior_summary_by_model_family.csv`: Bayesian posterior summary by model family