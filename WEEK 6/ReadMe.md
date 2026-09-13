# HealthConnect Clinic – Week 6
## Advanced Analytics & Decision Support

### Project Overview

HealthConnect Clinic is a healthcare analytics project focused on understanding appointment attendance and no-show behaviour.

Week 6 builds directly on the Week 5 Power BI dashboard by moving from descriptive analysis into deeper investigation of the factors associated with appointment no-shows.

The main focus of Week 6 is **booking lead time** and how it relates to previous no-show history, reminder channels, appointment type, and distance to the clinic.

The goal is to turn the findings into practical decision-support recommendations for improving appointment attendance and reducing lost appointment slots.

---

## Week 6 Objective

The objective of Week 6 was to improve the existing Week 5 dashboard by investigating relationships between booking lead time and other factors associated with higher observed no-show rates.

### Main Analytical Question

> **How does booking lead time relate to other factors associated with higher no-show rates?**

The analysis investigated:

- Booking lead time
- Previous no-show history
- Reminder channel
- Appointment type
- Distance to the clinic

---

## Week 5 → Week 6 Progression

Week 5 established the main descriptive patterns in appointment attendance.

The Week 5 dashboard showed:

- Overall no-show rate: **48.5%**
- Lost slot rate: **53.7%**
- Higher no-show rates among appointments booked further in advance
- Higher no-show rates among patients with previous no-show history
- Differences across reminder channels, appointment types, and distance groups

Week 6 builds on these findings rather than starting a new analysis.

The main improvement was to investigate whether the factors identified in Week 5 become more important when considered together.

---

## Dataset

The analysis uses the HealthConnect appointment dataset containing:

- **5,000 appointments**
- **1,696 unique patients**

Key variables used in the Week 6 analysis include:

- `booking_lead_days`
- `appointment_outcome`
- `previous_no_shows`
- `reminder_channel`
- `appointment_type`
- `distance_to_clinic_km`

---

## Tools Used

- **Power BI** – dashboard development and visual analysis
- **DAX** – calculated measures and KPI analysis
- **CSV Dataset** – source appointment data
- **GitHub** – project documentation and version control

---

# Key Findings

## 1. Booking Lead Time and No-Show Rate

Booking lead time showed a clear increase in observed no-show rates.

| Booking Lead Time | No-Show Rate |
|---|---:|
| 0–3 days | 24.8% |
| 4–14 days | 32.6% |
| 15–30 days | 43.2% |
| 30+ days | 60.5% |

Appointments booked more than 30 days in advance had the highest observed no-show rate at **60.5%**.

This makes extended booking lead time an important segment for further investigation.

---

## 2. Lead Time × Previous No-Show History

The strongest Week 6 finding was the combined effect of long booking lead time and previous no-show history.

Among appointments booked 30+ days in advance:

| Previous No-Show History | No-Show Rate |
|---|---:|
| Previous no-show | 67.9% |
| No previous no-show | 55.2% |

The difference between the two groups is approximately **12.7 percentage points**.

The combined segment of:

> **30+ day booking lead time + previous no-show history**

had the highest observed no-show rate in the analysis.

This finding was shared with the Data Science track as a potential interaction feature for future predictive modelling.

---

## 3. Lead Time × Appointment Type

Within appointments booked 30+ days in advance, observed no-show rates varied by appointment type.

| Appointment Type | No-Show Rate |
|---|---:|
| Follow-up | 65.1% |
| Diagnostic Test | 59.6% |
| Specialist Consultation | 59.2% |
| General Consultation | 58.1% |

Follow-up appointments showed the highest observed no-show rate within this long-lead segment.

---

## 4. Lead Time × Distance

Distance also provided an additional segmentation signal among appointments booked 30+ days in advance.

| Distance Group | No-Show Rate |
|---|---:|
| 15km+ | 66.4% |
| Unknown | 64.3% |
| <5km | 61.4% |
| 5–15km | 58.2% |

The 15km+ group had the highest observed no-show rate at **66.4%**.

However, distance should be treated as an additional signal rather than evidence of a simple causal relationship.

---

## 5. Lead Time × Reminder Channel

Reminder channels also showed variation within the 30+ day booking group.

| Reminder Channel | No-Show Rate |
|---|---:|
| Email | 61.9% |
| WhatsApp | 60.2% |
| SMS | 58.0% |

These differences are descriptive.

The analysis does **not** establish that one reminder channel causes better attendance because reminder assignment may not have been random.

