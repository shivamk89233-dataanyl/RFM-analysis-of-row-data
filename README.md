# RFM-analysis-of-row-data
RFM-based customer segmentation in Python that scores customers on Recency, Frequency and Monetary value, groups them into segments like Champions, Loyal and At Risk, and analyzes spending by age and marital status.
# Customer Segmentation using RFM Analysis

Segments customers by purchase behaviour using RFM (Recency, Frequency, Monetary) analysis, then profiles each segment by age and marital status.
## What it does
- **Data prep:** Loads customer master and transaction data, converts date fields to datetime, and drops transactions that have no matching customer record.
- **RFM metrics:** Calculates Recency (days since the last purchase, counted from one day after the latest transaction), Frequency (number of transactions) and Monetary (total spend) for each customer.
- **Scoring:** Scores each metric from 1 to 5 using fixed thresholds and combines the three into a single RFM score (e.g. `545`).
- **Segmentation:** Uses rules to sort customers into Champions, Loyal Customers, Potential Loyalist, At Risk, Lost, Big Spenders and Others.
- **Demographic insights:**
  - Age bracket mix within each segment (counts and % share)
  - Total, average and median spend by age bracket
  - Spending patterns by marital status
Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn

Dataset
Customer_Master_Data.csv: CustomerID, Gender, Age, MaritalStatus, JoinDate
Customer_Transactions.csv: CustomerID, TransactionDate, TransactionAmount
How to Run
Open RFM_Analysis.ipynb in Jupyter or Google Colab.
Upload both CSV files and update the file paths if needed (the notebook reads from /content/).
Run all cells.
Use Cases
Targeted marketing, retention campaigns, loyalty programs and win-back strategies for At Risk and Lost customers.
