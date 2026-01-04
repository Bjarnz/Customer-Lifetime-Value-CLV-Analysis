# Customer Lifetime Value (CLV) Analysis

## Project Overview
This project estimates the future value of customers for a UK-based online retailer using transaction-level data from the Online Retail II dataset.  
It demonstrates a full workflow: data ingestion, customer-level aggregation, predictive modeling with BG/NBD and Gamma-Gamma, visualization of key metrics, and business insights to identify high-value customers.

## Objective
Understand customer purchase behavior and predict future revenue to inform retention strategies and business decision-making.

## Dataset
- **Source:** Online Retail II (UK-based online retailer)  
- **Fields:**
  - `Invoice` — invoice number  
  - `StockCode` — product identifier  
  - `Description` — product description  
  - `Quantity` — units purchased  
  - `InvoiceDate` — date/time of purchase  
  - `Price` — unit price  
  - `Customer ID` — unique customer identifier  
  - `Country` — country of purchase

## Notebooks / Workflow
1. **`Data_Ingestion.ipynb`** — Load raw CSV into SQLite database for consistent data access.  
2. **`Customer_Lifetime_Value_Analysis.ipynb`** —  
   - Aggregate transaction data to customer-level RFM metrics  
   - Fit **BG/NBD** model to predict future purchase frequency  
   - Fit **Gamma-Gamma** model to estimate expected transaction value  
   - Compute **6-month CLV** and identify top customers  
   - Visualize distributions of predicted purchases and CLV (capped at 95th percentile)  
   - Provide actionable business insights

## Key Insights
- Most customers are predicted to make 0–2 purchases in the next 30 days (**BG/NBD**), while a small group of frequent buyers, likely wholesalers, accounts for much higher purchase volumes.  
- Average transaction values vary widely across customers (**Gamma-Gamma**), reflecting a mix of small and high-value wholesale purchases.  
- The 6-month CLV highlights that top customers contribute a disproportionately large share of expected revenue (**CLV**), with a highly skewed distribution.  
- **Overall:** A small number of high-frequency, high-value customers drive the majority of revenue, making them the most impactful segment for targeted retention and engagement efforts.

## Tools & Libraries
- Python 3.x  
- pandas, numpy  
- lifetimes (BG/NBD and Gamma-Gamma models)  
- matplotlib  
- SQLite

## How to Run
1. Open and run `Data_Ingestion.ipynb` to load the dataset into SQLite.  
2. Open and run `Customer_Lifetime_Value_Analysis.ipynb` to perform aggregation, modeling, visualization, and generate insights.  
3. Review the tables and figures for top customers and overall CLV distribution.
