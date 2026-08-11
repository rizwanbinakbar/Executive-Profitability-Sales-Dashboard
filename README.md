# Executive Profitability & Sales Dashboard

Comprehensive financial and sales reporting suite built with Power BI for a UK-based lighting company.

- **Client:** UK-Based Lighting Company  
- **Role:** Data Analyst / Power BI Developer  
- **Status:** Completed

---

## Project Objective
Design and deliver an automated, end-to-end Power BI reporting suite that provides daily insights into true profitability, granular sales trends, and quote conversion performance for stakeholders across departments.

---

## The Problem
- **Siloed data:** Financial and CRM data lived in Dynamics 365, Xero Accounting, and Excel files on SharePoint.  
- **Extraction limitations:** Dynamics 365 data was complex and restricted by view forms, preventing standard table extraction.  
- **Hidden profitability:** Net profit was obscured due to credit notes in Xero and Excel that required manual deductions from gross profit.  
- **Lack of unified reporting:** No central reporting hub separating executive summaries from department-level metrics.  
- **Manual bottlenecks:** Reporting processes were manual and stakeholders lacked visibility into data currency and refresh times.

---

## Data Architecture & Integration
- **Tri-source pipeline:** Integrated Dynamics 365, Xero, and Excel (SharePoint) into a single automated ETL pipeline.  
- **Custom pagination for Dynamics 365:** Engineered a custom M / Power Query function to paginate an OData feed (odata.maxpagesize=5000) and reliably extract records beyond standard view limits.  
- **Data modeling:** Built a relational model linking core tables: Accounts, Invoice History, Date, Opportunities, Products & Services, Code Headers, System Users, and Xero Credit Notes.  
- **Automation & refreshes:** Scheduled refreshes via Power BI Gateway to keep data current and reduce manual effort.

---

## Solution — 3-Part Power BI Dashboard Suite
A single Power BI report with three focused dashboards (tabbed) to serve different audiences:

### 1) Executive Dashboard
- Displays true net profit by programmatically combining live Xero financials and supplemental Excel adjustments (automatically deducts credit notes).  
- Custom DAX measures for YoY percentage change with conditional formatting to highlight positive/negative shifts.  
- High-level KPIs and executive-friendly visuals for fast decision making.

### 2) Sales Dashboard
- Tracks key KPIs: Invoice Count (example: 4,362), Average Invoice Value (example: £1.55K), Total Credits (example: £30.70K).  
- Top 20 Accounts and Top Products by sales to identify revenue drivers.  
- "Xero Status Breakdown" donut chart to monitor invoice payment states (Paid, Awaiting Payment, Authorised, Voided, Draft) — >80% Paid in the sample dataset.  
- Monthly trend visualizations and estimated revenue by account owner.

### 3) Quotes Dashboard
- Monitors Quote Count (example: 1,047), Total Quote Value (example: £3.49M), and Average Margin (example: 38.89%).  
- Conversion and quote-state metrics (Active vs. Inactive) and monthly quote generation trends.  
- Owner- and account-level analytics highlighting top accounts by quote value (examples: ABCD Asackpool, Edmundson).

---

## Deployment, Security & Administration
- **Cloud deployment:** Published to Power BI Service and configured gateway data connections.  
- **Access control:** Implemented Row-Level Security (RLS) to restrict data access by role/department.  
- **Automation:** Scheduled dataset refreshes to maintain real-time accuracy without manual intervention.  
- **Executive subscriptions:** Configured daily 09:00 AM snapshot subscriptions for executive distribution.  
- **Transparency:** Added a "Last Refreshed" timestamp indicator (example: 11 Aug 2026, 22:21) so users always know data currency.

---

## Business Impact
- Eliminated manual data extraction and manual profit calculations through full pipeline automation.  
- Delivered targeted visibility across departments with three distinct dashboards tailored to user needs.  
- Increased executive engagement and improved decision-making through automated daily snapshots.

---

## Contact
Muhammad Rizwan Khan  
(Data Analyst / Power BI Developer)  
GitHub: @rizwanbinakbar
