# HealthConnect Clinic – Week 8
## Final Analytics and Decision Support

### Project Overview
Week 8 focused on finalising the HealthConnect Clinic Data Analytics project. The work brought together the appointment analysis, KPI evaluation, Power BI dashboard refinement, testing and validation, and cross-track collaboration. The main objective was to use the findings to support better understanding of missed appointments and provide practical recommendations for the clinic.

### Work Completed

**1. Appointment Data Analysis**

I analysed the synthetic HealthConnect appointment dataset to identify patterns associated with missed appointments. The analysis focused on booking lead time, previous no-show history, reminder channels, appointment types, and distance to the clinic. Particular attention was given to how booking lead time and previous no-show history relate to no-show behaviour.

**2. KPI Evaluation and Key Findings**

I reviewed the project's key performance indicators and used them to summarise appointment outcomes. The final dashboard included the following results:

- Overall No-Show Rate: 48.5%
- 30+ Day No-Show Rate: 60.5%
- Repeat No-Show Rate: 55.4%
- Lost Slot Rate: 53.7%

The analysis showed that no-show rates increased across the booking lead-time groups, from 24.8% for appointments booked 0–3 days in advance to 60.5% for appointments booked more than 30 days in advance.

I also examined the combined relationship between long booking lead time and previous no-show history. Within the 30+ day group, appointments with a previous no-show history had a 67.9% no-show rate, compared with 55.2% for appointments without a previous no-show history. This represented a difference of 12.7 percentage points.

**3. Power BI Dashboard Refinement**

I refined the Power BI dashboard to make it more interactive and useful for exploring appointment patterns. The final dashboard included slicers for booking lead time, previous no-show history, reminder channel, and appointment type.

I also rearranged the dashboard layout and removed the static Top 3 Insights section from the main page to create more space for interactive slicers. The key insights were retained in the project documentation rather than removed from the overall analysis.

**4. Testing and Validation**

I tested the dashboard to check that the KPIs responded correctly to the slicer selections. During testing, I identified an issue with the Repeat No-Show KPI when the "No prior no-show" option was selected. I refined the DAX measure and retested it. After the correction, the KPI displayed 0.0% for that selection.

I also corrected the distance category sorting by adding a custom sort column in Power Query. These refinements improved the dashboard's behaviour and presentation.

**5. Business Insights and Recommendations**

The analysis highlighted booking lead time and previous no-show history as important patterns for the clinic to monitor. I recommended paying particular attention to appointments booked more than 30 days in advance, especially when the patient has a previous no-show history.

Other recommendations included reviewing patient-support needs across appointment types, monitoring reminder-channel outcomes, and evaluating future interventions using subsequent appointment results.

**6. Cross-Track Collaboration**

I shared the combined finding on long booking lead time and previous no-show history with the Data Science track. This supported discussion of a possible interaction feature combining both factors for further testing.

The feature was proposed for investigation; no improvement in model performance was confirmed as part of the Week 8 work.

### Tools and Technologies
- Power BI – dashboard development and visualisation
- Power Query – data preparation and transformation
- DAX – KPI calculations and measure refinement
- GitHub – project documentation and version control

### Final Outcome
Week 8 brought the HealthConnect Clinic Data Analytics work together into a final analytics and decision-support deliverable. The work included the completed analysis, refined interactive dashboard, KPI validation, documented findings, practical recommendations, and cross-track integration.

The dataset used is synthetic, and the findings describe associations rather than proving that any factor causes missed appointments. Further validation would be required before applying the findings in a real clinic.
