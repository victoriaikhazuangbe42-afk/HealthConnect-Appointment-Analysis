# HealthConnect Clinic — Data Analytics Track (Week 7)

**AnalystLab Africa Experience Lab Internship Programme**
Project: *Improving Patient Appointment Attendance and Healthcare Support Using Data and AI*
Track: Data Analytics | Status: Week 7 — Testing, Refinement & Validation

---

## Project Overview

HealthConnect Clinic is a fictional healthcare provider seeking to reduce missed appointments, improve appointment attendance, make better use of appointment slots, and provide more effective administrative support to patients.

Week 7 moved the Data Analytics track from development and integration into systematic testing, refinement, re-testing and validation. The existing HealthConnect appointment dataset, Power BI model and prior findings were retained and tested rather than rebuilt.

---

## Repository Structure

- data/
  - HealthConnect_Appointment_Data.csv — Approved project dataset (5,000 appointments)
- dashboard/
  - HealthConnect_No-Show_Dashboard.pbix — Refined Power BI dashboard
- reports/
  - Week7_Analytics_Testing_Refinement_Report.docx
  - Week7_Testing_Evidence_Pack.docx
  - Week7_Cross_Track_Testing_Validation.docx
  - Week7_Project_Summary.docx
- README.md

---

## Testing Focus

Week 7 validated KPI calculations, checked dashboard values against the underlying data, tested slicers and filter behaviour, investigated inconsistent results, refined identified weaknesses, re-tested the refined outputs, and reassessed key findings across relevant segments.

| Area | Work Completed | Outcome |
|---|---|---|
| Core KPIs | Overall No-Show Rate; 30+ Day No-Show Rate; Repeat No-Show Rate; Lost Slot Rate | Validated |
| Lead time | 0–3, 4–14, 15–30 and 30+ day segments | Validated |
| Previous no-show history | Has prior no-show / No prior no-show filters | Validated after refinement |
| Reminder channel | Email, None, SMS and WhatsApp | Validated |
| Appointment type | Four appointment-type segments | Validated |
| Dashboard functionality | Slicers, KPI labels, layout and filter behaviour | Refined and re-tested |
| Distance to clinic | Category sort order in the Lead Time × Distance chart | Refined and re-tested |

---

## Validated Key KPIs

| KPI | Value | Definition |
|---|---|---|
| Overall No-Show Rate | 48.5% | No-shows ÷ total appointments (5,000) |
| 30+ Day No-Show Rate | 60.5% | No-show rate among appointments booked 30+ days ahead |
| Repeat No-Show Rate | 55.4% | No-show rate among appointments with prior no-show history |
| Lost Slot Rate | 53.7% | (No-shows + Cancellations) ÷ total appointments |

## Validated Key Findings

- **Booking lead time** is the clearest observed segmentation pattern, rising from 24.8% (0–3 days) to 60.5% (30+ days).
- **30+ days + prior no-show**: 67.9% — the highest observed combined segment; association, not causation.
- **30+ days + no prior no-show**: 55.2% — long lead time remains elevated even without prior no-show history.
- **Lost Slot Rate** (53.7%) shows no-shows and cancellations together represent substantial scheduled-capacity loss.
- These are observed associations, not causal claims — the dataset is fictional/synthetic and intended for learning purposes.

---

## Issues Identified and Resolved

1. **Repeat No-Show KPI slicer-response issue** — the DAX measure explicitly filtered on the "Has prior no-show" category and did not respond to the "No prior no-show" slicer selection, remaining fixed at 55.4%. The measure was refined to respect the selected history context. Re-tested: now correctly returns 0.0% for "No prior no-show."
2. **Distance-to-clinic category sort order** — the chart legend displayed distance bands out of logical order (`<5km, 15km+, 5-15km, Unknown`). A custom sort column was applied in Power Query so the order now reads `<5km, 5-15km, 15km+, Unknown`. Re-tested: underlying values unchanged, order corrected.
3. **0–3 days Lost Slot Rate** — re-checked against the raw dataset (31.45%, rounds to 31.4%); confirmed to match the dashboard exactly, no discrepancy found.

Full before/after evidence and screenshots are documented in `Week7_Testing_Evidence_Pack.docx`.

---

## Dashboard Refinements

- Rearranged the dashboard to improve analytical flow and make space for interactive analysis.
- Removed the static Top 3 Insights panel to create space for slicers; underlying findings retained in documentation.
- Added slicers for Lead Time, Previous No-Show History, Reminder Channel and Appointment Type.
- Renamed the second KPI to "30+ Day No-Show Rate" to clarify its segment-specific meaning.
- Standardised user-facing labels and lead-time categories.
- Corrected the distance-to-clinic category sort order.

---

## Cross-Track Collaboration

The Lead Time × Previous No-Show History finding (67.9% vs. 55.2% within the 30+ day segment) was shared with the **Data Science track** as a candidate interaction feature for predictive modelling. Analytics-side validation is complete; Data Science's model-performance evaluation remains an open dependency. Full handoff record in `Week7_Cross_Track_Testing_Validation.docx`.

---

## Limitations

- Dataset is fictional/synthetic — for learning and analytical practice only, not clinical decision-making.
- Findings describe observed associations, not causal relationships.
- Distance and waiting-time fields contain some missing values.
- Reminder-channel differences are descriptive and should not be read as proof of causal effect.
- The Data Science interaction feature remains a candidate for predictive testing.

---

## Week 8 Readiness

- Refined Power BI dashboard and validated KPI logic, including the corrected distance sort order, are the current Analytics version.
- Validated findings and documented limitations carry forward into final integration.
- Status of the Data Science interaction-feature test to be completed/documented before final presentation.

---

## Tools Used

- **Power Query** — data preparation, calculated columns, custom sort order
- **Power BI / DAX** — KPI calculations, interactive dashboard, slicers

---

*Project progress shared on LinkedIn/X with #AnalystLabAfrica.*
