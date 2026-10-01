# Preliminary dataset choice

- **Dataset name:** Plant Shift Log Data
- **Source:** Internal Plant Data Engineering Team
- **Licence or permitted use:** Internal company use only (Restricted)
- **Data status:** restricted
- **Unit of observation:** One machine shift event/record
- **Time span:** [Insert dates, e.g., Jan 2024 - Dec 2024]
- **Number of rows and columns:** [Insert shape once you run the script, e.g., 5000 rows, 12 columns]
- **Variables relevant to the decision:** Timestamps, Machine ID, Downtime Duration, Error Codes, Shift ID
- **Important missing variables:** Operator notes explaining *why* an error occurred (only codes are provided)
- **Known quality issues:** Manual data entry by operators may lead to typos or missed logs
- **Why the data may fit the question:** It provides historical evidence of when and where failures happen
- **Why the data may not fit the question:** It may lack root-cause details needed to actually prevent downtime
- **Additional data or stakeholder evidence needed:** Interviews with maintenance crew to interpret error codes


## Intended role

Choose one and explain: exploratory description / decision-support pilot /
model development / unsuitable for the proposed use.

Decision-support pilot — the data will be used to generate initial insights and test whether a full predictive model is worth building next quarter.