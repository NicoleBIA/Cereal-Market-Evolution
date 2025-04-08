### 🧱 Data Architecture – Cereal Market Evolution Project

This document captures all key elements, strategies, and simulated design considerations behind the Cereal Market Evolution dataset created by Nicole Reaves BIA.

---

#### 🔹 Purpose of Dataset Design
To simulate a real-world consumer packaged goods (CPG) retail environment by designing a structured, AI-enhanced, multi-table dataset that could:
- Reflect actual market conditions
- Support pricing and promotional analysis
- Track brand loyalty and consumer behavior
- Quantify inflationary effects using CPI data
- Enable business intelligence reporting in Power BI and SQL

---

#### 🔹 Dataset Strategy Overview
Nicole led the end-to-end creation of a synthetic but business-aligned dataset, grounded in:
- **Retailer dynamics** (Walmart, Kroger, Costco, Sam’s Club, Target, Amazon Fresh)
- **Brand structure** (national brands vs. private labels)
- **Promotion types** (BOGO, 10% Off, Clearance, No Promotion)
- **Inflation simulation** via integration with **Year-over-Year CPI data** for food-at-home
- **Shrinkflation awareness**, reflected in package size and price-per-ounce comparisons
- **Behavioral economics models** for perceived value, price sensitivity, and loyalty behavior

---

#### 🔹 Primary Tables in Data Model
1. **Cereal_Sales_Pricing_Dataset_Corrected**  
   - Core dataset with: Retailer, Brand, Product, Size, Price, Promotion, Units Sold, Date
2. **Loyalty_Brand_Switching_Data**  
   - Captures prior purchases, switch frequency, and loyalty segmentation
3. **Perceived_vs_Actual_Price_Data**  
   - Compares expected price vs. real price to analyze psychological pricing
4. **Price_Sensitivity_Score_Data**  
   - Assigns scores per product/retailer to quantify elasticity and deal sensitivity
5. **AI_Driven_Price_Projection_Data**  
   - Forecasts future pricing scenarios using historical CPI and pricing trends
6. **CPI_FoodAtHome_Data**  
   - Quarterly YoY inflation data for context and comparative analysis

---

#### 🔹 Structural Design Elements
- **Entry_ID and Batch_ID** for each record to allow grouping, filtering, and versioning
- **Retailer_Batch_Key** as primary key across related tables
- Companion tables connected via **one-to-many relationships**
- Referential integrity enforced in Power BI’s data model view
- Prepared for **relational modeling** and **DAX-based transformation logic**

---

#### 🔹 Business Questions Simulated
- How do promotions and price perception affect consumer loyalty and switching?
- Which retailers offer price stability vs. volatility?
- Do private labels gain share during inflation spikes?
- How does shrinkflation impact consumer trust and brand perception?
- What are the most effective strategies for margin protection?

---

#### 🔹 AI Integration & Enhancement
- Used ChatGPT to simulate behavioral indicators and generate realistic data patterns
- Designed price forecasts based on trend logic and external CPI factors
- Developed AI-enhanced models to project future price trends while accounting for packaging size, inflation, and promotion type
- Integrated perceived vs. actual pricing gaps to evaluate their influence on consumer trust, urgency, and price sensitivity in real-time purchase decisions
- Ensured the dataset allowed for scenario testing, key influencer analysis, and behavioral response modeling to support strategic forecasting in Power BI

  ---
### 🔹 Outlier Treatment & Data Integrity Notes

   While the dataset maintains realistic variability to reflect real-world price behavior, select outlier points—especially in price 
   perception—were intentionally preserved to support behavioral edge case analysis.

**Key examples include:**

- **General Mills Cinnamon Toast Crunch** at Costco (BOGO promotion): Aggregate size of 99oz priced at $2.53, later confirmed to be 
    part of a dual-pack promo (49.5oz x 2), skewing unit perception.
- **Kellogg’s Frosted Flakes** at Costco: Outlier BOGO point at $9.76 for 61.9oz, sharply deviating from surrounding trend.

- These entries were retained for visual and regression contrast analysis, but users are encouraged to apply context-aware filters 
  when running sensitivity models or exploring perception gaps.

- This decision was guided by the project’s emphasis on behavioral pricing analytics and scenario realism.

