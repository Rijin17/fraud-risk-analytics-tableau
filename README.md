# Fraud Risk Analytics – Tableau

Interactive Tableau dashboard that turns ML fraud scores into business insights.

**What’s inside**
- `fraud_risk_dashboard.twbx` – packaged Tableau workbook
- `scored_test.csv` – sample scoring dataset
- Screenshots: Fraud by Hour, Score Distribution, Fraud Rate by Score Band

## Live Dashboard
> (Add link after publishing to Tableau Public)
> Example: https://public.tableau.com/views/fraud_risk_dashboard/Dashboard1

## Highlights
- **Fraud by Hour** – monitors hourly spikes for ops staffing & rule tuning  
  ![Fraud by Hour](./Fraud%20by%20Hour.png)

- **Score Distribution** – sanity check for the ML model; watch for drift/holes  
  ![Score Distribution](./Score%20Distribution.png)

- **Fraud Rate by Score Band** – clear risk segmentation (Low/Med/High/Very High)  
  ![Fraud Rate by Score Band](./Fraud%20Rate%20by%20Score%20Band.png)

## How to open locally
1. Install **Tableau Public** (free).
2. Download this repo (`Code → Download ZIP`) or `git clone`.
3. Open `fraud_risk_dashboard.twbx` in Tableau. The packaged file includes data.
4. If you prefer, connect `scored_test.csv` and refresh the extracts.


- Built KPI views aligned to model monitoring: hourly anomalies, distribution drift, and calibrated risk bands.
- Designed for **explainability** (labels, tooltips, % scales) so non-technical stakeholders can act.
- Ready to extend with new model versions or live database connections.

## License
MIT
