<img width="1080" height="1080" alt="Modern Creative Logo Instagram Post" src="https://github.com/user-attachments/assets/d0ab2702-989d-4874-9bd6-81ee07f4d395" />

# Project Background
Founded in 2023, Hive Tech is a global IT company dedicated to managing and resolving client support tickets through a structured, multi-stage support workflow. As the company operates in a high-volume, service-oriented environment, recurring technical issues, uneven support queue workloads, and extended resolution times can place pressure on support teams and affect client productivity. 
This project analyzes Hive Tech’s support ticket data to answer key business questions around ticket volume, recurring issues, queue workload, resolution patterns, and workflow performance, uncovering actionable insights that identify opportunities & improve overall support processes through data-driven decisions.

Insights and recommendations are provided across the following key areas:

**Ticket Volume & Seasonality:** Analysis of monthly ticket activity to identify recurring patterns and periods of higher or lower support workload.

**Support Queue Performance:** Evaluation of ticket distribution across support queues to understand workload concentration and identify areas requiring improvement.

**Recurring Issues & Categories:** Analysis of ticket categories and tags to identify frequently occurring issues and potential opportunities for proactive & preventive support.

A view of the dashboard used to report and explore the dataset is shown below.

<img width="801" height="482" alt="IT_dashboard" src="https://github.com/user-attachments/assets/f0cec22c-a67f-41fc-8972-98f60125260a" />


# Data Structure & Initial Checks

The dataset contains **11,923 records and 14 fields** with the grain representing an individual support ticket, including information about when the ticket was created and resolved, the support queue responsible for handling it, its priority, ticket type, and associated categories or tags.


<img width="1306" height="498" alt="Dataset_IT" src="https://github.com/user-attachments/assets/d6d894b8-67fa-4bd5-8f4d-9e892ffec165" />

