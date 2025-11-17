# 📈 E-commerce Conversion Funnel & Cohort Analysis

## Project Overview

This project was a foundational assignment for a Junior Data Analyst at an e-commerce company, focused on transforming raw, event-level transaction logs into key business metrics. The primary goals were to **construct a conversion funnel** to understand user flow and **prepare and calculate retention rates** via a detailed cohort analysis.

The analysis heavily relied on advanced spreadsheet techniques, including pivot tables, lookup functions (`VLOOKUP`), and date manipulation (`TEXT`, `DATEDIF`), to structure raw user activity data into actionable insights for the executive team.

## 💾 Dataset & Raw Data Structure

The analysis began with raw user activity logs, where each row represented an event on the company's website.

**Key Data Columns:**

| Column Name | Description |
| :--- | :--- |
| `user_id` | Unique customer identifier. |
| `event_type` | Type of user activity (e.g., `view`, `cart`, `purchase`). |
| `category_code` | Product category. |
| `brand` | Product manufacturer. |
| `price` | Product price in USD. |
| `event_date` | Date of the user activity (`YYYY-MM-DD`). |

## 📊 Part 1: Conversion Funnel Analysis

The first task was to evaluate website effectiveness by building a conversion funnel to track the user journey from product discovery to purchase.

* **Funnel Stages:**
    1.  Product Page Views
    2.  Shopping Cart Opens
    3.  Purchases
* **Methodology:** Used a Pivot Table to count the **unique users** at each stage of the funnel.
* **Metrics Derived:** Calculated two critical business metrics using formulas:
    * **Total Conversion Rate:** Percentage of users who start the funnel and complete a purchase.
    * **Step-by-Step Conversion Rate:** The drop-off rate between successive steps (e.g., from view to cart, and from cart to purchase).

## 📅 Part 2 & 3: Cohort Retention Analysis

The main focus of the project was building the data infrastructure required for a month-by-month cohort analysis based on user acquisition.

### Data Preparation Steps:

1.  **Filtering Purchases:** Isolated all `purchase` events into a dedicated `purchase_activity` sheet.
2.  **Calculating First Purchase Date:** Used a Pivot Table to find the `MIN(event_date)` for each user, representing their acquisition date.
3.  **Mapping Acquisition Date:** Employed the **`VLOOKUP()`** function to map the `first_purchase_date` back to every row in the `purchase_activity` sheet.
4.  **Date Transformation:** Created monthly grouping columns:
    * `event_month` and `first_purchase_month` using the **`TEXT()`** function (`YYYY-MM` format).
5.  **Cohort Age Calculation:** Determined the **`cohort_age`** (months elapsed between first purchase and current event) using the **`DATEDIF()`** function.

### Retention Rate Calculation:

* **Grouping:** A second Pivot Table (`cohort_analysis`) was constructed with `first_purchase_month` as rows (defining the cohorts) and `cohort_age` as columns. Values were the count of unique users.
* **Retention Table:** Calculated month-by-month retention rates for each cohort based on their starting size (Cohort Age 0), demonstrating user loyalty and product stickiness over time.

## 🛠️ Key Spreadsheet Skills Demonstrated

| Function/Tool | Purpose in Project |
| :--- | :--- |
| **Pivot Tables** | Building the Conversion Funnel, finding the Minimum First Purchase Date, and aggregating Cohort Data. |
| **`VLOOKUP()`** | Mapping a user's initial acquisition date back to every single transaction row for cohort assignment. |
| **`IF()` / Filters** | Isolating 'purchase' events from raw activity logs. |
| **`TEXT(date, "YYYY-MM")`** | Standardizing dates for consistent monthly grouping. |
| **`DATEDIF()`** | Calculating the `cohort_age` in months for retention tracking. |
| **Reference Fixing** | Using fixed column/row references in retention formulas to accurately calculate percentages across a dynamic cohort table. |

## ✨ Outcome & Impact

The project successfully delivered two core business assets: a **conversion funnel** providing immediate insight into user drop-off points, and a robust **cohort analysis** structure that now enables the executive team to monitor the long-term value and retention of customers acquired each month.
```
