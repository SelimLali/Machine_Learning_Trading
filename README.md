# Do commodity price moves lead industry returns?

Course project for APM_5FI15_AE "ML for Trading" (ENSAE Paris, M2 SFA), Selim-Antoine Lali and Quentin Borne, October 2026.

Work in progress: the notebook currently loads the data, the analysis comes next.

## Files

- `commodities_lead_industries.ipynb`: the project notebook. It is self-contained and only uses standard scientific Python packages.
- `data/`: the datasets, cached as parquet files by the notebook on its first run and committed with it. The notebook therefore runs offline, and the numbers do not change if a source is revised or a link breaks. Deleting the folder makes the notebook download everything again.
- `environment.yml`: the conda environment used to run the notebook.

## How to run

Open the notebook from its folder and run all cells. To recreate the environment:

```bash
conda env create -f environment.yml      # creates the "ml_trading" environment
conda activate ml_trading
jupyter lab commodities_lead_industries.ipynb
```

Without the interface:

```bash
jupyter nbconvert --to notebook --execute --inplace commodities_lead_industries.ipynb
```

## Data

| Data | Source | Coverage |
|---|---|---|
| 49 industry portfolios, monthly value-weighted returns | Ken French's data library, `49_Industry_Portfolios_CSV.zip` | July 1926 onwards |
| Commodity prices, monthly averages in US dollars | World Bank Commodity Price Data ("Pink Sheet"), `CMO-Historical-Data-Monthly.xlsx` | January 1960 onwards |

Both files were downloaded on 5 November 2026.
