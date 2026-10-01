# Data suitability checklist

| Check | Rating | Evidence or unresolved question |
|---|---|---|
| Source is recorded | Yes | Sourced from internal Plant Data Engineering Team (see `data_choice.md`). |
| Licence or permitted use is recorded | Yes | Internal company use only (Restricted). |
| Data status is clear | Yes | Internal historical shift log data. |
| Personal or sensitive fields are identified | Yes | Operator IDs may be present; must be anonymized (see `ethical_risk_note.md`). |
| Unit of observation is understood | Yes | One row represents a single machine shift event/record. |
| Variables match the proposed decision | Yes | Contains timestamps, machine IDs, error codes, downtime duration. |
| Time span represents the intended use | Unknown | Need to verify the CSV covers the relevant quarterly production cycle. |
| Missing values and duplicates are assessed | Yes | Checked via `src/profile_data.py`. Found no missing values, but 1 duplicate row. |
| Impossible or implausible values are assessed | Yes | Found 1 row with negative energy and 1 row with temp > 100°C. Needs cleaning. | 
| Impossible or implausible values are assessed | No | To be checked during EDA in `week2_problem_framing.ipynb`. |
| Dataset size is manageable this semester | Yes | It is a standard CSV file. |
| Stakeholder or domain evidence is available | Partly | We have the data, but need maintenance crew input to interpret error codes. |
| Required permission or ethics review is known | Yes | Internal use only, requires HR approval for operator fields. |
| Client, cross-border, or confidentiality obligations are identified | Yes | Internal company confidentiality applies. |
| Human review and non-use conditions are defined | Yes | Documented in the Guardrails section of `problem_brief.md`. |

## Preliminary decision
Select one: Proceed / Pilot / Change question / Stop

Pilot

## Justification
We recommend a Pilot approach. The proposed user (Plant Operations Manager) and the operational decision (shift scheduling and maintenance) are clearly defined. The available data evidence (plant_shift_log.csv) contains the necessary variables, such as timestamps and downtime duration, which directly align with the decision to reduce unplanned downtime by 10%. The primary ethical risk—using the data to unfairly penalize operators—has a defined safeguard: anonymizing operator IDs. Additionally, human oversight is required before any scheduling changes are made. The most important unresolved question is whether the error codes are recorded consistently enough across all shifts to support accurate modeling; this must be validated before moving beyond the pilot phase.
