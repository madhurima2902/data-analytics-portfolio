# Supply-Chain Deliveries Forecasting — Prototype

## Project Overview

This mini-project demonstrates how a small logistics provider can reduce stock-outs and overtime costs by producing an actionable, weekly forecast of order volume and pallet requirements. The analysis is built entirely with **Microsoft Excel (Power Query + Pivot Tables)** and **Power BI**—no proprietary code or internal data is required.

---

## Business Problem

### Objective

Forecast weekly order count and pallet volume for the **top ten customers**, achieve a forecasting error (MAPE) below **15%**, and quantify the cost savings from a **15% reduction** in urgent overtime and emergency replenishment.

A distribution-centre manager requested a proof of concept before sharing confidential order files. The open dataset used mirrors their data structure, enabling a **transferable, non-disclosive prototype**.

---

## Data Source

- **Dataset**: Time-Series Supply-Chain Dataset – *Philip Hyde*  
- **Kaggle URL**: [https://www.kaggle.com/datasets/philiphyde1/time-series-supply-chain-dataset](https://www.kaggle.com/datasets/philiphyde1/time-series-supply-chain-dataset)

The single CSV file loads directly into Excel Power Query and refreshes instantly in desktop Power BI.

---

## Methodology

### 1. Data Preparation (Excel – Power Query)
- Convert daily timestamps to ISO week format  
- Filter top-ten customers by total order count  
- Create summary table with: weekly orders, pallets, and average pieces  

### 2. Exploratory Pivots (Excel)
- Weekly trend by customer and business type  
- Seasonality heatmap (week vs. quarter)  
- Initial MAPE calculation using naïve forecast  

### 3. Forecast Model
- **Excel FORECAST.ETS** (additive seasonality, weekly granularity) – 12-week forecast horizon  
- Cross-check with Power BI’s built-in forecast visual  

### 4. Cost-of-Error Calculator (Excel)
- Inputs: overtime cost per pallet, stock-out penalty  
- What-If slider: adjust MAPE to see annualised savings  

### 5. Power BI Dashboard
- Tab 1: KPI cards – total weekly pallets, current MAPE, cost exposure  
- Tab 2: Forecast line chart with 80% confidence band  
- Tab 3: “Savings Simulator” – user sets target MAPE and views projected cost reduction  

---

## License

This project is released under the **MIT License**.  
The dataset is distributed under the license terms specified on its [Kaggle page](https://www.kaggle.com/datasets/philiphyde1/time-series-supply-chain-dataset).
