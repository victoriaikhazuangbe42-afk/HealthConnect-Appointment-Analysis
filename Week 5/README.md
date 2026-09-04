## Week 5 — HealthConnect Solution Development & Implementation (Data Analytics Track)

### Objective
Move from Week 4's planning stage into practical implementation: prepare the data, run exploratory analysis, calculate the five KPIs proposed in Week 4, build an interactive Power BI dashboard, and translate the findings into business recommendations.

### Business Questions Answered
| # | Question |
|---|---|
| Q1 | Which patient, booking and appointment characteristics are most strongly associated with no-shows? |
| Q2 | Does sending a reminder, and the channel used, measurably influence attendance? |
| Q3 | How much appointment capacity is lost to no-shows and cancellations, and where does it concentrate? |
| Q4 | Are patients with a prior history of missed appointments more likely to miss future ones? |
| Q5 | How do distance to the clinic and booking lead time relate to attendance behaviour? |

### KPIs Calculated
| KPI | Result | Business Question |
|---|---|---|
| No-Show Rate | 48.5% | Q1, Q3 |
| Reminder Effectiveness | SMS 45.75% → No Reminder 51.39% | Q2 |
| Lost Slot Rate | 53.7% | Q3 |
| Repeat No-Show Rate | 55.4% (prior no-show) vs. 43.5% (clean history) | Q4 |
| Distance / Lead-Time Attendance | Lead time 24.8%–60.5%; Distance 46.4%–54.1% | Q5 |

### Key Insights
1. **Booking lead time is the strongest observed driver** — no-show rate rises from 24.8% (0–3 days) to 60.5% (30+ days), a 35.7-point spread.
2. **Prior no-show history is a meaningful behavioural signal** — 55.4% vs. 43.5%, an 11.9-point gap.
3. **Reminder channel shows a modest, actionable association** — SMS (45.75%) outperforms Email, WhatsApp, and no reminder at all (51.39%).
4. **Distance is associated with attendance** — 46.4% (<5km) rising to 54.1% (15km+).
5. **Capacity loss is substantial** — 53.7% Lost Slot Rate.
6. **Appointment type shows smaller but consistent differences** — Follow-up highest at 51.23%, General Consultation lowest at 46.64%.
7. **Demographic differences (age, gender) are comparatively small** — tested directly on the dashboard, not just assumed; confirms these are not first-line targets.

### Business Recommendations
| Recommendation | Evidence | Priority |
|---|---|---|
| Strengthen confirmation for bookings made 15+ days ahead | 30+ day no-show rate = 60.5% | High |
| Flag patients with `previous_no_shows > 0` for outreach | 55.4% vs. 43.5% | High |
| Standardise SMS as the default reminder channel | SMS 45.75% vs. None 51.39% | High |
| Monitor Lost Slot Rate over time post-intervention | 53.7% baseline | High |
| Prioritise confirmation calls using lead time, history, distance, and type | Risk concentrated in identifiable segments | Medium |
| Explore telehealth/access alternatives for 15km+ patients | 15km+ rate = 54.11% | Medium |
| Review workflow for higher-risk appointment types | Follow-up = 51.23% | Medium |

### Data Preparation Summary
The dataset (5,000 records, 18 variables) was checked for completeness, uniqueness, and consistency — no duplicates or logical inconsistencies were found. `reminder_channel` nulls (27.3%) exactly match `reminder_sent = No` and were treated as a meaningful category rather than imputed. `distance_to_clinic_km` (1.8% missing) and `waiting_time_minutes` (1.2% missing) were excluded only from analyses using those specific fields. `waiting_time_minutes` was further flagged as unreliable — it is populated even for No-Show and Cancelled appointments with no meaningful relationship to outcome — and was excluded from driver analysis.

### Dashboard
An interactive Power BI dashboard (`HealthConnect_No-Show_Dashboard.pbix`) was built using Power Query for data preparation and DAX for all KPIs. It includes 8 KPI cards (including Total Patients and Total Appointments as context metrics), 8 charts across two rows — the four strongest drivers first, followed by supporting detail and demographic checks (age group, gender) — and 5 interactive slicers.

### Cross-Track Collaboration
Findings were shared with the Data Science track ahead of their Week 5 baseline modelling work: the five KPIs, the ranked list of attendance drivers, and a caution flagging `waiting_time_minutes` as unsuitable for use as a predictive feature. Full detail is documented in the Data Analytics → Data Science Collaboration Report.

### Tools Used
- **Power Query** — data import, validation, cleaning, derived fields (`distance_band`, `lead_band`, `prior_noshow_flag`)
- **Power BI** — data modelling, DAX measures, interactive dashboard

### Proposed Focus for Week 6
Compare descriptive findings against Data Science's baseline model performance and validated feature importance — where the two sources of evidence agree, confidence in prioritisation increases; where they differ, revisit segmentation or feature engineering rather than assuming either source is automatically correct.

---
Reminder Sent = No
