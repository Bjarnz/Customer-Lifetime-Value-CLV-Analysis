# Customer Lifetime Value (CLV) Analysis

This project estimates the future value of customers for a UK-based online retailer using the Online Retail II dataset.  
It demonstrates a full workflow: data ingestion, customer-level aggregation, predictive modeling with BG/NBD and Gamma-Gamma, and visualization of key metrics.

## Dataset
This project uses the **Online Retail II dataset** (UK-based online retailer).  

- The full dataset can be downloaded here: [UCI Machine Learning Repository — Online Retail II](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)

## Notebooks
- `Data_Ingestion.ipynb` — Loads and stores transaction data  
- `Customer_Lifetime_Value_Analysis.ipynb` — Aggregates data, predicts customer behavior, calculates 6-month CLV, and visualizes results

## Key Insights
- Most customers make 0–2 purchases in the next 30 days (**BG/NBD**)  
- High-value wholesalers account for the majority of revenue (**Gamma-Gamma** & **CLV**)  
- 6-month CLV is highly skewed; a small number of top customers drive most expected revenue
