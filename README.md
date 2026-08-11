# Executive-Profitability-Sales-Dashboard
An automated Power BI workflow for executive profitability, sales, and YoY performance reporting
Client: UK-Based Lighting Company

Role: Data Analyst / Power BI Developer

Status: Completed (Financials & sensitive data redacted for portfolio)

Project Objective

To engineer an automated, end-to-end Power BI dashboard providing executives with daily insights into true profitability, sales opportunities, and Year-over-Year (YoY) performance by integrating complex CRM, accounting, and flat-file data.

Data Architecture & Integration

    Tri-Source Integration: Seamlessly connected three disparate data sources: Microsoft Dynamics 365, Xero Accounting, and Excel (via SharePoint).

    Custom API Pagination (Dynamics 365): Bypassed standard view limitations by engineering a custom M/Power Query function. Utilized an OData feed (odata.maxpagesize=5000) with dynamic pagination logic to extract complex raw data directly from the CRM.

    True Profit Calculation: Extracted live financial data from Xero and integrated supplementary credit data from SharePoint Excel files to programmatically deduct credit notes from gross profit, revealing the actual net profit.

Data Modeling

    Designed a robust relational data model connecting eight core tables: Accounts, Invoice History, Date, Opportunities, Products and Services, Code Headers, System Users, and Xero Credits.

Dashboard Features & DAX Engineering

    Executive KPI Tracking: Engineered custom DAX measures to calculate YoY percentage changes (e.g., 38.4% vs. last year's same period).

    Conditional Formatting: Implemented intuitive visual cues (green/red indicator boxes) on KPI cards for immediate executive performance scanning.

    Refresh Tracking: Built a custom "Last Refreshed" timestamp indicator to ensure data transparency and save users time when verifying data currency.

Deployment, Security & Administration (Power BI Service)

    Cloud Deployment: Published the finalized dashboard to Power BI Service and managed gateway data connections.

    Access Control: Configured and assigned specific user roles (Row-Level Security) to govern data access across different departments.

    Automation: Established scheduled data refreshes to maintain real-time accuracy without manual intervention.

    Executive Subscriptions: Configured automated dashboard subscriptions, delivering high-level snapshot notifications to executives' inboxes daily at 9:00 AM.
