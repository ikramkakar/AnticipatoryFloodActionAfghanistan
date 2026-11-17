# Anticipatory Flood Action in Afghanistan Using Conformalized Quantile Rainfall Forecasting

A data analysis project applying rainfall forecasting and uncertainty quantification to support anticipatory flood action in Afghanistan. The repository compares statistical and neural forecasting approaches and evaluates uncertainty-aware decision triggers at the provincial level.

The main analysis uses 10-day rainfall forecasts with prediction intervals to identify periods when drought- or flood-related early action may be warranted.

## Highlights

- Forecasts 10-day rainfall at Afghanistan subnational administrative levels
- Compares SARIMA, RNN, LSTM, and quantile-LSTM approaches
- Uses conformalized prediction intervals to quantify forecast uncertainty
- Evaluates cost-loss decision policies for anticipatory action
- Includes provincial case studies and reproducible model outputs

## Repository Structure

```text
.
├── Data/
│   ├── afg-rainfall-subnat-full.csv
│   └── ReadMe
├── Figures/
│   ├── acf.png
│   ├── decomposition.png
│   ├── decision_triggers.png
│   ├── quantile_lstm_intervals.png
│   └── provincial_case_study.png
├── Notebooks/
│   └── Forecasting_10_day_rainfall_with_prediction_intervals_to_trigger_early_action_on_drought_and_floods_in_Afghanistan.ipynb
├── Report/
│   └── Anticipatory_Flood_Action_in_Afghanistan_Using_Conformalized_Quantile_Rainfall_Forecasting.pdf
└── Results/
    ├── nn_validation_tuning.csv
    ├── provincial_case_study.csv
    ├── table2_test_point_models.csv
    └── table3_cost_loss_policies.csv
```

## Main Notebook

Open [`Forecasting_10_day_rainfall_with_prediction_intervals_to_trigger_early_action_on_drought_and_floods_in_Afghanistan.ipynb`](Notebooks/Forecasting_10_day_rainfall_with_prediction_intervals_to_trigger_early_action_on_drought_and_floods_in_Afghanistan.ipynb).

The notebook covers data preparation, time-series analysis, baseline and neural forecasts, prediction intervals, and evaluation of decision triggers.

## Data

The project uses the [Afghanistan Subnational Rainfall dataset](https://data.humdata.org/dataset/afg-rainfall-subnational) distributed by the Humanitarian Data Exchange (HDX).

- File: `Data/afg-rainfall-subnat-full.csv`
- Geographic coverage: Afghanistan
- Spatial level: Subnational administrative areas
- Format: CSV
- Provider: Humanitarian Data Exchange (OCHA / HDX)

Additional data notes are available in [`Data/ReadMe`](Data/ReadMe). Consult the original HDX dataset for the latest version, field definitions, licensing terms, and update date.

## Reproducing the Analysis

1. Clone the repository:

   ```bash
   git clone https://github.com/ikramkakar/AnticipatoryFloodActionAfghanistan.git
   cd AnticipatoryFloodActionAfghanistan
   ```

2. Create and activate a Python environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

   On Windows, activate the environment with:

   ```powershell
   .venv\Scripts\Activate.ps1
   ```

3. Install Jupyter and the libraries imported by the notebook. For example:

   ```bash
   pip install jupyter pandas numpy matplotlib seaborn scipy statsmodels scikit-learn torch
   ```

4. Launch Jupyter and open the main notebook:

   ```bash
   jupyter notebook Notebooks/Forecasting_10_day_rainfall_with_prediction_intervals_to_trigger_early_action_on_drought_and_floods_in_Afghanistan.ipynb
   ```

Run the notebook from top to bottom. The outputs are written to the `Figures/` and `Results/` directories where configured.

## Report and Outputs

- Full project report: [`Report/Anticipatory_Flood_Action_in_Afghanistan_Using_Conformalized_Quantile_Rainfall_Forecasting.pdf`](Report/Anticipatory_Flood_Action_in_Afghanistan_Using_Conformalized_Quantile_Rainfall_Forecasting.pdf)
- Forecast diagnostics and model visualizations: [`Figures/`](Figures)
- Validation, provincial case-study, model-comparison, and policy tables: [`Results/`](Results)

## Methods

The analysis combines conventional time-series forecasting with deep learning and calibrated uncertainty estimates. Conformalized quantile forecasting provides prediction intervals, while cost-loss policy evaluation examines how uncertainty-aware triggers could be translated into decision thresholds for different provinces and action costs.

## Project Status

This repository contains the research notebook, generated tables and figures, report, and source rainfall data. Results should be interpreted in the context of the study period, administrative aggregation, forecast horizon, and available observations.

## License

No separate software license is included in this repository. The rainfall data and downstream outputs remain subject to the terms of their respective data providers and original sources. Check the [HDX dataset page](https://data.humdata.org/dataset/afg-rainfall-subnational) before redistributing or republishing the data.