The data dictionary gives a clear description of the data and can be downloaded [here](https://github.com/jirenonso/IT-Performance-Analysis/blob/main/Data_Dictionary.md)
# Executive Summary

### Overview of Findings
Ticket volume **declined by 12.6% in February 2024 & increased by 13.8% in March**, and has since been relatively steady before dropping in Q4. While **January recorded the highest ticket volume at 735 tickets**, a similar February–March pattern appeared again in 2025, suggesting a recurring seasonal pattern in support activity.

Support workload was concentrated across a small number of queues, with **Technical Support accounting for 28.62% of all tickets**, followed by Product Support at 18.72% and Customer Service at 15.59%.

Recurring issue analysis also showed that a relatively small number of categories represented a significant share of support activity. The top three categories accounted for approximately **39%** of categorized tickets, while the top five represented approximately **48%**.

The following sections explore these patterns in greater detail and identify opportunities for improved support planning, workload management, issue prevention, and future data collection.

# Insights Deep Dive

### Ticket Volume & Seasonality
 **February 2024 experienced a 12.6% decline in ticket volume**, followed by a **13.8% increase in March**. January recorded the highest ticket volume overall, with **735 tickets**.

Interestingly, the February–March pattern appeared again in 2025, with ticket volume declining in February and increasing in the following month by 16.6% respectively. This recurring pattern was associated with high influx of incidents and requests, suggesting that the fluctuations were not isolated to only a single year and may reflect a recurring seasonal pattern in support activity.
Ticket activity also declined toward November and December, indicating relatively lower support activity in Q4.


<img width="646" height="291" alt="Tickets_volume   Seasonality" src="https://github.com/user-attachments/assets/b1d88199-99ad-4c91-aec4-d69d8e8bb882" />


These patterns provide a useful basis for support capacity planning. Periods with historically higher ticket volumes, particularly around June, may require greater staffing capacity and resource availability, while lower-volume periods could provide opportunities for backlog reduction, documentation, process improvement, and other operational activities.

---

### Support Queue Distribution
The data showed that some queues handled substantially more tickets than others, with **Technical Support accounting for approximately 28.62% of all tickets**.

The leading support queues were:

| Support Queue      | Ticket Share |
| ------------------ | -----------: |
| Technical Support  |       28.62% |
| Product Support    |       18.72% |
| Customer Service   |       15.59% |
| IT Support         |       11.67% |
| Billing & Payments |       10.92% |


<img width="607" height="284" alt="Support queue distribution" src="https://github.com/user-attachments/assets/3a8ce640-c3af-4d2f-972e-bf69617dae97" />


Technical Support, Product Support, and Customer Service therefore represented a significant proportion of the overall workload.

However, high ticket volume does not automatically indicate poor performance. A queue may handle more tickets simply because it is responsible for a larger or more complex category of requests.

### Recurring Issues & Categories
Category and tag analysis was performed to identify the issues appearing most frequently across the support environment.

The most frequently occurring categories included:

* IT
* Performance
* Bug
* Technical Support
* Outage

The top three categories accounted for approximately **39% of categorized tickets**, while the top five represented approximately **48%**.

<img width="440" height="363" alt="Recurring tickets" src="https://github.com/user-attachments/assets/5800c74a-5c6d-4c9b-bcb5-e03e86a89a8d" />


This concentration is important because recurring support issues may represent opportunities to reduce future ticket volume rather than repeatedly resolving the same problems.

Potential preventive interventions include:

* Knowledge-base articles
* Self-service documentation
* User training
* System improvements
* Product fixes
* Preventive monitoring
* Automated troubleshooting

This goes beyond measuring workload toward identifying opportunities for **proactive issue prevention**.

# Recommendations

Based on the findings above, the following recommendations were developed for IT support management:

| **Priority** | **Action**                                                                                                                  | **Owner**                    | **Impact**                                                                                   | **Metric to Track**                                                      |
| ------------ | --------------------------------------------------------------------------------------------------------------------------- | ---------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **High**     | Utilize ticket patterns to plan staffing and resources ahead of high-volume periods, particularly around January, being the month with the highest tickets recorded.       | IT Support Management        | Improve capacity planning and reduce potential workload bottlenecks during peak periods.     | Monthly Ticket Volume; Queue Workload; Backlog Volume; Staffing Capacity |
| **High**     |Stabilize eligible ticket routing across support queues as Technical Support and Product Support handle a disproportionately large share of incoming tickets, while General Inquiry and HR account for less than 5% combined.                               | IT Support / Service Desk Management        | Reduce workload concentration in high-volume queues, improve workload balance across support teams, and support more efficient ticket handling.     |queue share (%), Avg resolution time by queue|
| **High**     |IT accounted for 1999 tickets followed by Performance (985) and Tech support (773). Investigate recurring IT, Performance, Bug, Technical Support, Outage issues and automate where necessary.                                          | IT Support & Technical Teams | Reduce repetitive tickets through preventive action, documentation, and system improvements. | Recurring Issue Volume; Ticket Reduction; Knowledge-Base Usage           |
| **Medium**   | Add customer segment, affected product/system, escalation history, SLA status, and resolution category to future datasets.  | IT Operations / Data Team    | Improve root-cause analysis and identify the operational drivers of support workload.        | Root Cause; Resolution Category; Escalation Rate; SLA Breaches           |

# Assumptions and Caveats

Throughout the analysis, several assumptions and data limitations were identified:

* The dataset spans approximately **17 months**, rather than two complete calendar years, limiting full year-over-year seasonal comparisons.
* Some records contained null values and required appropriate handling during the data preparation process.
* Inconsistencies were identified across category, tag, and text fields and were standardized during cleaning.
* Some fields contained multiple values within a single cell and required transformation into structured categories before analysis.
* The **Days to Resolve** metric showed a strong relationship with priority, limiting its usefulness as an independent measure of operational efficiency.
* Ticket volume was treated as a measure of **support activity/workload**, rather than being interpreted directly as customer demand or team performance.
* High ticket volume within a support queue was not automatically interpreted as poor performance because workload may reflect the nature and complexity of tickets assigned to that queue.
* The dataset did not contain sufficient operational timestamps to independently measure metrics such as first-response time, escalation duration, or SLA compliance.

# Key Takeaways

The following are the key takeaways from the analysis:

* **Ticket activity followed recurring seasonal patterns**, with February declines followed by March increases and June recording the highest ticket volume at **735 tickets**.
* **Technical Support handled the largest share of the workload at 28.62%**, followed by Product Support at 18.72% and Customer Service at 15.59%.
* **Recurring issue categories represented a significant portion of support activity**, with the top three categories accounting for approximately 39% of categorized tickets and the top five representing approximately 48%.
* **High ticket volume does not necessarily indicate poor support performance**, as workload concentration may reflect the type and complexity of issues handled by each queue.
* **Resolution time was closely aligned with ticket priority**, limiting its usefulness as an independent measure of actual support-team efficiency.
* **Historical ticket patterns can support proactive resource planning**, particularly around periods of higher support activity such as June.
* **Recurring technical and performance-related issues provide opportunities for prevention**, including knowledge-base development, self-service resources, system improvements, and automated troubleshooting.
* **Future datasets should capture additional operational timestamps and dimensions** to support more reliable performance measurement and root-cause analysis.
* Combining **ticket volume, queue workload, recurring issues, priority, resolution patterns, and seasonality** provides a more complete view of IT support operations than ticket volume alone.

# Tools & Technologies

**Data Preparation & Transformation**

* Microsoft Excel, Power Query

**Data Analysis**

* PivotTables
* Calculated fields
* KPI analysis
* Trend analysis

**Data Visualization**

* Excel Charts
* Conditional Formatting
* Interactive Slicers
* Dashboard Development
* Data story-telling

**Analytical Techniques**

* Data profiling
* Data cleaning
* Data transformation
* Descriptive analytics
* Segmentation






