# 🧠 Power BI Data Model Enhancements – Optimized Reference Guide

This reference documents all key **enhancements made to the Power BI data model** to improve performance, ensure flexibility across visuals, and support deeper analysis across pricing, sales, volume, inflation, and consumer behavior.

These enhancements enabled Nicole to build highly dynamic visuals and cross-model analytics with seamless table connectivity and precision targeting.

---

## Purpose: Why These Optimizations Matter

In a project analyzing cereal pricing, inflation, and behavioral insights, a performant and well-structured data model is essential.

Optimizing the model enables:
- Faster visual load times.
- Clean joins across multiple data sources.
- DAX-powered insight generation.
- Scalability across advanced dashboards.
- Seamless drill-throughs and filters by key dimensions.

---

## 📐 DAX Measures Created

These DAX measures were designed to power interactive visuals, compute core metrics, and support behavioral economics storytelling.

| Measure Name | Purpose |
|--------------|---------|
| **Total Sales** | Calculates price × volume (USD). |
| **Total Sales by Retailer** | Aggregated sales per retailer (used in bubble charts & tooltips). |
| **Total Sales by Brand** | Aggregated sales per brand (used in brand ranking visuals). |
| **Average Price by Brand** | Computes average product pricing by brand. |
| **Price Per Ounce by Retailer** | Unit price ($/oz) by retailer — used in anchoring bias visuals. |
| **Average Price per Ounce** | Unit pricing average across all retailers. |
| **Price Volatility** | Measures price fluctuation across time per product. |
| **Price Volatility by Product Name** | Fine-grain price variance per product. |
| **Retailer Sales Rank** | Used in Ribbon/Rank visuals to detect volatility & leaderboard shifts. |
| **Unique Retailers** | DISTINCTCOUNT measure used to validate cardinality across model. |

---

## 🧱 Supporting Tables Added

| Table Name | Description |
|------------|-------------|
| **CPI Bridge Table** | Links food-at-home CPI YoY inflation data to sales timelines. Enables macroeconomic overlays. |
| **Date Table** | Standardized date logic with relationships to `Batch_ID`, `Date`, and visual time slicing. |

---

## 🔑 Columns & Keys Engineered

| Column | Purpose |
|--------|---------|
| **Retailer_Batch_Key** | Combines Retailer + Batch_ID to serve as a primary key for seamless joins across all datasets (used in relationships & DAX). |

---

## 💡 Strategic Impact

These optimizations enabled:
- Smoother experience across 8+ datasets.
- Dynamic filtering across Retailers, Brands, Promotions, Time, and Region.
- Stronger performance with 99K+ rows in the core dataset.
- Enriched visuals tied to consumer psychology, pricing strategy, and inflation response.

> ✨ _This model architecture turned a raw pricing dataset into a fully intelligent, responsive BI system tailored for executive-level market strategy._ 🚀

---
