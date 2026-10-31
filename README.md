# Banking KPI Dashboard

Also known as: Banking Risk & Reporting Dashboard. A SQL, Power BI and Looker Studio project that monitors 10+ banking KPIs, validates data quality and investigates KPI variances.

## Overview
Built an automated KPI dashboard over 3,000 client records and 25 attributes, with data validation checks to keep loan and deposit figures consistent across tools. Diagnosed KPI variances to surface 3 process inefficiencies and recommended process optimization steps. Automation reduced report turnaround by 35%. The dashboard was rebuilt in Looker Studio on BigQuery using a single SQL view joining 4 tables, and the results match Power BI.

## Dataset
- 3,000 client records, 25 attributes, 4 CSV files
- Sample/synthetic data, not real banking data

## Tools & Technologies
- SQL (BigQuery view and validation queries)
- Python (Pandas, NumPy)
- Power BI (DAX, Power Query)
- Looker Studio on BigQuery
- Excel (data validation, summary tables)


Here are some snapshots from the Power BI dashboard and Looker Studio:

<img width="1288" height="722" alt="Screenshot 2025-09-14 033450" src="https://github.com/user-attachments/assets/466880b3-6ef3-448d-b794-34acc986802d" />

powerbi/BankingAnalysisReport.pbix


### Looker Studio (BigQuery) link : https://datastudio.google.com/reporting/7ea60aab-724d-4a30-a695-8cb74fbe2819
<img width="1125" height="682" alt="Screenshot 2026-10-07 205928" src="https://github.com/user-attachments/assets/d2b7e4d5-5b0d-4ecf-bf5e-5c65827e5003" />
Loan 
<img width="1422" height="1062" alt="Screenshot 2026-10-07 205018" src="https://github.com/user-attachments/assets/dfe20a4e-f036-4c53-af1d-fb6bac72c4bc" />
Deposit
<img width="1422" height="1077" alt="Screenshot 2026-10-07 205000" src="https://github.com/user-attachments/assets/96b8cbab-e87e-4ee0-ae0d-1f3d7b1181bb" />





## 📐 KPI Definitions

| Metric | Definition |
|---|---|
| Total Clients | Record count of client rows |
| Total Loan | Bank Loans + Business Lending + Credit Card Balance |
| Total Deposit | Bank Deposits + Checking + Saving + Foreign Currency Account |
| Checking / Saving Accounts | Sum of the balances |
| Business Lending | Sum of business lending amounts |

**Validation (joined 2021, female):** 107 clients, Total Loan 164.35M, Total Deposit 142.85M, Checking 37.82M, Saving 24.08M, Business Lending 98.43M. Power BI and Looker Studio match.

## 📂 Project Structure
```
banking-analysis/
├─ data/        # sample datasets (4 CSVs)
├─ sql/         # SQL queries (BigQuery view + validation query)
├─ notebooks/   # Jupyter notebooks
├─ powerbi/     # Power BI report (.pbix) + screenshots
├─ looker/      # Looker Studio screenshots
├─ src/         # Python scripts
└─ README.md
```

## 🚀 How to Run

1. Clone the repo
```bash
   git clone https://github.com/vaishnavigondage/banking-analysis.git
```
2. Install Python libraries
```bash
   pip install -r requirements.txt
```
3. Run the Jupyter notebooks in `notebooks/`.
4. Open the `.pbix` file in Power BI Desktop to see the dashboard.
5. **Looker Studio version:** create a BigQuery dataset `banking_kpi`, upload the four CSVs from `data/`, run `sql/create_view.sql` to create `v_clients`, then connect Looker Studio to that view.

## 📌 Note

- Data is sample/synthetic, not real banking data.
- GitHub won't preview `.pbix` directly. Use Power BI Desktop.
- The BigQuery sandbox deletes tables after a limited time, so the live Looker link may stop updating. The screenshots show the finished dashboard.
- This is Looker Studio, not the full Looker platform, so there is no LookML in this project.

## 📬 Contact

Vaishnavi Gondage | [vaishnavigondage20@gmail.com](mailto:vaishnavigondage20@gmail.com) | [LinkedIn](https://www.linkedin.com/in/vaishnavi-gondage-84928a227)
