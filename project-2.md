# Project 2 — Used Car Price Analytics Lakehouse (Microsoft Fabric)

**Course:** CIS 409 — Business Data Warehouses & Dimensional Modeling · Arizona State University · Spring 2026
**Type:** Team project (5 members) · **My role:** Data modeling & analytics contributor

---

## Problem Statement
Pricing a used car is a real decision problem for both buyers and sellers, but the factors that actually drive price — brand, mileage, size, accident history, color — are usually discussed by intuition rather than data.

## Objective
Build an end-to-end analytics solution that answers one central question: **How do brand value, mileage, vehicle size, accident history, and color influence used-car prices, and which factors matter most?**

## Tools Used
Microsoft Fabric (Lakehouse) · Power BI (Direct Lake) · Dimensional modeling (star schema) · Kaggle datasets (CSV)

## Methodology
- **Ingestion:** loaded three structured Kaggle datasets (listing-level pricing, brand/year sales data, and color-focused listings) into a Fabric lakehouse.
- **Cleaning:** standardized brand/model/year/mileage/price/color fields, converted numeric types, removed invalid rows, and derived mileage bands (0–20k, 20–60k, 60–100k, 100k+) and an accident/no-accident flag.
- **Dimensional model (star schema):**
  - `FactCarPrice` — one row per listing (price, mileage, year, accident flag, foreign keys)
  - `DimBrand`, `DimCarType/Size`, `DimColor`, `DimAccidentHistory`
- **Visualization:** connected Power BI to the Fabric warehouse via **Direct Lake** to build interactive dashboards on the gold-layer tables.

## Analysis & Results
- **Mileage** was one of the strongest predictors — a clear, moderately strong **negative** relationship with price.
- **Accident history** had a large negative impact on value.
- **Brand** explained which vehicles retained value better over time (comparing prices within the same model year to isolate brand from depreciation).
- **Color** mattered, but much less — bright/uncommon colors (yellow, orange) correlated with higher prices mostly because they appear on specialty/sports models, not because color itself drives value.

**Bottom line:** condition-related variables (mileage, accident history) drive price most; brand drives value retention; appearance is secondary.

## Business Impact
The model gives buyers a data-backed view of what justifies a higher price and gives sellers a rational basis for pricing inventory and trade-ins, rather than relying on gut feel.

## Key Takeaways
This project taught me the full modern data-warehouse stack — lakehouse architecture, star-schema design, and Direct Lake reporting — and reinforced a habit from finance: control for the obvious confounder (here, holding model year constant to separate brand from depreciation) before you trust a relationship.

## Skills Demonstrated
Microsoft Fabric · lakehouse architecture · dimensional modeling / star schema · Power BI (Direct Lake) · data cleaning & feature derivation · analytical interpretation · team collaboration
