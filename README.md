# 👟 NIKE GLOBAL ANALYTICS

### *End-to-End Analytics Pipeline: From Raw Telemetry to Executive Intelligence*

---

## 1. Executive Summary & Key Highlights

This project engineers an end-to-end data pipeline over a global dataset of **83,492 Nike ecommerce records** across key international markets (US, GB, JP, IE, FI, SI). 

By integrating multi-stage **Python** automation, robust **DBeaver SQL** cleaning, and high-impact **Power BI** visual modeling, this solution transforms raw, unstandardized retail telemetry into actionable operational insights for revenue optimization and supply chain control.

### 🔑 Key Decision-Making Highlights
* **Revenue Drivers**: Footwear dominates with **$4.6M** in sales, outperforming Apparel ($3.4M) and Equipment combined.
* **Geographic Expansion**: The United States (US) leads global revenue share, followed by Western European hubs.
* **Supply Chain Bottleneck**: **36.96% (~37%)** of active catalog sits at critical `LOW` stock thresholds, requiring immediate replenishment triggers to avoid stockouts.

---

## 2. Project Overview

This project analyzes a global Nike product feed to explore pricing, availability, product mix, and market differences across countries. The workflow moves from raw CSV through Python and SQL cleaning to interactive Power BI dashboards.

### Key Objectives
* Compare product prices and discounts across international markets (US, GB, JP, etc.).
* Analyze availability and stock signals by market and category.
* Explore product mix (Footwear, Apparel, Equipment) and sub-brands (*Nike, Jordan, Converse, Kobe, ACG*).
* Normalize multi-currency records to a unified USD baseline for accurate comparison.

---

## 3. Project Structure

| Folder / File | Description |
| :--- | :--- |
| **`RAW DATA_Nike.csv`** | Original dataset snapshot (83,492 records across global markets). |
| **`Python/`** | Contains automated ETL scripts (`01_initial_cleaning.py`, `02_translation.py`, `03_currency_product_cleaning.py`). |
| **`SQL/`** | Contains `sql.txt` with DBeaver validation queries and data logic constraints. |
| **`Dashboard/`** | Holds the interactive Power BI report (`Nike_Dashboard.pbix`) and high-res screenshots. |

---

## 4. Data Dictionary

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `snapshot_date` | Date | Snapshot date for the record |
| `country_code` | Text | Two-letter country code (e.g., US, GB, JP, IE, FI, SI) |
| `product_name` | Text | Standardized/translated product title |
| `model_number` | Text | Internal model identifier |
| `currency` | Text | Local currency code (USD, EUR, JPY, GBP) |
| `price_local` | Decimal | Local price value |
| `sale_usd` | Decimal | Converted standardized USD price |
| `discount_pct` | Decimal | Discount percentage applied |
| `category` | Text | High-level category (`FOOTWEAR`, `APPAREL`, `EQUIPMENT`) |
| `clean_subcategory` | Text | Standardized subcategory classification |
| `product_id` | Text | Unique Product UUID |
| `sku` | Text | Stock Keeping Unit identifier |
| `brand_name` | Text | Brand classification (*Nike, Jordan, Converse, Kobe, ACG*) |
| `gender_clean` | Text | Normalized demographic category (`Men`, `Women`, `Kids`, `Unisex`) |
| `availability_level` | Text | Stock availability status (`HIGH`, `MEDIUM`, `LOW`, `OOS`) |
| `in_stock` | Boolean | Inventory presence flag (`True`/`False`) |
| `sport_tags` | Text | Sport classification (Running, Basketball, Soccer, etc.) |

---

## 5. Data Summary & Key Metrics

* **Total Analyzed Records**: 83,492 rows
* **Total Analyzed SKUs**: 17,890 unique products
* **Total Revenue**: **$8.11M USD**
* **Total Discounts Given**: **$348.58K USD**
* **Stock Warning Ratio**: **36.96% Low Stock**
* **Observed Markets**: US, GB, JP, IE, FI, SI

---

## 6. Cleaning & Data Quality Notes (Challenges Handled)

* **Multi-Currency Normalization**: Converted local currencies (EUR, GBP, JPY) to a unified USD value using standard exchange rates.
* **Foreign Language Translation**: Processed Japanese and French product names/tags using Python NLP translation routines.
* **Demographic Standardization**: Cleaned overlapping gender fields (`Men`, `Men's Lifestyle`, `Unisex`) into `gender_clean`.
* **Subcategory Mapping**: Re-mapped non-standardized subcategory text into structured `clean_subcategory` tiers.
* **Deduplication**: Handled duplicate snapshots using `product_id` and `sku` constraints in SQL.

---

## 7. Business Questions & Insights To Explore

1. **Discount Elasticity**: Does a higher `discount_pct` increase sell-through rate, or are premium lines (like *Jordan*) discount-resistant?
2. **Regional Price Variance**: What is the price delta for identical `product_id` items across US vs. European vs. Asian markets?
3. **Stockout Risk Mapping**: Which subcategories have the highest proportion of `LOW` and `OOS` items?
4. **Brand Portfolio Split**: How does inventory distribution compare between core *Nike* lines and sub-brands (*Converse*, *ACG*, *Kobe*)?

