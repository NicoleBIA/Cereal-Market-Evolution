# Perceived_vs_Actual_Price_Data

This dataset explores the gap between **expected (perceived) pricing** and **actual shelf pricing** across retailers and brands. It supports insights into **anchoring bias**, **price trust**, and **consumer value perception** in an inflationary retail environment.

---

## 🔹 Purpose

To simulate the psychological dynamics of price perception by comparing what consumers expect to pay (based on brand, history, or packaging) with actual market prices — providing a foundation for behavioral pricing insights.

---

## 🔹 Key Columns

| Column Name              | Description                                                                  |
|--------------------------|------------------------------------------------------------------------------|
| Entry_ID                 | Unique identifier for each price perception record                           |
| Retailer                 | Retail chain observed                                                        |
| Brand                    | Brand under consideration (store or national)                                |
| Product_Name             | Specific cereal product                                                      |
| Batch_ID                 | Data collection period aligned with price forecasting logic                  |
| Size_oz                  | Product size in ounces                                                       |
| Perceived_Price_USD      | Simulated consumer expectation of product price                              |
| Actual_Price_USD         | Shelf price at the time of observation                                       |
| Price_Delta              | Difference between perceived and actual price                                |
| Region                   | Regional context for perception modeling                                     |

---

## 🔹 Row Count Logic

- Contains **24,000 rows**
- Structured by `Retailer + Brand + Product_Name + Batch_ID`
- Perceived price generated using **anchoring bias models** based on historical pricing, package size, and promotion history
- Allows for regional variance in price sensitivity and perception

---

## 🔹 Use in Power BI

- Supports visuals like **“Perceived vs. Actual Price Scatterplots”** and **“Price Psychology Insights”**
- Enables calculation of **trust metrics** and analysis of price fairness perceptions
- Integrates with promotional and volume data to contextualize pricing strategies

---

## 🔹 Connected Business Questions

- Where are consumers most sensitive to price discrepancies?
- How do actual price increases affect perceived value across retailers?
- Which brands create the greatest gap in expectation vs. reality — and why?
- Can trust in pricing be linked to brand loyalty or switching behavior?

---

## 🔹 Related Tables

- `Cereal_Sales_Pricing_Dataset_Corrected`
- `Loyalty_Brand_Switching_Data`
- `CPI_FoodAtHome_Data`
- `AI_Driven_Price_Projection_Data`
