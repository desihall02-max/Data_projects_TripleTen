# 💰 Manhattan Airbnb Market Analysis: Investment Strategy

## Project Overview

This project focuses on analyzing the New York City Airbnb data, specifically within Manhattan, to provide a client with strategic investment guidance. The core objective was to identify the most attractive property types (by neighborhood and size) and quantify their potential revenue generation, using advanced spreadsheet functions and pivot tables.

My role involved transforming raw, complex data into clear, actionable financial recommendations to drive the client's investment decisions in the vacation rental market.

---

## 🎯 Key Questions Addressed

The analysis was structured to answer two primary business questions:

### 1. Which neighborhoods and property sizes are most attractive for investment?

To determine "attractiveness," the analysis used the **number of reviews in the last 12 months (`number_of_reviews_ltm`)** as a proxy for rental frequency and demand.

* **Neighborhood Selection:** Identified the **top 10 most attractive neighborhoods** in Manhattan based on total reviews.
* **Property Size Preference:** Determined the **most popular property sizes (number of bedrooms)** across the dataset.
* **Neighborhood Specialization:** Cross-analyzed the top 10 neighborhoods with property sizes to recommend the **optimal apartment size for investment in each specific neighborhood** (e.g., Harlem vs. Midtown).

### 2. How much money did these most attractive listings generate?

The second stage involved financial modeling to quantify the revenue potential of the highly recommended properties.

* **Top Listing Identification:** Narrowed the listings down to those matching the optimal neighborhood and property size criteria (e.g., 1-bedroom in most top neighborhoods, Studios in Midtown).
* **Revenue Calculation:** Used the `calendar` sheet data to calculate `revenue_earned` for each rented night (`available` = "f") over a 30-day period.
* **Annualized Revenue:** Estimated annual revenue for the top-performing listings by multiplying the 30-day revenue total by 12.

---

## 🛠️ Data Analysis & Spreadsheet Skills

This project required the application of several advanced spreadsheet techniques:

* **Data Cleaning & Preparation:**
    * Created clean data columns (`neighborhood_clean`, `bedrooms_clean`).
    * Handled inconsistent capitalization and trailing spaces in text fields.
    * Used the **`IF()`** function to replace empty cells in the `bedrooms` column with `0` (representing studios).
* **Pivot Table Creation:** Extensively used Pivot Tables for:
    * Ranking the top 10 neighborhoods by demand (`number_of_reviews_ltm`).
    * Counting the popularity of property sizes (Studios, 1-bedrooms, 2-bedrooms, etc.).
    * Cross-tabulating neighborhood demand against property size preferences.
* **Financial Modeling:**
    * Used the **`IF()`** function and price data to calculate daily revenue.
    * Used the **`SUMIF()`** function to aggregate total 30-day revenue for specific listings.
    * Created a calculated field for **Annual Estimated Revenue** (30-day revenue x 12).
* **Data Filtration & Recommendation:** Created a new binary column (`top_listing`) to filter and analyze only the properties that matched the final investment criteria.

---

## 🔑 Key Investment Recommendations

The final analysis provided a highly refined strategy based on demand and revenue:

* **High-Demand Property Sizes:** Studios, 1-bedrooms, and 2-bedrooms were identified as the most popular overall property sizes.
* **Neighborhood Specialization:** The analysis confirmed that **1-bedroom** listings were the optimal investment size for nearly all top 10 neighborhoods, with the key exception being **Midtown**, where **Studios** were most popular.
* **Top Revenue Generator:** Identified the single top-earning listing ID and projected its substantial **estimated annual revenue**.

---

## 🗃️ Project Deliverables

* **Executive Summary and Table of Contents:** Provided a clear project overview and navigation.
* **Change Log:** Documented all assumptions and data cleaning steps (e.g., neighborhood and bedroom cleaning).
* **Data Analysis:** Pivot tables and supporting bar charts for top 10 neighborhoods and property size popularity.
* **Final Report:** A recommendation focused solely on the most attractive, high-revenue listings.
