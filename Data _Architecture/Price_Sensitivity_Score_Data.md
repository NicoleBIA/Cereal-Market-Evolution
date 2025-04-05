# 💸 Price_Sensitivity_Score_Data

This dataset quantifies **consumer price sensitivity** by retailer and product, supporting elasticity analysis, promotional strategy refinement, and margin optimization.

---

## 🔹 Purpose

To assign a **Price Sensitivity Score** (PSS) between 0 and 1 for each product at each retailer, indicating how likely consumers are to change purchase behavior in response to pricing changes.

---

## 🔹 Key Columns

| Column Name              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Entry_ID                 | Unique record identifier                                                    |
| Retailer                 | Name of retailer (e.g., Target, Walmart, Costco)                            |
| Brand                    | Cereal brand name                                                           |
| Product_Name             | Name of cereal product                                                      |
| Size_oz                  | Package size in ounces                                                      |
| Price_USD                | Standard (non-discounted) price                                             |
| Promotion                | Most common promotion type applied historically                            |
| Price_Sensitivity_Score  | Score between 0 (not sensitive) and 1 (highly sensitive)                    |
| Segment_Label            | Categorical group: Low, Medium, or High Sensitivity                         |

---

## 🔹 Row Count Logic

- ~30,000 rows representing distinct **Retailer + Brand + Product_Name** combinations
- Scores generated based on sales variance, promotion responsiveness, and volume trends over time
- Segment labels derived using quantile binning logic (AI-assisted scoring)

---

## 🔹 Use in Power BI

- Drives **Key Influencers** analysis and discount effectiveness visuals
- Enables **price elasticity mapping** for brands and product categories
- Supports strategic visuals like
