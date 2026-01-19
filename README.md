# US Macro Correlation Analysis (2020–2026)

This project builds a **monthly U.S. macroeconomic dataset** and studies the relationships between:

* **Inflation (CPI, Monthly % change)**
* **Unemployment Rate**
* **Effective Federal Funds Rate (EFFR)**

The objective is **educational and market-oriented**:
to demonstrate how macroeconomic data is **cleaned, aligned, and analyzed** in a way that is directly relevant for **Sales & Trading / Macro roles**.

---

## 📁 Project Structure

```
US-Macro-Correlation/
│
├── US Macro Correlation Analysis (2020–2026).ipynb
├── data/
│   ├── CPIAUCSL.csv
│   ├── UNRATE.csv
│   └── EFFR.csv
└── README.md
```

All data files must be placed inside the **`data/` folder**.
No absolute paths are used, so the project runs on **any machine**.

---

## 📊 Data Sources

All macroeconomic series are downloaded from **FRED (Federal Reserve Economic Data)**:

* **CPIAUCSL** – Consumer Price Index
* **UNRATE** – U.S. Unemployment Rate
* **EFFR** – Effective Federal Funds Rate (daily)

---

## ⚙️ Methodology

### 1️⃣ Data loading

* CSV files are loaded using **relative paths**
* Dates are parsed automatically

### 2️⃣ Frequency alignment

* CPI and unemployment are monthly
* EFFR is **daily → converted to monthly average**
* All series are aligned using a **monthly period index**

### 3️⃣ Inflation calculation

* Inflation is computed as **Month-over-Month % change**:

\[
\text{Inflation}_t = 100 \times \left( \frac{CPI_t}{CPI_{t-1}} - 1 \right)
\]


(MoM is intentionally used to capture **short-term market sensitivity**)

### 4️⃣ Correlation analysis

Pearson correlations are computed between:

* Inflation ↔ Unemployment
* Inflation ↔ Interest Rates
* Unemployment ↔ Interest Rates

### 5️⃣ Visualization

* Time-series plot of all three variables
* Correlation heatmap for quick interpretation

---

## ▶️ How to Run

### 1) Install dependencies

```bash
pip install pandas matplotlib seaborn jupyter
```

### 2) Launch Jupyter Notebook

```bash
jupyter notebook
```

### 3) Open and run

Open:

```
US Macro Correlation Analysis (2020–2026).ipynb
```

Run all cells from top to bottom.

---

## 📌 Key Takeaways

* Shows **real-world macro data handling**, not toy examples
* Focuses on **frequency alignment**, a common pitfall in macro analysis
* Highlights how inflation, labor markets, and monetary policy interact
* Directly relevant for **Sales & Trading**, **Macro Research**, and **Rates / FX desks**

---

## ⚠️ Disclaimer

This project is **descriptive** and **educational**.
Correlation does not imply causation and should not be used as an investment signal.

---

## 🚀 Possible Extensions

* Inflation YoY vs MoM comparison
* Lagged correlations (rates leading inflation)
* Regime analysis (high vs low inflation periods)
* Add asset returns (SP500, FX, Rates futures)

---

**Author:**
Youssef Triki – M1 Finance
Target roles: Sales & Trading / Macro / Markets
