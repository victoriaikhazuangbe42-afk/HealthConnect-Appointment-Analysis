# HealthConnect-Appointment-Analysis
Analysis of HealthConnect appointment data to identify factors influencing patient attendance, no-shows, waiting times and reminder effectiveness.

### Project Overview
HealthConnect Clinic is a fictional healthcare provider facing high rates of missed appointments. This week marks the start of the **HealthConnect Experience Lab**, a multi-week project exploring how data and AI can reduce no-shows and improve the patient support experience. From Week 4 onward, all AnalystLab Africa tracks contribute to this shared project from their own professional lens.

**Central Project Question:** How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

**My Track:** Data Analytics — understanding the appointment data and identifying how it can be used to investigate appointment attendance and no-show patterns.

### Objective
Establish a clear understanding of the HealthConnect business problem, review the appointment dataset, and define an initial data analysis approach — without yet building the final KPIs, visuals, or dashboard (that begins Week 5).

### Data
| File | Description |
|---|---|
| `HealthConnect_Appointment_Data` | 5,000 fictional, anonymised appointment records across 1,696 patients |
| `HealthConnect_Data_Dictionary.xlsx` | Field definitions and expected value ranges for the appointment dataset |

### Key Findings
- **48.5%** of scheduled appointments end in a **No-Show**, 46.3% are Attended, 5.3% are Cancelled — confirming this is a substantial problem worth investigating.
- The dataset is clean and internally consistent: no duplicate records, no logical violations between historical fields, and minimal missing data (under 2% outside of one fully explained field).
- Identified a data quality anomaly: `waiting_time_minutes` is populated even for No-Show and Cancelled appointments with near-identical averages across outcomes — flagged as unlikely to be a genuine attendance-linked measurement.
- Early signal: patients with a prior no-show have a **55.4%** no-show rate on their next appointment, vs. **43.5%** for patients with a clean history — the strongest candidate driver found so far.

### 5 Potential KPIs Identified
1. No-Show Rate (overall & by segment)
2. Reminder Effectiveness (reminder sent vs. not, by channel)
3. Lost Slot Rate (% of slots lost to No-Show/Cancelled)
4. Repeat No-Show Rate (by prior no-show history)
5. Distance/Lead-Time Banded Attendance Rate

### Tools Used
- **Power Query** — data import, type validation, cleaning and shaping
- **Power BI** — data modelling, DAX measures, and dashboard build (Week 5 onward)

### Proposed Focus for Week 5
Clean and load the data via Power Query, build the Power BI data model, calculate the five candidate KPIs as DAX measures, and produce initial visuals to confirm which factors most strongly relate to no-shows ahead of full dashboard design.

---
*Part of the AnalystLab Africa Experience Lab Internship Programme — #AnalystLabAfrica*
