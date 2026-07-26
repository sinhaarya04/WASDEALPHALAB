<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Data-USDA%20WASDE-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Markets-Corn%20%7C%20Soybean%20%7C%20Wheat-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Alpha%20Research-purple?style=for-the-badge" />
</p>

<h1 align="center">🌽 WASDE Alpha Lab</h1>

<p align="center">
  <b>Mining the USDA's monthly WASDE report for tradeable signals in grain futures</b>
</p>

---

## 🔍 What it does

Once a month, the USDA drops the **World Agricultural Supply and Demand Estimates (WASDE)** — and grain futures move. This lab builds the data infrastructure to study *how* corn, soybean, and wheat futures respond to WASDE surprises, and whether the futures curve carries predictable structure around report dates.

## ⚙️ The research pipeline

The notebooks form an ordered pipeline from raw files to analysis:

| Notebook | What it does |
|---|---|
| `02_build_base_tables.ipynb` | Turn raw futures + fundamentals files into clean base tables |
| `03_curve_and_spread_features.ipynb` | Engineer futures-curve features: calendar spreads, carry, curve shape |
| `04_wasde_alignment.ipynb` | Align WASDE release dates with market data for event-study analysis |
| `05_visualizations.ipynb` | Visualize curve behavior and WASDE responses |

## 📁 Data layout

```
├── raw/
│   ├── futures/          # corn / soybean / wheat contract prices
│   ├── fundamentals/     # wasde / macro series
│   └── reference_pdfs/   # source WASDE documents
├── processed/
│   ├── base_tables/      # cleaned panel data
│   ├── curve_tables/     # curve & spread features
│   └── wasde_aligned/    # event-aligned datasets
└── notebooks/            # the pipeline above
```

## 🚀 Getting started

```bash
git clone https://github.com/sinhaarya04/WASDEALPHALAB.git
cd WASDEALPHALAB
pip install pandas numpy matplotlib jupyter
jupyter notebook notebooks/
```

Run notebooks in numeric order — each stage writes the inputs for the next.

## 🧰 Tech stack

`pandas` · `numpy` · `matplotlib` · `jupyter`

---

<p align="center"><i>Research project — not investment advice.</i></p>
