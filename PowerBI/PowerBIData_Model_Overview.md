# 📊 Power BI Data Model Overview  

## 🟦 Establishing a Strong Data Foundation  
The **Cereal Market Evolution: Pricing, Inflation & AI-Driven Consumer Insights** project leverages a structured **Power BI Data Model** to ensure **seamless relationships, accurate calculations, and scalable business intelligence insights.**  

The model is anchored by **Retailer_Batch_Key**, a unique key that **connects all datasets** and facilitates cross-analysis across pricing, brand-switching, price sensitivity, and market trends.

---

## Power BI Data Model
![Cereal Sales Performance Data Model](/Images/Cereal_Market_Evolution_DataModel.png)

## 🔑 Retailer_Batch_Key: The Core Relational Key  

### 🟢 Purpose of Retailer_Batch_Key  
- Serves as the **primary key** across all datasets.  
- Enables **one-to-many relationships** between the **master pricing dataset** and **supplementary datasets**.  
- Supports **efficient querying & accurate cross-referencing** in Power BI.  

### 🟢 Datasets Connected via Retailer_Batch_Key  
- **Cereal Sales & Pricing Dataset** → Master dataset  
- **Loyalty & Brand Switching Data** → Tracks brand-switching behavior  
- **Perceived Price vs. Actual Price Data** → Analyzes price perception accuracy  
- **Price Sensitivity Score Data** → Measures consumer pricing elasticity  
- **AI-Driven Price Projection Data** → Forecasts future price trends  
- **CPI Inflation Data (QoQ & YoY)** → Aligns pricing with macroeconomic trends  

These structured relationships enable **powerful insights into consumer behavior, retailer pricing strategy, and inflation impact.**  

---

## **DAX Queries Reference: Key Measures & Calculations**  

# 📊 DAX Queries Reference: Key Measures & Calculations  
**Cereal Sales Performance: Inflation, Pricing, and Consumer Loyalty Insights (CSPIPCLI)**  
This page outlines the DAX measures developed for this simulation and how each contributes to the broader strategy of market segmentation, pricing analysis, behavioral modeling, and inflation-adjusted forecasting.

---

## 🔷 1. Total Sales Measures

### ✅ `Total_Sales`  
**Description:** Calculates total sales revenue based on unit price and quantity sold.  
**DAX Code:**  
```dax
Total_Sales = SUM(Cereal_Sales_Pricing_Dataset_Corrected[Price_USD] * Cereal_Sales_Pricing_Dataset_Corrected[Units_Sold])
```
**Use Case:**  
- Used in all sales-based visuals: Total Sales by Brand, Retailer, and Region.  
- Foundational for comparing performance across categories, time, and promotional periods.  
- Enables high-level forecasting, CAGR, and YoY growth modeling.

---

### ✅ `Total_Sales_by_Brand`  
**Use Case:**  
- Evaluates brand market share and pricing performance.  
- Used in stacked bar charts and brand-specific time series.  
- Anchors analysis of price-to-performance and promotional dependency.

---

### ✅ `Total_Sales_by_Retailer`  
**Use Case:**  
- Compares total retailer performance over time.  
- Used in retailer ranking visuals, loyalty segmentation, and margin contribution comparisons.

---

### ✅ `Total_Sales_by_Region_and_Brand`  
**Use Case:**  
- Enables geographic segmentation modeling.  
- Supports brand performance insights by distribution region.  
- Used in slicer-based cross-regional comparisons and elasticity visuals.

---

### ✅ `Quaker_Oats_Total_Sales`  
**Use Case:**  
- Isolates Quaker Oats' portfolio performance for strategic loyalty deep dives.  
- Featured in pie charts and loyalty-pressure visuals.  
- Supports consumer behavior segmentation.

---

### ✅ `MaltOMeal_Total_Sales`  
**Use Case:**  
- Analyzes MOM’s volume-driven strength in value segments.  
- Paired with loyalty scores to assess brand stickiness.  
- Used in intra-brand segmentation visuals.

---

### ✅ `MaltOMeal_Sales_Percent`  
**Use Case:**  
- Measures MOM’s share of total sales by brand.  
- Supports intrabrand positioning and cost-conscious buyer analysis.  
- Key for identifying substitution effects and strategic loyalty pivots.

---

### ✅ `Total_Sales_Loyalty`  
**Use Case:**  
- Compares loyalty-generated sales to total sales volume.  
- Helps detect performance pressure or upside from repeat buyers.  
- Used in loyalty breakdown visuals and strategy implications.

---

## 🔷 2. Price and Elasticity Measures

### ✅ `Average_Price_by_Brand`  
**Use Case:**  
- Core input for inflation trend modeling and price variance by portfolio.  
- Used in perceived pricing and shrinkflation analysis.  
- Supports elasticity insights when paired with volume.

