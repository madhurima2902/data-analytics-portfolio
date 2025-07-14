**Supply-Chain Deliveries Forecasting — Prototype**

**Project overview**

This mini-project demonstrates how a small logistics provider can reduce stock-outs and overtime costs by producing an actionable, weekly forecast of order volume and pallet requirements.
The analysis is built entirely with Microsoft Excel (Power Query + pivots) and Power BI; no proprietary code or internal data is required.

**Business problem**

Objective

Forecast weekly order count and pallet volume for the top ten customers, achieve a forecasting error (MAPE) below 15 percent, and quantify the cost saving from a 15 percent reduction in urgent overtime and emergency replenishment.

A distribution-centre manager asked for a proof of concept before sharing confidential order files. The open dataset below mirrors their data structure, allowing a transferrable, non-disclosive prototype.

**Data source**

Dataset : Time-Series Supply-Chain Dataset – Philip Hyde

Kaggle URL : https://www.kaggle.com/datasets/philiphyde1/time-series-supply-chain-dataset

The single CSV loads directly into Excel Power Query and is small enough to refresh instantly in desktop Power BI.

**Methodology**

_1. Data preparation (Excel – Power Query)_

    Convert daily timestamps to ISO week.
    
    Filter top-ten customers by total order count.
    
    Create summary table: weekly orders, pallets, average pieces.
    

_2. Exploratory pivots (Excel)_

     Weekly trend by customer and business type.
     
     Seasonality heat-map (week vs. quarter).
     
     Initial MAPE calculation using naïve forecast.
     

_3. Forecast model_

     Excel FORECAST.ETS (additive seasonality, weekly granularity)– produces 12-week horizon.
     
     Cross-check with Power BI’s built-in forecast visual.
     

_4. Cost-of-error calculator (Excel)_

     Inputs: overtime cost per pallet, stock-out penalty.
     
     What-If slider: adjust MAPE to see annualised savings.
     

_5. Power BI dashboard_

     Tab 1: KPI cards – total weekly pallets, current MAPE, cost exposure.
     
     Tab 2: Forecast line chart with 80 % confidence band.
     
     Tab 3: “Savings Simulator” – user sets target MAPE and views projected cost reduction.
     

**Licence**

This project is released under the MIT License. The underlying dataset is distributed under the licence terms specified on its Kaggle page.
