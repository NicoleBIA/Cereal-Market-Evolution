# Data Architecture Summary Index

This index provides a high-level overview of all supporting dataset documentation files in the `/Data_Architecture/` folder of the Cereal Market Evolution project. Each file outlines the structure, purpose, row count, business value, and Power BI integration for one of the core or companion datasets.

Use this index to quickly understand the purpose of each dataset and how they work together to simulate a real-world CPG analytics environment.

---

## 🧱 Primary Files & Descriptions

1. [Cereal_Sales_Pricing_Dataset_Corrected.md](Cereal_Sales_Pricing_Dataset_Corrected.md)  
   Core sales dataset with pricing, promotion, retailer, and volume data  
   Foundation for most visuals and KPIs in Power BI

2. [Loyalty_Brand_Switching_Data.md](Loyalty_Brand_Switching_Data.md)  
   Simulates brand loyalty, prior purchases, and switching frequency  
   Powers loyalty-based segment analysis and switching strategy visuals

3. [Perceived_vs_Actual_Price_Data.md](Perceived_vs_Actual_Price_Data.md)  
   Compares expected vs. actual pricing  
   Used to model anchoring bias, trust, and value perception

4. [Price_Sensitivity_Score_Data.md](Price_Sensitivity_Score_Data.md)  
   Scores consumer sensitivity to price changes per product and retailer  
   Drives elasticity mapping and promotion risk strategy

5. [AI_Driven_Price_Projection_Data.md](AI_Driven_Price_Projection_Data.md)  
   Simulates future prices based on past trends and CPI forecasts  
   Supports scenario analysis, margin forecasting, and strategic planning

6. [CPI_FoodAtHome_Data.md](CPI_FoodAtHome_Data.md)  
   Simulated CPI data for Food-at-Home category (2019–2024)  
   Provides macroeconomic context for pricing decisions

---

## How to Use This Folder

- Start with the [README_Data_Architecture.md](README.md) to understand the **strategic design approach**
- Use this Summary Index to navigate each dataset’s **structure and business logic**
- Combine insights across multiple datasets for cross-table analysis in Power BI or SQL

---

📁 This documentation reflects the architectural thinking behind dataset simulation, forecasting, behavioral modeling, and business alignment in the Cereal Market Evolution project.


