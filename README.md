# Spatiotemporally explicit machine learning estimates for U.S. residential electricity consumption from 2009–2022

Open the scripts in `src/` with Python 3.11 and install `requirements.txt`.

Clone this repository with Git LFS installed and run `git lfs pull` to download the prediction inputs.

## Data

- `data/training/`: four seasonal county–month tables.
- `data/prediction/`: four seasonal tract-year-month predictor tables.
- `data/processed/`: Figure 2 and Tables S2–S6.
- `data/predictor_dictionary.csv`: predictor definitions and sources.

## Scripts

1. `01_Model_training_and_prediction.ipynb` — model fitting, full-sample refitting, and tract prediction.
2. `02_Performance_and_explanations.ipynb` — held-out evaluation, permutation importance, SHAP, and Figures 3–5/S1–S3.
3. `03_Maps_and_tables.ipynb` — Figure 2 and Tables S2–S6.
4. `04_External_validation.ipynb` — LEAD/EIA comparisons and Figures 6–7.

Set the same `WORK_DIR`, which defaults to `Code_run/`: models are in `models/`, tract predictions in `predictions/`, and intermediate result files directly in `WORK_DIR` with branch and season in their names.

## External inputs

Low-Income Energy Affordability Data (LEAD) Tool/U.S. Energy Information Administration (EIA) benchmark files and geographic boundaries are not included. Sources are [LEAD](https://doi.org/10.25984/1784729), [EIA electricity data](https://www.eia.gov/electricity/data.php#sales), and [Census TIGER/Line](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html).

Download the required files separately and set their relative filenames under `external/validation/` and `external/boundaries/` for mapping and external validation purposes.
