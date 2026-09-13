# Indian E-Commerce Retail Analytics

## Executive Summary

This project presents an end-to-end **Indian E-Commerce Retail Analytics** solution developed as part of an MBA assessment in **Data Automation and Advanced Spreadsheet Modelling**.

The objective was to transform a raw and inconsistent e-commerce transaction dataset into a structured analytical model and an interactive **Power BI business intelligence dashboard**.

The project demonstrates the complete analytics workflow:

**Raw Data → Data Cleaning → Data Transformation → Data Modelling → DAX → Interactive Dashboard → Business Insights → Lean Recommendation**

---

## Business Context

The organisation operates as a pan-India office-supplies and technology retailer with transactions generated from multiple regional order systems.

The source dataset contained approximately **9,994 order line-items across 28 columns** and included several data-quality issues, including inconsistent category labels, non-standard date formats and text-based profit values.

The purpose of the analysis was to provide management with a reliable view of:

- Revenue performance
- Profitability
- Customer segments
- Product categories
- Regional and state performance
- Delivery performance
- Geographical distribution

---

## Project Objectives

The key objectives of this project were to:

1. Clean and standardise the raw transaction data using Power Query.
2. Separate transactional and geographical information into appropriate analytical tables.
3. Develop a structured data model.
4. Create business-focused DAX measures.
5. Analyse sales, profit, margin and discount performance.
6. Identify patterns across categories, regions, states and customer segments.
7. Build an interactive Power BI dashboard for decision-making.
8. Develop a Lean/business improvement recommendation based on the analysis.

---

# Data Preparation & Transformation

## Power Query

Power Query was used as the primary data preparation layer.

### Profit Transformation

The original `Profit` column contained:

- Currency symbols
- Positive numeric values
- Loss values represented using the text prefix `loss`

The transformation process:

```text
Remove Currency Symbol
        ↓
Identify "loss" values
        ↓
Convert loss values to negative numbers
        ↓
Convert column to Decimal Number
