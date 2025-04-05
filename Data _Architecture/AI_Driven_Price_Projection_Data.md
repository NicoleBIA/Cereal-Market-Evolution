# AI_Driven_Price_Projection_Data

This dataset uses AI-driven logic to simulate **future pricing scenarios** by retailer, brand, and product — based on historical sales trends, CPI data, and promotional behavior.

---

## 🔹 Purpose

To model projected shelf prices using predictive indicators such as past pricing trends, batch-level CPI inflation, and brand-specific discount patterns. Supports strategic pricing, margin planning, and what-if analysis.

---

## 🔹 Key Columns

| Column Name              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Entry_ID                 | Unique record identifier                                                    |
| Date                     | Forecasted date for projected pricing                                       |
| Retailer                 | Retail chain where projection applies                                       |
| Brand                    | Brand being projected (national or store brand)                             |
| Product_Name             | Cereal product name                                                         |
| Size_oz                  | Package size                                                                |
| Projected_Price_USD      | Forecasted shelf price                                                      |
| CPI_Adjusted             | Boolean flag indicating if CPI adjustment was applied                      |
| Baseline_Price_USD       | Historical baseline price before projection                                |
| Promotion_Scenario       | Simulated future promo type or \"None\"                                     |
| Region                   | Region-specific context for projection modeling                            |

---

## 🔹 Row Count Logic

- **40,000 rows** representing **Retailer + Brand + Product + Date** combinations across monthly forecast intervals
- Prices projected based on weighted average increases from past price deltas, CPI trends, and retailer volatility scores
- Includes simulated promo scenarios to test discount risk and sensitivity response

---

## 🔹 Use in Power BI

- Enables **price forecasting visuals** and dynamic scenario simulation tools
- Supports executive dashboard components like **“Future Margin Risk by Brand”**
- Integrates with perceived price and sensitivity scores to model **behavioral reaction to future pricing**

---

## 🔹 Connected Business Questions

- What are the expected price points for high-volume products in the next 6–12 months?
- Which brands may experience margin compression due to inflation or promotion dependency?
- How can proactive price changes be modeled against loyalty and perceived value?

---

## 🔹 Related Tables

- `Cereal_Sales_Pricing_Dataset_Corrected`
- `Price_Sensitivity_Score_Data`
- `CPI_FoodAtHome_Data`
- `Perceived_vs_Actual_Price_Data`
