# 👟 Nike Global E-Commerce & Inventory Analytics

An end-to-end Data Analytics project analyzing Nike's global e-commerce feed. The project spans raw data extraction, multi-stage Python pre-processing, SQL transformations via DBeaver, and an interactive 3-page Power BI Dashboard for executive reporting and inventory control.

---

## 📌 Project Overview

This project analyzes a global Nike product dataset (**83,492 total records**) to explore pricing, availability, product mix, and market differences across various countries (US, GB, JP, IE, FI, SI, etc.). 

The analytical workflow standardizes local currencies to USD, cleans foreign product names and subcategories, and produces business insights on sales dynamics and inventory risks.

---

## 📊 Executive Summary & Key Dashboard Insights

- **Total Revenue**: **$8.11M USD** generated across global markets.
- **Top Sales Category**: **Footwear** leads revenue ($4.6M), followed by **Apparel** ($3.4M).
- **Core Market**: The **United States (US)** generates the highest revenue share.
- **Inventory Health**: **36.96%** of products are currently at **Low Stock Level**, highlighting critical inventory replenishing needs for high-demand lines.

---

## 📁 Repository Structure

```text
├── Dashboard/
│   ├── Screenshots/
│   │   ├── Sales_Overview.png
│   │   ├── Product_Deep_Dive.png
│   │   └── Inventory_Stock.png
│   └── Nike_Dashboard.pbix              # Interactive 3-Page Power BI Report
├── Python/
│   ├── 01_initial_cleaning.py           # Deduplication & unnecessary column removal
│   ├── 02_translation.py                # Foreign language text translation
│   └── 03_currency_product_cleaning.py  # Currency normalization & subcategory standardization
├── SQL/
│   └── sql.txt                          # DBeaver SQL data cleaning & validation queries
├── RAW DATA_Nike.csv                    # Original raw dataset (Tracked via Git LFS)
└── README.md
