# Fraud Risk Analytics (Tableau)

Interactive Tableau dashboard by **Rijin** showing:
- **Fraud by Hour** – operational monitoring for spikes/outages
- **Score Distribution** – calibration & drift sanity check
- **Fraud Rate by Score Band** – business-friendly risk tiers

**Live dashboard:** *[<div class='tableauPlaceholder' id='viz1763256114750' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Fr&#47;FraudProbability&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='FraudProbability&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Fr&#47;FraudProbability&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1763256114750');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='420px';vizElement.style.maxWidth='650px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='420px';vizElement.style.maxWidth='650px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='927px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>](https://public.tableau.com/views/FraudProbability/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)*  
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
