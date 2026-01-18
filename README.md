# US Macro Correlation Study (CPI, Unemployment, Interest Rates)

This project analyzes the relationship between key US macroeconomic variables from 2020 to 2026:

* Inflation (CPI, monthly percentage change)
* Unemployment rate
* Short-term interest rates (Effective Federal Funds Rate)

The goal is not to predict markets, but to understand how macro variables interact over time using clean, well-aligned data.

## What the project does

1. Loads official US macroeconomic data from CSV files (FRED)
2. Filters all series to a common time period
3. Converts daily interest rate data into monthly averages
4. Computes monthly inflation from CPI
5. Aligns all variables on a common monthly timeline
6. Computes pairwise correlations
7. Visualizes the results with time series plots and a correlation heatmap

## Data sources

* CPIAUCSL: Consumer Price Index
* UNRATE: Unemployment Rate
* EFFR: Effective Federal Funds Rate
  (Source: Federal Reserve Economic Data – FRED)

## Methodology notes

* Inflation is measured month-over-month, which captures short-term price dynamics.
* Interest rates are averaged monthly to match the frequency of other macro variables.
* Correlation is used for descriptive analysis only and does not imply causality.

## Output

Running the script produces:

* Correlation values printed in the terminal
* A time-series plot of inflation, unemployment, and interest rates
* A correlation heatmap summarizing relationships between variables

## How to run

Install dependencies:

```
pip install pandas matplotlib seaborn
```

Run:

```
python main.py
```

## Limitations & extensions

This project is descriptive. Possible extensions include:

* Using inflation YoY instead of MoM
* Studying lagged relationships
* Defining macro regimes (tightening vs easing)
* Linking macro variables to asset returns

This project is intended as a learning exercise for understanding macroeconomic data handling and interpretation in a markets context.
