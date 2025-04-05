# 📊 CPI_FoodAtHome_Data

This dataset contains **Year-over-Year Consumer Price Index (CPI)** data for the Food-at-Home category, used as a macroeconomic benchmark for simulating inflationary trends in cereal pricing.

---

## 🔹 Purpose

To provide a realistic economic layer to the dataset, enabling historical inflation analysis, price change justification, and forecasting alignment for retail price simulation and consumer response.

---

## 🔹 Key Columns

| Column Name              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| CPI_Record_ID            | Unique identifier for each CPI record                                      |
| Year                     | Calendar year                                                              |
| Quarter                  | Quarter of the year (Q1–Q4)                                                |
| YoY_CPI_Percent_Change   | Year-over-year CPI % change for Food-at-Home category                      |
| Source                   | Indicated as synthetic data modeled after U.S. Bureau of Labor Statistics |
| CPI_Tier_Label           | Bucketed classification (Low, Moderate, High Inflation)                    |

---

## 🔹 Row Count Logic

- Contains **24 rows** (one for each quarter from 2019 to 2024)
- Used only for **Year-over-Year inflation calculations**, not transaction-level data
- Simplified for interpretability and joined into pricing visuals using `Year + Quarter`

---

## 🔹 Use in Power BI

- Used to annotate visuals and provide economic context in dashboards
- Integrated into **AI price projections** for inflation-adjusted price forecasting
- Used as a filter and reference in **CPI Impact on Pricing and Loyalty** visuals

---

## 🔹 Connected Business Questions

- How have inflation patterns impacted cereal pricing since 2020?
- Did consumer switching behavior increase during high-inflation periods?
- Are some retailers better at buffering CPI-driven price hikes than others?

---

## 🔹 Related Tables

- `AI_Driven_Price_Projection_Data`
- `Cereal_Sales_Pricing_Dataset_Corrected`
- `Perceived_vs_Actual_Price_Data`
