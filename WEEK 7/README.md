# HealthConnect Clinic – Week 7
## Data Analytics | Testing, Validation and Refinement

## Project Overview

HealthConnect Clinic is a synthetic healthcare analytics project focused on understanding missed patient appointments and identifying data-driven opportunities to improve appointment attendance and clinic capacity.

The Data Analytics work progressed through exploratory analysis in Week 5, advanced no-show analysis and integration in Week 6, and testing, validation and refinement in Week 7.

This repository documents the Week 7 analytical work, including KPI validation, dashboard testing, issue resolution, dashboard refinement, analytical validation and cross-track collaboration.

---

## Project Question

**How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?**

---

## Week 7 Objectives

The Week 7 work focused on:

- Validating KPI calculations against the underlying dataset.
- Testing dashboard filters, slicers and interactions.
- Identifying and resolving calculation issues.
- Re-testing dashboard outputs after refinement.
- Validating key analytical findings.
- Refining dashboard layout and usability.
- Documenting cross-track collaboration.
- Preparing validated outputs for further project integration.

---

## Dashboard Overview

The Week 7 dashboard was developed from the Week 6 **HealthConnect | Advanced No-Show Analysis** dashboard.

Interactive slicers included:

- Lead Time
- Previous No-Show History
- Reminder Channel
- Appointment Type

These slicers enabled the dashboard to support deeper exploration of patient and appointment segments.

### Core KPIs

| KPI | Validated Value |
|------|---------------:|
| Overall No-Show Rate | 48.5% |
| 30+ Day No-Show Rate | 60.5% |
| Repeat No-Show Rate | 55.4% |
| Lost Slot Rate | 53.7% |

---

## Testing and Validation

Week 7 focused on validating the dashboard rather than developing new analysis.

Testing included:

- KPI validation
- Dashboard functionality testing
- Lead-time segment testing
- Previous no-show testing
- Reminder channel testing
- Appointment-type testing
- Cross-filter testing
- Dashboard usability testing

During testing, an issue was identified in the **Repeat No-Show Rate** measure.

When **No Prior No-Show** was selected, the KPI incorrectly continued to display **55.4%**.

The DAX measure was refined to respond correctly to the selected filter context.

After refinement:

| Measure | Re-tested Value |
|----------|---------------:|
| No-Show Rate | 43.5% |
| 30+ Day No-Show Rate | 55.2% |
| Repeat No-Show Rate | 0.0% |
| Lost Slot Rate | 49.5% |

The refined measure passed re-testing.

---

## Key Findings

The validated analysis identified several important patterns:

| Segment | Result |
|----------|--------:|
| Overall No-Show Rate | 48.5% |
| 30+ Day No-Show Rate | 60.5% |
| Previous No-Show History | 55.4% |
| No Prior No-Show | 43.5% |
| 30+ Days + Previous No-Show | 67.9% |
| 30+ Days + No Previous No-Show | 55.2% |

The analysis showed that longer booking lead times and previous no-show history were associated with higher observed no-show rates.

The combination of these two factors formed the highest observed risk segment in the dataset.

---

## Dashboard Refinements

Several improvements were made during Week 7:

- Dashboard layout rearrangement.
- Addition of interactive slicers.
- Correction of Repeat No-Show DAX behaviour.
- Renaming of KPI labels for clarity.
- Removal of the static **Top 3 Insights** section.
- Creation of additional space for interactive analysis.

These refinements improved dashboard usability and analytical exploration.

---

## Cross-Track Contribution

The Week 7 work carried forward the Week 6 collaboration between the Data Analytics and Data Science tracks.

The observed interaction between:

- Long booking lead time
- Previous no-show history

was shared as a potential feature for predictive-model testing.

No claim is made that the feature improved model performance because additional Data Science validation was not available during Week 7.

---

## Evidence

Detailed testing evidence is maintained separately and includes:

- Final dashboard
- KPI validation
- Lead-time testing
- Repeat No-Show DAX refinement
- Re-testing evidence
- Cross-track collaboration evidence

---

## Tools Used

- Power BI
- Power Query
- DAX

---

## Limitations

- The dataset is synthetic.
- Findings represent observed patterns rather than causal relationships.
- Some distance and waiting-time values are missing.
- Reminder-channel results should not be interpreted as evidence of effectiveness.
- Further predictive-model testing remains dependent on the Data Science track.

---

## Week 7 Status

✅ KPI validation completed

✅ Dashboard testing completed

✅ DAX refinement completed

✅ Dashboard refinement completed

✅ Analytical findings validated

✅ Cross-track contribution documented

---

**HealthConnect Clinic | Data Analytics | Week 7**
