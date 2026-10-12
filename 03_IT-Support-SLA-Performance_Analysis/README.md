### IT SLA Support Performance Analysis

Designed an **IT SLA Support Performance Dashboard** using Microsoft Excel to analyze service-level agreement (SLA) performance, ticket resolution status, and support team efficiency. The dashboard transforms ticket data into interactive visual reports, helping users monitor SLA compliance, identify overdue tickets, track resolution performance, and support data-driven decision-making.

---

### 1. SLA Dashboard
![SLA Dashboard](Screenshots/dashboard.png)

---

## Project Overview

The dashboard uses Pivot Tables, Pivot Charts, and interactive filters to summarize ticket data and present important performance indicators in an easy-to-understand format.

The project focuses on:

- SLA compliance monitoring
- Ticket resolution performance
- Open, closed, and overdue ticket analysis
- Support team performance reporting
- Identification of SLA breaches
- Interactive reporting for operational insights

  ---

  ## Business Problem
- An IT support team resolves hundreds of tickets a month. Managers need quick answers to questions such as:
- Are we meeting our SLA target overall?
- Which request types, priorities, agents, regions and countries cause the most breaches?
- Is SLA performance improving or getting worse over time?

This dashboard answers those questions on one screen. Slicers let anyone filter the view without touching the data.

---

## Core Objective
The goal of this project is to demonstrate how ticket data can be transformed into meaningful operational reports. Using Excel data analysis and visualization techniques, the dashboard summarizes SLA performance, tracks ticket status, and helps identify areas that may require further investigation or improvement.

---


## Dataset Overview

| Item | Detail |
|---|---|
| Records | 1,126 support tickets |
| Period | January – December 2024 |
| Columns | Ticket ID, Region, Country, Request Type, Request Description, Priority, Assigned To, Open Date, Close Date, Actual Days, Status, Month |
| Nature | Practice / sample dataset. Not real company or customer data. |

- **SLA Rule used:** A ticket is marked **Not Met** if it takes 1 or more days to close (`Close Date - Open Date >= 1`). Otherwise, it is marked **Met**. The same SLA rule applies to all priority levels.
- **Target SLA:** 94% (assumed target for this practice project).

---

### Data Preparation

- Stored the ticket data as an Excel Table so formulas and pivots expand with the data.
- Added calculated columns: Actual Days (Close Date minus Open Date), Status (IF(Actual Days >= 1,    "Not Met", "Met")) and Month (TEXT(Open Date, "mmm")).
- Built 11 PivotTables from one shared data source and added helper tables (target vs actual) for     the charts.

### KPIs

| KPI | Value |
|---|---|
| Total tickets |	1,126|
| SLA met |1,059 |
| SLA breaches (Not Met) | 67 |
| Overall SLA compliance | 94.05% |

The KPI cards are linked to pivot cells with formulas, so they update automatically.

---

### Dashboard Features
**5 KPI cards:** Overall SLA, Total Tickets, Breach Count, Weakest Performer, Priority to Watch
**6 charts:**
- SLA % by Monthly Trend (actual vs target)
- Breaches by Request Type
- Ticket Volume by Region
- SLA % by Assigned Person
- Breaches by Priority
- SLA Compliance by Country (lowest 5)
 **- 4slicers:** Month, Priority, Request Type and Region, all connected to every PivotTable
**- Key Insights panel** summarising the main findings

  ---

 
## Key Insights

- **Overall SLA Compliance:** 94.05%, with 67 SLA breaches out of 1,126 support tickets.
- **Agent Performance:** Sarah recorded the lowest SLA compliance at 83.7%, while Robert achieved the highest at 99.1%.
- **Priority Analysis:** Medium-priority tickets accounted for 43% of all breaches (29 out of 67).
- **Request Type Analysis:** Access Request had the highest number of breaches (24), followed by Password Reset and VPN Access (10 each).
- **Monthly Performance:** January was the weakest month, with SLA compliance of 81.4%.
- **Country Analysis:** Germany (86.4%) and India (87.7%) recorded the lowest SLA compliance among the countries analyzed.

## Suggested Actions

- **Improve Agent Performance:** Review workloads and provide coaching support to agents with lower SLA compliance.
- **Reduce Access Request Breaches:**Create a self-service guide or automation for Access Request tickets, the most common breach type.
- **Optimize Medium-Priority Ticket Handling:** Review workload distribution, response processes, and escalation procedures for medium-priority tickets.
- **Monitor Monthly Performance:** Investigate the reasons for lower SLA compliance in January and track monthly trends to identify recurring issues.
- **Focus on Low-Performing Countries:** Analyze regional workflows and ticket patterns in Germany and India to identify opportunities for improvement.

---

## Tools and Skills Demonstrated

- **Microsoft Excel:** PivotTables, PivotCharts, Excel Tables, and slicers
- **Excel Formulas:** `GETPIVOTDATA`, `IF`, `IFERROR`, `INDEX`, `MATCH`, and `TEXT`
- **Data Analysis:** SLA compliance, SLA breach analysis, trend analysis, and category-wise and agent-wise performance comparison
- **Dashboard Design:** KPI cards, target vs. actual SLA line chart, consistent colour formatting, and highlighting underperforming areas
- **Business Communication:** turning data into written insights and recommended actions

  ---
 
## What I Learned

- how to structure ticket data so multiple PivotTables can use a common data source.
- how to Connected slicers to multiple PivotTables to make the dashboard interactive.
- how to Link KPI cards to PivotTable results using `GETPIVOTDATA` and `INDEX` / `MATCH`.
- how to check that chart axes and titles describe the data honestly.
---

## Limitations and Assumptions

- The data is a sample dataset created for learning and portfolio practice.
- The SLA rule (1 or more days = Not Met) is the same for all priorities. In a real environment,      High-priority tickets would have a tighter target.
- The 94% target is assumed.
- The Key Insights text is written from the full dataset and does not change when slicers are used.

---

## Possible Improvements

- Use priority-based SLA targets (for example 4h, 8h and 24h).
- Add hour-level resolution times instead of whole days.
- Add first-contact resolution and customer satisfaction (CSAT) metrics.
- Rebuild the same dashboard in Power BI for comparison.

  ---

 ### Project Files

 03_IT-SLA-Performance-Analysis/
├── README.md
├── Dashboard.png
└── Dataset.xlsx

---

### Author

**Sakshi Gadewar** B.E. in Electronics and Telecommunication Engineering | Aspiring Data Analyst | Excel | Power BI | SLA Reporting


**Linkedin** [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/sakshi-gadewar-604175343)
**Github** [![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)](https://github.com/sakshi-gadewar)

