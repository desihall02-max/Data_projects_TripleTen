# 📈 Shopify App Store Analysis: Success Factors & Developer Insights (Power BI)

## Project Overview

This project was a deep-dive analysis of the Shopify App Store landscape, utilizing publicly available scraped data to determine the key factors that contribute to an app's success. The findings were delivered through a comprehensive, multi-page report built in **Power BI**, showcasing proficiency in data modeling, custom DAX measures, and focused data visualization.

The analysis aimed to move beyond surface-level metrics to identify actionable insights for developers and investors in the e-commerce app ecosystem.

---

## 💾 Dataset & Data Modeling

The analysis was based on a structured dataset containing four primary tables, requiring careful establishment of relationships for cross-table metrics:

* **`apps`**: Details about the apps (ID, developer, last modification date).
* **`apps_categories`**: Bridge table connecting apps and categories (many-to-many relationship).
* **`categories`**: App category names.
* **`reviews`**: Detailed user reviews (rating, comment, helpful count, developer reply).

### Key Data Modeling Step:
* A **many-to-one relationship** was created between the `Reviews` table (many) and the `Apps` table (one) using the `app_id` and `id` columns, allowing review data to be aggregated and analyzed against app details like the developer.

---

## 💻 Technical Skills Demonstrated

This project involved significant work in both the Power BI interface and advanced DAX formula language:

### DAX Formula Creation:

1.  **`helpful_reviews` (Calculated Column):** Created a weighted review score using the formula `rating * (1 + helpful_count)` to prioritize reviews that users found most useful.
2.  **`developer_answered` (Calculated Column):** Created a binary flag (`1` or `TRUE` if `developer_reply` is not blank, `0` or `FALSE` otherwise) to measure developer responsiveness.

### Power BI & Visualization:

* **Custom Visuals:** Utilized various chart types including KPI Cards, Line Charts, and Scatterplots.
* **Drill-Down Filtering:** Applied visual-level filters (e.g., filtering for apps with `reviews_count` > 500) to ensure meaningful, non-skewed analysis.
* **Annotation:** Used Power BI's built-in text box functionality to annotate visualizations, providing immediate context and interpretation for complex relationships (e.g., the relationship between review count and average rating).

---

## 📊 Report Pages & Key Insights

The final Power BI report was organized into three distinct pages, each focusing on a different aspect of app success:

### Page 1: App Landscape

* **Unique App Count:** Used a KPI Card to establish the size of the total market.
* **Review Trends:** Line chart tracking the **Sum of Review Count over Time (`lastmod date`)** to understand market growth and review velocity.
* **Success Correlation:** Scatterplot comparing `reviews_count` (X-axis) vs. `average rating` (Y-axis) to visually assess the correlation between volume and quality.

### Page 2: Reviews

* **Weighted Quality:** Card displaying the **Average `helpful_reviews`** to show the overall perceived quality of the app ecosystem.
* **Responsiveness Impact:** Scatterplot comparing average `rating` against the `developer_answered` flag to determine if developer responses correlate with higher user ratings.

### Page 3: App Reviews & Developer Performance

* **Developer Quality:** Bar charts comparing developers based on both raw `sum of rating` (showing potential bias) and the more accurate **average `helpful_reviews`**.
* **Responsiveness Ranking:** Bar chart ranking developers by the count of their `developer_answered` flag, filtered to only include apps with high review volume (`reviews_count > 500`), thereby identifying the **most responsive and engaged developers** in the high-stakes app segment.
```
