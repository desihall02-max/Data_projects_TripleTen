# 🚀 Venture Capital Investment Analysis (VentureInsight)

## Project Overview

This project served as the initial assignment for a Data Analyst at **VentureInsight**, a research firm providing critical analytics to Venture Capital (VC) firms and startup investors. The objective was to leverage a comprehensive relational database to generate key insights that would inform the firm's upcoming quarterly investment report.

This analysis focused on mastering the provided database structure, utilizing SQL to extract, join, and aggregate data across various tables related to funding, acquisitions, and personnel to create actionable investment recommendations.

## 💾 Database & Data Modeling

The project required a deep understanding of a complex relational database structure . The analysis involved joining and querying data from the following key tables:

* `company`: Core information about startups (funding, status, category).
* `fund`: Details about the venture capital funds involved.
* `funding_round`: Records specific investment rounds (date, amount).
* `investment`: Detailed records of specific VC investments.
* `acquisition`: Information regarding company acquisitions.
* `people`: Details about founders, employees, and investors.
* `education`: Educational backgrounds of key people.

## 🎯 Analytical Objectives

The series of analysis tasks were designed to provide a comprehensive view of the VC landscape, likely answering questions such as:

1.  **Funding Dynamics:** What are the average funding amounts and valuation changes across different startup categories or funding stages?
2.  **Investor Performance:** Which VC funds are the most active, and which have the highest rate of successful exits (acquisitions)?
3.  **Talent & Education:** Are there specific educational backgrounds or institutions that correlate with higher startup success rates or funding outcomes?
4.  **Acquisition Trends:** Analyzing the frequency, size, and timeline of successful startup acquisitions.
5.  **Geographic Hotspots:** Identifying geographic areas that show the highest concentration of funding or successful exits.

## 💻 SQL Skills Demonstrated

To successfully complete the analysis series, the following advanced SQL concepts and techniques were required:

* **Complex Joins (`INNER`, `LEFT`, `RIGHT`):** Successfully linking data across multiple tables (e.g., joining `company`, `funding_round`, and `investment` to track a fund's portfolio).
* **Aggregation and Grouping (`GROUP BY`, `SUM`, `AVG`, `COUNT`):** Calculating metrics such as average funding round size by year, or counting the number of investments per fund.
* **Filtering (`WHERE`):** Isolating data based on specific criteria (e.g., companies with a status of 'acquired' or funding rounds after a certain date).
* **Subqueries and CTEs (Common Table Expressions):** Creating temporary result sets for multi-step data processing and complex metric calculation.
* **Data Cleaning:** Utilizing SQL functions to standardize names, handle null values, and ensure data integrity prior to analysis.

## ✨ Outcome & Impact

The analysis contributed directly to the quarterly investment report by providing **data-driven validation** for investment theses. The insights helped clients:

* **De-risk Investments:** By highlighting historical success rates across categories and geographies.
* **Identify Emerging Trends:** By tracking shifts in funding activity and acquisition patterns.
* **Benchmark Performance:** By comparing portfolio performance against industry-wide metrics.
