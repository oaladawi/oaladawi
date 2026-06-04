# Project 1 — Superstore Sales Analysis (Python)

**Course:** CIS 404 — Programming Analytics & AI in Business · Arizona State University · Spring 2026
**Type:** Team project (5 members) · **My role:** Analytics & reporting contributor

---

## Problem Statement
A retail "Superstore" had four years of transactional data (2014–2017) but no clear, repeatable way to turn it into decisions. Sales and profit patterns were buried in roughly 10,000 order records spanning regions, customer segments, and product categories.

## Objective
1. Build a clean, **reproducible Python analytics pipeline** that prepares the data for analysis.
2. Engineer meaningful business features (profit margin, shipping duration, loss-making flags).
3. Run exploratory analysis to answer three questions: How do sales and profit move over time? Which segments drive revenue? How does performance differ by region and category?
4. Convert the findings into practical business recommendations.

## Tools Used
Python · pandas · numpy · matplotlib · seaborn · Spyder (development) · Google Colab (shared collaboration)

## Methodology
- **Data cleaning:** standardized column names, dropped non-analytical fields (Row ID, Customer Name, Country, Postal Code), converted Order/Ship dates to datetime, checked nulls, enforced numeric types on financial fields.
- **Feature engineering:** calculated ship duration (days between order and ship), profit margin, and flags for loss-making orders.
- **EDA:** monthly time-series charts, segment-level views, and regional/category breakdowns using line, area, and stacked bar charts.
- Kept all logic in code and mirrored it between Spyder and a shared Colab notebook so any teammate could re-run the full pipeline.

## Analysis & Results
- The dataset held **9,994 order-level records across 21 columns**.
- **Steady sales growth over time**, with clear **seasonal peaks**.
- The **Consumer segment dominated** revenue relative to Corporate and Home Office.
- Meaningful differences appeared **across regions (West, East, Central, South) and categories (Furniture, Office Supplies, Technology)**, including pockets of loss-making orders worth attention.

## Business Impact
We translated the patterns into concrete recommendations around **inventory planning, targeted marketing, regional strategy, and product mix** — for example, leaning into seasonal peaks and re-examining categories/regions where margins were thin or negative.

## Key Takeaways
A reproducible pipeline is worth more than a one-off chart. Because the whole workflow lived in code, our analysis was transparent and any team member (or the TA) could reproduce it end to end. That discipline — clean inputs, documented steps, repeatable output — is exactly what I carry into financial modeling.

## Skills Demonstrated
Python data analysis · data cleaning & feature engineering · EDA & visualization · reproducible workflows · translating analysis into business recommendations · team collaboration