Further testing would be required before recommending one channel as more effective.

---

# Week 6 Dashboard

The Week 6 Power BI dashboard was enhanced from the Week 5 dashboard.

### Dashboard Title

**HealthConnect – Advanced No-Show Analysis**

### Main Dashboard Components

The dashboard includes:

- Overall No-Show Rate
- 30+ Day No-Show Rate
- Repeat No-Show Rate
- Lost Slot Rate
- Lead Time × Previous No-Show History
- Lead Time × Reminder Channel
- Lead Time × Appointment Type
- Lead Time × Distance
- Segment-level comparison table

The dashboard is designed to move beyond individual KPIs and show how different factors relate to booking lead time.

---

# Decision-Support Recommendations

Based on the Week 6 findings, the following actions are recommended.

### 1. Target appointments booked 30+ days in advance

Appointments with extended booking lead times should receive additional confirmation attention because this group had a **60.5% observed no-show rate**.

### 2. Prioritise patients with previous no-shows

Patients with previous no-show history and appointments booked 30+ days in advance should receive additional attention because this segment had a **67.9% observed no-show rate**.

### 3. Give additional attention to long-lead follow-up appointments

Follow-up appointments booked 30+ days ahead had a **65.1% observed no-show rate**, making this a useful segment for targeted intervention.

### 4. Investigate travel-related barriers

The 15km+ group within the 30+ day segment had a **66.4% observed no-show rate**.

HealthConnect could investigate whether travel time, transport availability, or clinic accessibility contributes to missed appointments.

### 5. Test reminder strategies

Reminder channels showed different observed no-show rates, but the analysis does not prove that one channel is more effective.

Controlled testing should therefore be used before changing reminder policy.

### 6. Test the Lead Time × Previous No-Show interaction

The Data Science track identified the combination of long booking lead time and previous no-show history as a potential interaction feature for predictive modelling.

This should be tested during Week 7 using appropriate model performance metrics.

---

# Cross-Track Integration

The Week 6 analysis produced a direct contribution to the Data Science track.

The key finding shared was:

> **67.9% observed no-show rate for appointments booked 30+ days in advance among patients with previous no-show history, compared with 55.2% among patients without previous no-show history.**

The Data Science team confirmed that the current model treats booking lead time and historical no-show behaviour as independent signals.

Based on the Week 6 analysis, the team identified a potential interaction feature that combines:

- Extended booking lead time
- Previous no-show history

The interaction will be considered for testing in Week 7.

### Integration Flow

**Data Analytics**

→ Identified combined high no-show segment

**Data Science**

→ Identified potential interaction feature

**Week 7**

→ Test whether the interaction improves predictive performance

The Week 6 analysis does not claim that the interaction will improve the model. Its effectiveness must be validated during model testing.

---

# Limitations

The Week 6 analysis is primarily descriptive.

Therefore:

- Observed relationships should not be interpreted as causal relationships.
- Reminder channel differences do not prove channel effectiveness.
- Some segments have smaller appointment volumes and should be interpreted carefully.
- The analysis does not yet provide a validated predictive model.
- The proposed interaction feature has not yet been tested for model performance.

These limitations will be addressed through further validation and testing in Week 7.

---

# Week 7 Next Steps

The Week 6 findings provide a clear direction for the next stage of the project.

Planned areas for Week 7 include:

1. Test the **Lead Time × Previous No-Show** interaction feature.
2. Evaluate whether the interaction improves predictive model performance.
3. Compare model performance with and without the interaction.
4. Continue validating the strongest Week 6 segments.
5. Refine dashboard insights based on testing results.
6. Continue cross-track collaboration between Data Analytics and Data Science.
7. Prepare the final decision-support recommendations based on validated evidence.

---

# Week 6 Outcome

Week 6 successfully builds on the Week 5 dashboard by moving from individual descriptive patterns toward deeper relationship analysis.

The strongest finding was that **booking lead time becomes particularly important when combined with previous no-show history**.

The analysis also identified additional segmentation signals across appointment type, distance, and reminder channel.

These findings have been translated into practical decision-support recommendations and shared with the Data Science track to support predictive modelling work for Week 7.

---

## Project Status

**Week 6 Status: Completed**

### Progression

**Week 5**
→ Descriptive dashboard and baseline KPIs

**Week 6**
→ Advanced relationship analysis and decision support

**Week 7**
→ Predictive feature testing, validation and refinement

---