---

### ✅ `Average_Price_by_Retailer`  
**Use Case:**  
- Retailer benchmark analysis for strategic pricing.  
- Enables regional forecasting, margin comparisons, and positioning insights.  
- Used in comparative column charts and scatter plots.

---

### ✅ `Average_Price_Per_Ounce_by_Retailer`  
**Use Case:**  
- Standardizes pricing for cross-retailer comparison.  
- Supports shrinkflation analysis and value communication modeling.  
- Used in bar/line visuals with conditional formatting and insight annotations.

---

### ✅ `Price_Per_Ounce`  
**DAX Code:**  
```dax
Price_Per_Ounce = DIVIDE([Price_USD], [Package_Size_Oz])
```
**Use Case:**  
- Adjusts for product size changes over time.  
- Tracks unit cost increases masked by shelf price stability.  
- Central to shrinkflation and fairness pricing analysis.

---

### ✅ `Actual_Price_Per_Ounce`  
**Use Case:**  
- Used to map true unit costs in scatter plots.  
- Paired with perceived price for behavioral gap analysis.  
- Inputs into pricing strategy and value perception models.

---

### ✅ `Perceived_Price_Per_Ounce`  
**Use Case:**  
- Captures consumer expectation or interpreted value.  
- Used in anchoring bias, price psychology, and BOGO/no-promo behavior modeling.  
- Featured in dual-axis and trend deviation visualizations.

---

### ✅ `Price_Volatility`  
**Use Case:**  
- Measures variance in pricing over time by brand or retailer.  
- Supports elasticity curves and risk forecasting.  
- Used in box plots or slicer-enabled comparative charts.

---

### ✅ `Price_Volatility_by_Product`  
**Use Case:**  
- Highlights inconsistencies at the product level.  
- Supports SKU rationalization, promo risk, and consumer confidence strategy.  
- Used in diagnostic visuals to assess promotional effectiveness.

---

## 🔷 3. Segmentation, Loyalty & Ranking Measures

### ✅ `Loyalty_Status`  
**Use Case:**  
- Classifies customers as Repeat or Switch based on purchase history.  
- Used to calculate switch frequency and segment loyalty value.  
- Critical for intrabrand behavior modeling and churn indicators.

---

### ✅ `Retailer_Sales_Rank`  
**Use Case:**  
- Ranks retailer performance by total sales.  
- Enables retail segmentation and market share forecasting.  
- Used in ribbon charts and leaderboard visuals.

---

## 🧠 Analytical Themes Enabled

These DAX measures collectively power the following strategic frameworks:

| Theme                          | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| **Segmentation Modeling**     | Regional, brand, and consumer segmentation based on price, loyalty, and sales. |
| **Forecasting & Trend Models**| YoY sales trends, retailer volume forecasting, and pricing response curves.  |
| **Shrinkflation Diagnostics** | Analysis of package size, price per ounce, and margin masking.              |
| **Elasticity & Behavior**     | Analysis of price sensitivity, loyalty stickiness, and consumer urgency.     |
| **Perception vs. Reality**    | Comparison of expected vs. actual pricing through scatter plots and DAX pairs.|

---

### 1️⃣ Total Sales Calculation  
This measure calculates **total revenue**, multiplying unit price by sales volume.

#### **DAX Code:**
```DAX
Total_Sales = SUM(Cereal_Sales_Pricing_Dataset_Corrected[Price_USD] * Cereal_Sales_Pricing_Dataset_Corrected[Sales_Volume_Units])
```

## Use Case and Purpose
- Tracks total revenue by retailer, brand, and region.
- Used in Total Sales by Brand visualization to compare brand market share.
- Supports revenue trend analysis for inflation-adjusted pricing models

### 2️⃣ Unique Retailers Measure
This measure counts the number of **distinct retailers** in the dataset.

#### **DAX Code:**
```DAX
Unique_Retailers = DISTINCTCOUNT(Cereal_Sales_Pricing_Dataset_Corrected[Retailer])
```

## Use Case and Purpose
- Ensures **all retailers** are properly accounted for.
- Supports retailer-specific analysis & segmentation.
- Helps **validate data integrity** by ensuring no duplicate retailer entries.
- Used in dashboards to analyze Retailer Product Offerings & Exclusivity trends.

### Why These Measures are **Critical** ?
- ✅ Total Sales Calculation → Provides key revenue insights for pricing impact analysis.
- ✅ Unique Retailers Measure → Validates data integrity and helps analyze retailer exclusivity strategies.
- ✅ Retailer_Batch_Key → Ensures efficient data structuring and enhances model performance.

-----

> These DAX queries form the analytical backbone of the CSPIPCLI project, ensuring high-integrity insights across inflation trends, retail behavior, and strategic pricing impact.

