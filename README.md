# Anticipatory Flood Action in Afghanistan Using Conformalized Quantile Rainfall Forecasting

This project explores rainfall forecasting and anticipatory flood action in Afghanistan using conformalized quantile forecasting methods. It uses subnational rainfall data to support data-driven, uncertainty-aware flood-risk preparedness.

## Data Source

The project uses the Afghanistan subnational rainfall dataset available from the Humanitarian Data Exchange (HDX):

- **Dataset:** https://data.humdata.org/dataset/afg-rainfall-subnational
- **File:** `afg-rainfall-subnat-full.csv`

The CSV contains rainfall observations aggregated for Afghanistan at subnational administrative levels. Because the file may be too large for a direct GitHub upload, it is not currently stored in this repository. Download the CSV from HDX and place it in the `Data/` folder before running the analysis.

## Project Structure

```text
.
├── Data/
│   └── ReadMe
├── README.md
└── (analysis, notebooks, or model scripts)
```

## Getting Started

1. Download `afg-rainfall-subnat-full.csv` from the HDX dataset page.
2. Place the downloaded file in the `Data/` directory:

   ```text
   Data/afg-rainfall-subnat-full.csv
   ```

3. Install the dependencies required by the project's analysis scripts or notebooks.
4. Run the forecasting or modeling workflow described in the repository.

## Objective

The goal is to forecast rainfall while accounting for uncertainty, then use the predicted probability intervals to inform anticipatory flood-action decisions.

## Data Notes

- Geographic coverage: Afghanistan
- Spatial level: Subnational administrative areas
- Data format: CSV
- Source: Humanitarian Data Exchange
- The original source should be consulted for the latest file version, field definitions, and update date.

## License

Check the license and terms displayed on the [HDX dataset page](https://data.humdata.org/dataset/afg-rainfall-subnational) before redistributing or republishing the data.
