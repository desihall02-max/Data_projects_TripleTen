# 📈 Storytelling with Data: Reducing Superstore Returns (Tableau)

## Project Overview

This was a capstone project focused on solving the high volume of returned orders at the Superstore. The objective was not only to perform a deep root-cause analysis but also to **design a comprehensive, executive-level data story and monitoring dashboard** specifically for the CEO.

The analysis required expertise in data preparation, advanced visualization techniques, and, critically, the ability to **construct a persuasive narrative** that clearly outlines the problem, its causes, and actionable solutions. All deliverables, including the analysis, dashboard, and story, were developed using **Tableau**.

---

## 🔬 Part 1: Root Cause Analysis

The initial phase involved rigorous data preparation and building various visual arguments to uncover the drivers of returned orders.

### Data Preparation:
* **Data Joining:** Executed a **LEFT JOIN** on the `Orders` and `Returns` tables to ensure all original orders were present for accurate rate calculation.
* **Metrics Creation:** A calculated field was created to quantify returns (null $\rightarrow$ 0, Yes $\rightarrow$ 1). This field allowed for the calculation of the **Return Rate (Average)** and the **Total Volume of Returns (Sum)**.

### Key Visualizations Developed:

1.  **Sales vs. Returns:** Scatterplot to check for correlation between total sales and total returns, aggregated by **Product Subcategory**.
2.  **Product Risk:** Bar chart showing **Return Rate by Product Category** to highlight high-risk inventory.
3.  **Customer Behavior:** Bar chart showing Return Rate by Customer, filtered to remove single-order customers to identify **high-frequency returners**.
4.  **Geographic Concentration:** Map visualization showing **Return Rate by State or City**.
5.  **Seasonal Effects:** Time series visualization showing **Return Rate by Month or Week**.
6.  **Composite Factors:** Two different charts analyzing return rate across combinations of multiple factors (e.g., date, geography, shipping mode, and product category).

---

## 🖼️ Part 2: Dashboard Design and Implementation

The findings from the root cause analysis were consolidated into a monitoring tool.

* **Design & Mock-ups:** Created **low-fidelity, pen-and-paper mock-ups** to plan the dashboard layout and ensure optimal information flow, demonstrating user-centric design principles.
* **Implementation:** Created the finalized interactive dashboard in Tableau, matching the chosen mock-up template and incorporating necessary filters and titles.

---

## 🗣️ Part 3: Storytelling and Presentation

This phase focused on creating a full presentation narrative using the Tableau Story feature.

### Story Arc Components:

1.  **Problem Definition:** Defined **how to measure returns** (rate vs. volume vs. cost) and when each metric is most appropriate for business decision-making.
2.  **Key Root Causes:** A sequence of story points dedicated to presenting the most salient findings from the analysis (e.g., high-risk categories, problematic geographic zones).
3.  **Dashboard Demonstration:** Provided an explanatory overview of each dashboard component and a **step-by-step demonstration** of how the CEO or operations manager would use filters to diagnose issues in real-time.
4.  **Actionable Conclusion:** Outlined specific, proposed next steps and actions (e.g., updating quality control for certain product lines, implementing a stricter return policy for identified high-risk customers).

---

## 🚀 Skills & Tools

| Category | Tool / Skill Demonstrated |
| :--- | :--- |
| **Data Visualization** | **Tableau**, creating multiple customized charts (scatterplots, maps, composite charts). |
| **Data Preparation** | **LEFT JOIN**, creating robust, analytical calculated fields for rate calculations. |
| **Business Strategy** | Translating data into actionable strategies for **reducing loss** and **optimizing operations**. |
| **Communication** | **Building a full Tableau Story** (narrative arc) and delivering a timed presentation to executive stakeholders. |
| **Design** | Low-fidelity dashboard mock-ups and high-fidelity dashboard implementation. |
