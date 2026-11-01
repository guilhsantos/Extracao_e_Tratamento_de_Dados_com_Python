[🇧🇷 Português](README.md) · 🇺🇸 **English**

# Data cleaning and customer RFM for e-commerce

Cleaning of a real e-commerce sales dataset covering 37 countries, plus an RFM calculation (recency, frequency, and average ticket) for each customer, ready for segmentation.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guilhsantos/Extracao_e_Tratamento_de_Dados_com_Python/blob/main/DataPreparationnapratica.ipynb)

## Problem

The raw data had unidentified customers, zero prices, and negative quantities (returns and discounts). Any analysis on top of it would show wrong numbers.

## Solution

A pandas pipeline that cleans the data, creates order value and month columns, computes RFM per customer, and generates the sales charts.

## Result

- **RFM table per customer**, exported to `e-commerce_RFM.csv`. Example: customer 12347 last bought 1 day ago, has 182 purchases, and an average ticket of 23.68.
- **Top 10 countries** by revenue and **top 10 best-selling products**.
- **Monthly sales trend**, overall and by country, showing the year's peaks and troughs.

## How I did it

1. Load and inspect: nulls, prices ≤ 0, and quantities ≤ 0.
2. Cleaning: removed nulls, returns, and outliers.
3. New columns: `TotalPrice` (quantity × price) and `YearMonth`.
4. RFM per customer: days since last purchase, number of purchases, and average value per order.
5. Bar and line charts with Seaborn and Matplotlib.

## Next step

Cluster customers on this RFM. The first version of the segmentation, done per purchase, is in [RFV_Analysis_Clustering](https://github.com/guilhsantos/RFV_Analysis_Clustering).

## Stack

Python · pandas · NumPy · Seaborn · Matplotlib · Google Colab

---

Made by [Guilherme Santos](https://portifolio-guilherme-santos.vercel.app) · [LinkedIn](https://www.linkedin.com/in/guilherme-santos-dataeng)
