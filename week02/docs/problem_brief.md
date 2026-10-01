# Week 2 industrial problem brief

Keep this brief to approximately one page. Use short, concrete statements.

## Decision statement
For "Plant Operations Managers", use "historical shift log data (downtime, errors, output)" to support "decisions on shift scheduling and maintenance prioritization" before "the next quarterly production cycle".


## Problem frame
**User:** Plant Operations Manager
- **Decision owner:** Plant Supervisor
- **Affected people:** Machine operators, maintenance crew
- **Data owner:** Plant Data Engineering Team
- **Decision to support:** Whether to adjust shift handover procedures or schedule preventative maintenance.
- **Action that may follow:** Implementing new pre-shift checklist protocols based on common failure points.
- **Available evidence:** `plant_shift_log.csv` (Historical logs of shifts, machine status, and errors).
- **Desired value:** Reduce unplanned machine downtime by 10%.
- **Technical success measure:** A model or report that correctly identifies the top 3 causes of shift failures with 85% accuracy.
- **Operational success measure:** A 10% reduction in downtime within 3 months of implementing recommendations.
## Guardrail
- **Baseline comparison:** Compare against the current average downtime rate from existing shift logs.
- **Main constraint:** Only use data available in `plant_shift_log.csv` — no new sensors or extra budget.
- **Condition for non-use:** If the log data is incomplete, biased, or unreliable, do not use it for decisions.
## Assumptions and open questions
1. **Assumption:** The `plant_shift_log.csv` file contains all downtime events for the quarter (no missing shifts).
2. **Open question:** Are the machine error codes in the log standardized, or do they vary by operator?
3. **Open question:** Does the log include timestamps precise enough to calculate exact downtime duration?

