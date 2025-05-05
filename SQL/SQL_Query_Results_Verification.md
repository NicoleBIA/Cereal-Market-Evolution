# 🟩 SQL Table & Data Verification – Query Results Log

**Date:** March 31, 2025  
**Author:** Nicole Reaves  
**Project:** Cereal Market Evolution  
**Database:** `CerealSalesDB`  
**Folder:** `/SQL/`

---

This documentation verifies the **structure and data quality** of the two key tables imported into SQL Server:

- `dbo.Cereal_Sales_Pricing_Dataset`  
- `dbo.Promotions_Table`  

🟪 SQL queries were executed in SSMS and validated through visual inspection and screenshots.

---

## 🔹 1. Table Structure Verification – `sp_help`

###  Table: `Cereal_Sales_Pricing_Dataset`

```sql
EXEC sp_help 'dbo.Cereal_Sales_Pricing_Dataset';
```

### Table: 

## 🔹 1.2 Table Structure Verification – `sp_help`

```sql
EXEC sp_help 'dbo.'Promotions_Table;`
```

## 🔹 2. Top 100 Rows – **Cereal_Sales_Pricing_Dataset**

```sql
SELECT TOP 100 *  
FROM dbo.Cereal_Sales_Pricing_Dataset;
```

## 🔹 2.1 Top 100 Rows – **Promotions_Table**
```sql
SELECT TOP 100 *  
FROM dbo.Promotions_Table;
```



