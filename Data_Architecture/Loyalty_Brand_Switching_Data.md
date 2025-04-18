# 🔄 Loyalty_Brand_Switching_Data

This dataset tracks **brand switching behavior and loyalty indicators** at the retailer-product level. It supports behavioral segmentation, consumer retention analysis, and strategy recommendations around pricing and promotion design.

---

## 🔹 Purpose

To simulate real-world loyalty data by identifying which consumers repeatedly purchase the same brand vs. those who switch in response to price, promotion, or availability.

---

## 🔹 Key Columns

| Column Name              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Entry_ID                 | Unique identifier for each loyalty entry                                   |
| Date                     | Date of observation (bi-monthly format)                                    |
| Retailer                 | Retail chain (e.g., Walmart, Kroger, Sam's Club)                            |
| Retailer_Batch_Key       | Primary key for linking across tables                                      |
| Brand                    | Cereal brand being analyzed                                                |
| Product_Name             | Name of the product purchased                                               |
| Size_oz                  | Product package size                                                       |
| Price_USD                | Shelf price at time of purchase                                            |
| Promotion                | Promotion type (if any) during the transaction                             |
| Sales_Volume_Units       | Units sold for the product in that period                                  |
| UPC_Code                 | Simulated unique product identifier                                        |
| Region                   | Geographic sales region                                                    |
| Previous_Purchase_Brand | Brand purchased in the previous batch by same simulated customer segment   |
| Switch_Frequency_Score   | Score from 0 (never switches) to 1 (always switches)                       |

---

## 🔹 Row Count Logic

- Contains **35,000 rows**
- Structured to simulate repeated purchase behavior across time
- Includes brand switching data per retailer and customer segment
- `Switch_Frequency_Score` derived using probabilistic AI logic for segmentation

---

## 🔹 Use in Power BI

- Drives loyalty dashboards and customer segmentation visuals
- Connected to `Cereal_Sales_Pricing_Dataset_Corrected` via `Retailer_Batch_Key`
- Used in visuals like **“Sales Volume by Brand and Loyalty Behavior”** and **“Malt-O-Meal Loyalty Spotlight”**

---

## 🔹 Connected Business Questions

- Which brands have the highest retention rates per retailer?
- What promotions are most effective in reducing switch frequency?
- Where are consumers most likely to switch from national to store brands?
- Which products demonstrate intra-brand stickiness?

---

## 🔹 Related Tables

- `Cereal_Sales_Pricing_Dataset_Corrected`
- `Price_Sensitivity_Score_Data`
- `AI_Driven_Price_Projection_Data`
