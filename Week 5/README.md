# 🏥 HealthConnect Appointment Analytics

**Appointment Attendance & No-Show Analysis**

---

## 📌 Project Overview

HealthConnect Appointment Analytics examines **5,000 clinic appointments** to understand patterns behind missed appointments and identify opportunities to improve attendance.

The analysis moves beyond simply measuring the no-show rate by examining factors such as **booking lead time, previous attendance behaviour, reminder activity, distance to the clinic, and appointment type**.

The findings are presented through an interactive Power BI dashboard designed to support faster identification of higher-risk appointment segments.

---

## 🚀 Project Status

**Week 5 — Completed: Initial Analytics & Dashboard Development**

This stage of the project covers:

- Data preparation and quality validation
- Exploratory analysis of appointment attendance
- KPI development
- No-show pattern analysis
- Business insight generation
- Power BI dashboard development
- Initial business recommendations

The next stage will focus on further refinement, deeper segmentation, and potential predictive analysis.

---

## 🎯 Business Focus

The analysis addresses four key questions:

- How significant is the clinic's no-show problem?
- Which appointment characteristics are most associated with missed appointments?
- Do reminders appear to improve attendance?
- Which patient or appointment groups may require additional intervention?

---

## 📊 Dataset

| Metric | Value |
|---|---:|
| Appointments | **5,000** |
| Unique Patients | **1,696** |
| Variables | **18** |
| Overall No-Show Rate | **48.5%** |
| Lost Slot Rate | **53.7%** |

---

## 🔎 Key Findings

### 1. Booking Lead Time is the Strongest Signal

No-show rates increased significantly as the time between booking and appointment increased.

| Booking Lead Time | No-Show Rate |
|---|---:|
| 0–3 days | 24.8% |
| 4–14 days | 32.6% |
| 15–30 days | 43.2% |
| 30+ days | **60.5%** |

There is a **35.7 percentage-point difference** between the shortest and longest lead-time groups.

### 2. Previous No-Shows Matter

Patients with a previous no-show had a **55.4%** no-show rate compared with **43.5%** among patients without a previous no-show.

This suggests that previous attendance behaviour can be useful when identifying appointments that may require additional follow-up.

### 3. Reminders Show a Moderate Effect

| Reminder Status | No-Show Rate |
|---|---:|
| Reminder sent | 47.4% |
| No reminder | 51.4% |

Among reminder channels, SMS recorded the lowest no-show rate at **45.8%**.

### 4. Distance Has a Secondary Effect

Patients living **15 km+** from the clinic had a **54.1%** no-show rate compared with **46.4%** among those living less than 5 km away.

---

## 📈 Power BI Dashboard

The dashboard provides an interactive view of appointment attendance and highlights the strongest no-show patterns.

### Dashboard Includes

- No-Show Rate
- Lost Slot Rate
- Repeat No-Show Rate
- Reminder Effectiveness
- No-Show Rate by Lead Time
- No-Show Rate by Distance
- Previous No-Show Analysis
- Appointment Type Analysis
- Age & Gender Breakdown
- Interactive filters and slicers

---

## 🛠️ Tools & Technologies

### Data Preparation

- Microsoft Excel
- Power Query

### Analytics & Visualisation

- Power BI
- DAX

### Documentation & Version Control

- GitHub

---

## 💡 Business Recommendations

The findings suggest that HealthConnect could improve attendance by:

1. **Strengthening confirmation for long-lead appointments**, particularly those booked 15+ days in advance.

2. **Flagging patients with previous no-shows** for additional confirmation.

3. **Prioritising effective reminder channels**, with SMS showing the lowest no-show rate in this dataset.

4. **Paying closer attention to Follow-up appointments**, which recorded the highest no-show rate among appointment types.

5. **Exploring access solutions** for patients living farther from the clinic, including telehealth where appropriate.

---

## ⚠️ Limitations

- The dataset is synthetic and is intended for analytics practice.
- `waiting_time_minutes` was excluded from the main driver analysis because of data-quality concerns.
- The analysis focuses primarily on relationships between individual variables.
- No predictive modelling or statistical significance testing was performed at this stage.

---

## 📁 Repository Structure

**HealthConnect/**
- 📁 **Data/**
  - HealthConnect_Appointment_Data
- 📁 **Power BI/**
  - HealthConnect_No-Show_Dashboard.pbix
- 📁 **Reports/**
  - HealthConnect_Week5_Analytics_Report.docx
- 📁 **Documentation/**
- 📄 **README.md**

---



