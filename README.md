Comprehensive Financial & Sales Reporting Suite

Client: UK-Based Lighting Company

Role: Data Analyst / Power BI Developer

Status: Completed

Project Objective

To engineer an automated, end-to-end Power BI reporting suite providing stakeholders across different departments with daily insights into true profitability, granular sales trends, and quote conversions by integrating complex CRM, accounting, and flat-file data.

The Problem

    Siloed Data: Financial and CRM data were scattered across Dynamics 365, Xero Accounting, and flat Excel files (SharePoint).

    Extraction Limitations: Dynamics 365 data was highly complex and restricted within view forms, making standard table extraction impossible.

    Hidden Profitability: Actual net profit was obscured because credit notes from Xero and Excel needed to be manually deducted from gross profits.

    Lack of Unified Reporting: Stakeholders lacked a central hub that separated executive-level summaries from granular, department-specific metrics (Sales and Quotes).

    Manual Bottlenecks: Reporting was highly manual, and stakeholders had no visibility into data currency or refresh times.

Data Architecture & Integration

    Tri-Source Pipeline: Seamlessly connected and integrated three disparate data sources: Microsoft Dynamics 365, Xero Accounting, and Excel (via SharePoint).

    Custom API Pagination (Dynamics 365): Bypassed standard view limitations by engineering a custom M/Power Query function. Utilized an OData feed (odata.maxpagesize=5000) with dynamic pagination logic to extract complex raw data directly from the CRM.

    Data Modeling: Designed a robust relational data model connecting eight core tables: Accounts, Invoice History, Date, Opportunities, Products and Services, Code Headers, System Users, and Xero Credits.

The Solution: A 3-Part Dashboard Suite
I built a cohesive, tabbed Power BI report categorized into three highly focused dashboards:

1. Executive Dashboard

    Calculates and displays true net profit by programmatically extracting live financial data from Xero and supplementary Excel files, automatically deducting credit notes from the gross profit.

    Features custom DAX measures for Year-over-Year (YoY) percentage changes (e.g., highlighting positive/negative shifts with intuitive green and red conditional formatting).

2. Sales Dashboard

    Volume & Value Tracking: Monitors exact KPIs including Invoice Count (e.g., 4,362), Average Invoice Value (£1.55K), and Total Credits (£30.70K).

    Account & Product Visibility: Ranks the Top 20 Accounts (e.g., Widnes Sceptical, CLP Group FS LTD) and Top Products by Sales to identify key revenue drivers.

    Financial Health: Includes a "Xero Status Breakdown" donut chart to track payment statuses (Paid, Awaiting Payment, Authorised, Voided, Draft), with over 80% successfully paid.

    Performance Timelines: Visualizes granular monthly sales trends and estimated revenue broken down by account owner.

3. Quotes Dashboard

    Pipeline Monitoring: Tracks Quote Count (1,047), Total Quote Value (£3.49M), and Average Margin % (38.89%).

    Conversion & State Metrics: Breaks down quotes by state (Active vs. Inactive) and visualizes the monthly quote generation trend.

    Owner & Account Analytics: Details Quote Value and Quote Count by specific account owners, as well as highlighting the top accounts by quote value (e.g., ABCD Asackpool, Edmundson).

Deployment, Security & Administration

    Cloud Deployment: Published the finalized dashboard to Power BI Service and managed gateway data connections.

    Access Control: Configured and assigned specific user roles utilizing Row-Level Security (RLS) to strictly govern data access across different departments.

    Automation: Established scheduled data refreshes to maintain real-time accuracy without manual intervention.

    Executive Subscriptions: Configured automated dashboard subscriptions, delivering high-level snapshot notifications to executives' inboxes daily at 9:00 AM.

    Transparency: Engineered a custom "Last Refreshed" timestamp indicator (e.g., 11 Aug 2026, 22:21) to ensure data transparency for all end-users.

Business Impact

    Eliminated manual data extraction and complex profit calculation by fully automating the pipeline.

    Provided specific departments with targeted, immediate visibility into their exact KPIs across three distinct dashboards.

    Improved executive engagement and decision-making through automated 9:00 AM snapshot deliveries directly to their inboxes.

Regards,

Muhammad Rizwan Khan
