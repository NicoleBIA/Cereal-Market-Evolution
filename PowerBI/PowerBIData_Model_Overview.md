# 📊 Power BI Data Model Overview  

## 🔑 Establishing a Strong Data Foundation  
The **Cereal Market Evolution: Pricing, Inflation & AI-Driven Consumer Insights** project leverages a structured **Power BI Data Model** to ensure **seamless relationships, accurate calculations, and scalable business intelligence insights.**  

The model is anchored by **Retailer_Batch_Key**, a unique key that **connects all datasets** and facilitates cross-analysis across pricing, brand-switching, price sensitivity, and market trends.

---

## 🔑 Retailer_Batch_Key: The Core Relational Key  

### ✅ Purpose of Retailer_Batch_Key  
- Serves as the **primary key** across all datasets.  
- Enables **one-to-many relationships** between the **master pricing dataset** and **supplementary datasets**.  
- Supports **efficient querying & accurate cross-referencing** in Power BI.  

### ✅ Datasets Connected via Retailer_Batch_Key  
- **Cereal Sales & Pricing Dataset** → Master dataset  
- **Loyalty & Brand Switching Data** → Tracks brand-switching behavior  
- **Perceived Price vs. Actual Price Data** → Analyzes price perception accuracy  
- **Price Sensitivity Score Data** → Measures consumer pricing elasticity  
- **AI-Driven Price Projection Data** → Forecasts future price trends  
- **CPI Inflation Data (QoQ & YoY)** → Aligns pricing with macroeconomic trends  

These structured relationships enable **powerful insights into consumer behavior, retailer pricing strategy, and inflation impact.**  

---

## **DAX Queries Reference: Key Measures & Calculations**  

### 1️⃣ Total Sales Calculation  
This measure calculates **total revenue**, multiplying unit price by sales volume.

#### **DAX Code:**
```DAX
Total_Sales = SUM(Cereal_Sales_Pricing_Dataset_Corrected[Price_USD] * Cereal_Sales_Pricing_Dataset_Corrected[Sales_Volume_Units])

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

## How its Used 
- Ensures **all retailers** are properly accounted for.
- Supports retailer-specific analysis & segmentation.
- Helps **validate data integrity** by ensuring no duplicate retailer entries.
- Used in dashboards to analyze Retailer Product Offerings & Exclusivity trends.

### Why These Measures are **Critical** ?
- ✅ Total Sales Calculation → Provides key revenue insights for pricing impact analysis.
- ✅ Unique Retailers Measure → Validates data integrity and helps analyze retailer exclusivity strategies.
- ✅ Retailer_Batch_Key → Ensures efficient data structuring and enhances model performance.

