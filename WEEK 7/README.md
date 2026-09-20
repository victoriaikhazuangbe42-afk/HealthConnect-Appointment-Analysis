# HealthConnect Clinic — Data Analytics Track

**AnalystLab Africa Experience Lab Internship Programme**
Project: *Improving Patient Appointment Attendance and Healthcare Support Using Data and AI*
Track: Data Analytics | Current Status: Week 7 — Testing, Refinement & Validation

---

## Project Overview

HealthConnect Clinic is a fictional healthcare provider seeking to reduce missed appointments, improve appointment attendance, make better use of appointment slots, and provide more effective administrative support to patients.

This repository holds the Data Analytics track contribution to the multi-track HealthConnect Experience Lab, built and refined across Weeks 4–7 of the programme using **Power Query** and **Power BI**.

The central question this track investigates:

> How does booking lead time relate to previous no-shows, reminder channel, appointment type, and distance to the clinic — and what does that mean for reducing missed appointments?

---

## Repository Structure

- data/
  - HealthConnect_Appointment_Data.csv — Approved project dataset (5,000 appointments)
- dashboard/
  - HealthConnect_No-Show_Dashboard.pbix — Power BI dashboard (Week 5–7)
- reports/
  - Week4_Initial_Analysis_Document.docx
  - Week4_Project_Summary.docx
  - Week5_Analytics_Report.docx
  - Week5_Project_Summary.docx
  - Week6_Advanced_Analytics_Report.docx
  - Week7_Analytics_Testing_Refinement_Report.docx
  - Week7_Testing_Evidence_Pack.docx
  - Week7_Cross_Track_Testing_Validation.docx
  - Week7_Project_Summary.docx
- README.md

*(Adjust the paths above to match your actual folder names/casing if they differ.)*

---

## Key KPIs (Current, Week 7)

| KPI | Value | Definition |
|---|---|---|
| Overall No-Show Rate | 48.5% | No-shows ÷ total appointments (5,000) |
| 30+ Day No-Show Rate | 60.5% | No-show rate among appointments booked 30+ days ahead |
| Repeat No-Show Rate | 55.4% | No-show rate among appointments with prior no-show history |
| Lost Slot Rate | 53.7% | (No-shows + Cancellations) ÷ total appointments |

## Headline Findings

- **Booking lead time is the strongest observed pattern**: no-show rate rises from 24.8% (0–3 days) to 60.5% (30+ days).
- **Previous no-show history compounds the effect**: within the 30+ day group, patients with prior no-shows reach 67.9%, vs. 55.2% for those without.
- These are **observed associations, not causal claims** — the dataset is fictional/synthetic and intended for learning purposes.

---

## Dashboard

Open `HealthConnect_No-Show_Dashboard.pbix` in Power BI Desktop. The dashboard includes:

- Four headline KPI cards
- Lead Time × Previous No-Show History breakdown (table + segment risk table)
- Lead Time × Reminder Channel, × Appointment Type, × Distance to Clinic (charts)
- Interactive slicers: Lead Time, Previous No-Show History, Reminder Channel, Appointment Type

---

## Week-by-Week Progress

| Week | Focus | Output |
|---|---|---|
| 4 | Problem understanding, resource review, planning | Initial Analysis Document, Project Summary |
| 5 | Initial EDA, KPI development, first dashboard | Analytics Report, Project Summary, interactive dashboard |
| 6 | Advanced segmentation, cross-track integration | Advanced Analytics Report |
| 7 | Systematic testing, refinement, validation | Testing & Refinement Report, Evidence Pack, Cross-Track Validation, Project Summary |

### Week 7 Testing Summary

Week 7 validated all core KPIs and segment breakdowns against the raw dataset, and identified and resolved two issues:

1. **Repeat No-Show KPI slicer-response bug** — the DAX measure ignored the "No prior no-show" slicer selection and always returned 55.4%. Refined and re-tested; now correctly returns 0.0% for that selection.
2. **Distance-to-clinic category sort order** — the chart legend displayed distance bands out of logical order. Corrected via a custom sort column in Power Query; re-tested with values unchanged.

Full test records, before/after evidence, and screenshots are in `Week7_Testing_Evidence_Pack.docx`.

---

## Cross-Track Collaboration

The Lead Time × Previous No-Show History finding (67.9% vs. 55.2% within the 30+ day segment) was shared with the **Data Science track** as a candidate interaction feature for predictive modelling. See `Week7_Cross_Track_Testing_Validation.docx` for the full handoff record.

---

## Limitations

- Dataset is fictional/synthetic — for learning and analytical practice only, not clinical decision-making.
- Findings describe observed associations, not causal relationships.
- Distance and waiting-time fields contain some missing values.
- Reminder-channel differences are descriptive and should not be read as proof of causal effect.

---

## Tools Used

- **Power Query** — data preparation, calculated columns, custom sort order
- **Power BI / DAX** — KPI calculations, interactive dashboard, slicers

---

*Project progress shared on LinkedIn/X with #AnalystLabAfrica.*
