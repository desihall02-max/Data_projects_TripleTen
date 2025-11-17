# 📊 Superstore Profitability & Operational Review (Tableau)

## Project Overview

This project involved acting as a consultant for a struggling "Superstore" to reverse declining profitability and avoid bankruptcy. The core objective was to utilize the provided sales and returns data (`Superstore.xls`) to identify key drivers of profit and loss, optimize product offerings, and determine the most cost-effective advertising strategy.

The entire analysis was conducted and presented using **Tableau**, demonstrating the ability to craft compelling, individualized visualizations to support specific business conclusions and recommendations.

## 🎯 Business Questions & Visual Arguments

The analysis was structured into three parts, each focused on solving a critical business problem through data visualization:

### Part 1: Profit & Loss Identification

**Objective:** Isolate specific dimensions (e.g., product category, region) that are major financial contributors or liabilities.

* **Key Deliverables:**
    * Visualization identifying the **two biggest profit centers** and the **two biggest loss-makers** across all dimensional pairs (e.g., `Subcategory + Region`).
    * Visualization supporting the recommendation of **which products to stop selling** due to chronic unprofitability.
    * Visualization and recommendation for the **top 3 product subcategories to focus on** and the **3 subcategories to discontinue**.

### Part 2: Advertising Strategy Optimization

**Objective:** Determine the optimal timing and location for advertising based on profit per unit sold, ensuring a high Return on Ad Spend (ROAS).

* **Key Deliverables:**
    * Visualization identifying the **3 best combinations of State and Month** for advertising, based on average profit per unit.
    * A compelling visual argument and calculation for the maximum amount the store should be willing to pay for advertising in those specific windows, based on the principle of spending **1/5 of anticipated profits**.

### Part 3: Return Rate Analysis & Operational Review

**Objective:** Utilize the `Returns` table to identify high-risk products, analyze customer behavior, and evaluate business segments based on profitability versus return rate.

* **Data Preparation:** Created a calculated field to transform the `Returned` status (null/Yes) into a quantifiable metric (0/1) for rate calculation.
* **Key Deliverables:**
    * Visualization identifying the individual **products with the highest return rates**.
    * Visualization identifying the individual **customers with the highest return rates**.
    * A comparative visualization plotting **Average Profit vs. Average Return Rate** across a chosen business dimension (e.g., Shipping Mode) to argue whether the Superstore should continue or discontinue operations within that segment.

## 💻 Technical Skills Demonstrated

| Tool / Technique | Application in Project |
| :--- | :--- |
| **Tableau Desktop** | Primary tool for data connection, visual design, and analysis. |
| **Data Joining** | Used a **LEFT JOIN** to merge the `Returns` table with the `Orders` table to capture all transactions, including non-returned items. |
| **Calculated Fields** | Created the **Return Rate Field** (`IF [Returned] = 'Yes' THEN 1 ELSE 0 END`) for quantitative analysis. |
| **LOD Expressions (Implicit)** | Utilized aggregation and fixed calculations within visualizations to determine profit/loss centers and average metrics. |
| **Business Storytelling**| Developed multiple, focused visualizations, where *each chart* served as a self-contained justification for a specific recommendation. |
| **Financial Modeling** | Applied business logic (1/5th profit advertising budget) directly to visualized data. |
