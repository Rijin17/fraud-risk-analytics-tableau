# Fraud Risk Analytics (Tableau)

Interactive Tableau dashboard by **Rijin** showing:
- **Fraud by Hour** – operational monitoring for spikes/outages
- **Score Distribution** – calibration & drift sanity check
- **Fraud Rate by Score Band** – business-friendly risk tiers

**Live dashboard:** *(add your Tableau Public link once published)*  
**Download workbook:** [`fraud_risk_dashboard.twbx`](./fraud_risk_dashboard.twbx)  
**Sample data:** [`scored_test.csv`](./scored_test.csv)

## Problem
Teams need a simple way to monitor fraud model behavior and communicate risk without ML jargon.

## What’s inside
- **Fraud by Hour:** average fraud rate by hour.
- **Score Distribution:** histogram of predicted probabilities.
- **Fraud Rate by Score Band:** Low / Medium / High / Very High bands.

## How to open
1. Download `fraud_risk_dashboard.twbx`.
2. Open in **Tableau Public (Desktop)** — data is packaged, no setup needed.

## Data dictionary
- `Fraud Probability` — model score (0–1)  
- `Is Fraud` — 0/1 label  
- `Hour` — transaction hour (0–23) 
- `Score Band` — calculated field:

IF [proba_fraud] >= 0.8 THEN "Very High"
ELSEIF [proba_fraud] >= 0.6 THEN "High"
ELSEIF [proba_fraud] >= 0.4 THEN "Medium"
ELSE "Low" END


## Talking points (for recruiters/interviews)
- Designed for **model monitoring**: catches operational spikes (by hour), checks **calibration/drift** (distribution), and presents **actionable risk tiers** for business.
- Emphasis on **explainability & adoption**: clear % labels, readable bins, and bands that map to policy (review/hold/decline).

## Screenshots
![Fraud by Hour](./Fraud%20by%20Hour.png)
![Score Distribution](./Score%20Distribution.png)
![Fraud Rate by Score Band](./Fraud%20Rate%20by%20Score%20Band.png)
![Dashboard](./Fraud%20Risk%20Dashboard.png)

## License
MIT — see [LICENSE](./LICENSE).

---

**Author:** **Rijin Stalin** • LinkedIn: *www.linkedin.com/in/rijin-s-83455326b*
