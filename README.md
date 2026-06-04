# Carbon Emission Dataset Analysis

This repository contains a complete solution for the **Advanced Python Project: Carbon Emission Dataset** assignment. The project analyzes the public Kaggle file `carbon_emission_dataset_with_Industry.csv` using **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, **SciPy**, and **Statsmodels**.

The analysis includes data cleaning, exploratory data analysis, statistical analysis, correlation heatmap, pairplot, boxplots, time-series analysis, moving averages, rolling variance, time-series decomposition, and answers to the five required analytical questions.

## Dataset

The required dataset is the public Kaggle dataset **Carbon Emission Forecasting Dataset** by Freshers Staff. The CSV used in this project is:

```text
data/raw/carbon_emission_dataset_with_Industry.csv
```

The target variable is:

```text
Carbon_Emission_tCO2e_TARGET
```

## Project Structure

```text
carbon_project/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/
│   │   ├── carbon_emission_dataset_with_Industry.csv
│   │   └── carbon_dataset.zip
│   └── processed/
│       ├── carbon_emission_cleaned.csv
│       └── daily_time_series.csv
├── notebooks/
│   └── carbon_emission_analysis.ipynb
├── reports/
│   ├── Carbon_Emission_Report_Summary.md
│   ├── Carbon_Emission_Report_Summary.pdf
│   ├── analysis_summary.json
│   ├── correlation_matrix.csv
│   ├── emissions_by_sector.csv
│   ├── emissions_by_industry_sector.csv
│   ├── source_variability.csv
│   └── figures/
│       ├── 01_required_feature_distributions.png
│       ├── 02_categorical_frequency_bars.png
│       ├── 03_energy_line_over_time.png
│       ├── 04_emissions_vs_time_scatter.png
│       ├── 06_emission_source_pair_comparison.png
│       ├── 07_correlation_heatmap.png
│       ├── 08_emissions_boxplot_by_industry.png
│       ├── 09_numeric_boxplots.png
│       ├── 10_selected_features_pairplot.png
│       ├── 11_group_based_emissions.png
│       ├── 12_emissions_time_series_moving_averages.png
│       ├── 13_rolling_variance.png
│       └── 14_time_series_decomposition.png
└── src/
    ├── analysis.py
    ├── create_notebook.py
    └── create_report.py
```

## Setup Instructions

Create a virtual environment if desired, then install the dependencies:

```bash
pip install -r requirements.txt
```

## How to Run the Project

Run the full analysis script from the project root:

```bash
python src/analysis.py
```

Generate the notebook if needed:

```bash
python src/create_notebook.py
```

Generate the Markdown report if needed:

```bash
python src/create_report.py
```

The required Jupyter Notebook is located at:

```text
notebooks/carbon_emission_analysis.ipynb
```

The required PDF report summary is located at:

```text
reports/Carbon_Emission_Report_Summary.pdf
```

## Key Findings

The dataset contains 18,250 records with no missing values in the original columns. The analysis found that **NonRenewable_Energy_Consumption_kWh** has the strongest correlation with carbon emissions, followed by **Carbon_Tax_USD** and **Total_Energy_Consumption_kWh**. Emissions are not normally distributed under the D’Agostino-Pearson normality test. The time-series analysis indicates a modest upward trend across the year, while decomposition suggests only a weak seasonal component.

## Assignment Coverage

| Required Item | Included |
|---|---|
| Load and inspect dataset | Yes |
| Show first rows, info, describe | Yes |
| Handle missing values and datatypes | Yes |
| Basic statistics | Yes |
| Distributions | Yes |
| Frequency bar charts | Yes |
| Energy line plot over time | Yes |
| Scatter plots | Yes, except temperature because no temperature column exists |
| Compare emission-source pairs | Yes |
| Correlation heatmap | Yes |
| Boxplots | Yes |
| Pairplot | Yes |
| Group-based analysis | Yes |
| Time-series analysis | Yes |
| Moving averages | Yes |
| Rolling variance | Yes |
| Time-series decomposition | Yes |
| Analytical questions | Yes |
| PDF report | Yes |
| GitHub-ready structure | Yes |

## Note on Temperature Analysis

The assignment document requests an emissions-versus-temperature plot and a temperature trend over time. The provided CSV does not contain a temperature column. The notebook checks for temperature-like columns automatically and reports this limitation clearly.
