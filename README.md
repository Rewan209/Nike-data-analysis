<div align="center">

# 👟 NIKE GLOBAL ANALYTICS
### *End-to-End Analytics Pipeline: From Raw Telemetry to Executive Intelligence*

![Nike Header](https://img.shields.io/badge/Brand-Nike_Inc.-black?style=for-the-badge&logo=nike)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Tech-Python_%7C_SQL_%7C_Power_BI-blue?style=for-the-badge)

---

</div>

## 📌 Executive Summary

This project engineers an **end-to-end data pipeline** over a global dataset of **83,492 Nike ecommerce records** across key international markets (US, GB, JP, IE, FI, SI). 

By integrating multi-stage **Python** automation, robust **DBeaver SQL** cleaning, and high-impact **Power BI** visual modeling, this solution transforms raw, unstandardized retail telemetry into actionable operational insights for revenue optimization and supply chain control.

---

## ⚡ Business Impact at a Glance

<div align="center">

| 💵 Total Revenue | 🏷️ Total Discounts | 👟 Analyzed SKUs | ⚠️ Stock Warning |
| :---: | :---: | :---: | :---: |
| **$8.11M USD** | **$348.58K USD** | **17.89K Products** | **36.96% Low Stock** |

</div>

### 🎯 Key Decision-Making Highlights
* **Footwear Dominance**: Generates **$4.6M** in sales, outperforming Apparel ($3.4M) and Equipment combined.
* **Geographic Driver**: The **United States (US)** leads global market revenue share, followed by Western European hubs.
* **Supply Chain Bottleneck**: **~37% of active catalog** sits at critical `LOW` stock thresholds, requiring immediate replenishment triggers to avoid stockouts.

---

## 🛠️ Data Pipeline & Architecture

The repository is structured to reflect a clean separation of concerns across the data lifecycle:

```text
 ┌────────────────┐     ┌──────────────────────┐     ┌─────────────────┐     ┌───────────────────┐
 │  RAW DATASET   │ ──> │ Python Transformation│ ──> │ SQL Validation  │ ──> │ Interactive BI    │
 │  (83k+ Rows)   │     │ (Clean, Translate)   │     │ (DBeaver Script)│     │ (Power BI Engine) │
 └────────────────┘     └──────────────────────┘     └─────────────────┘     └───────────────────┘
