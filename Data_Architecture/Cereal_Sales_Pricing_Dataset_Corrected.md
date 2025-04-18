# 🥣 Cereal_Sales_Pricing_Dataset_Corrected

This is the **core dataset** in the Cereal Market Evolution project. It simulates realistic cereal sales data across major U.S. retailers, accounting for inflation, shrinkflation, pricing behavior, and promotional patterns. 

---

## 🔹 Purpose

To serve as the central fact table capturing transactional-level cereal sales across brands, packaging sizes, and promotion types—enabling trend analysis, margin tracking, and strategic insights.

---

## 🔹 Key Columns

| Column Name             | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| Entry_ID                | Unique identifier for each transaction row                                 |
| Batch_ID                | Groups sales entries by bi-monthly collection period                       |
| Retailer                | Name of the retailer (e.g., Walmart, Kroger, Costco)                        |
| Brand                   | National or private label cereal brand                                     |
| Product_Name            | Specific cereal product (e.g., Honey Oats Crunch, Organic Corn Flakes)      |
| Size_oz                 | Package size in ounces                                                      |
| Price_USD               | Shelf price in U.S. dollars                                                 |
| Promotion               | Type of promotion (e.g., BOGO, 10% Off, Clearance, No Promotion)           |
| Sales_Volume_Units      | Total units sold during the batch period                                   |
| Date                    | Date of entry (aligned with Batch_ID and retailer activity)                |
| Region                  | Geographic sales region (e.g., Midwest, Northeast)                         |

---

## 🔹 Row Count Logic

- Dataset contains **99,500 rows**
- Each retailer is represented across **bi-monthly batches**
- Includes all major national brands + exclusive private labels
- Promotion activity creates repeat entries for products across time

---

## 🔹 Use in Power BI

- Connected to **companion tables** via `Retailer_Batch_Key`
- Used to calculate **Total Sales**, **Average Price per Ounce**, and **Promotion Impact**
- Enables dynamic filtering by **Retailer**, **Brand**, **Promotion**, and **Time**

---

## 🔹 Connected Business Questions

- What are the monthly and yearly revenue trends by retailer and brand?
- How do promotions affect unit sales and total revenue?
- How do sales patterns vary by region or product size?
- What are the high-volume but low-margin areas in the portfolio?

---

## 🔹 Related Tables

- `Loyalty_Brand_Switching_Data`
- `Perceived_vs_Actual_Price_Data`
- `Price_Sensitivity_Score_Data`
- `AI_Driven_Price_Projection_Data`
- `CPI_FoodAtHome_Data`

---
