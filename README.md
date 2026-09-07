# Hotel Booking Analysis

![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28%2B-FF4B4B?logo=streamlit&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Server-CC2927?logo=microsoftsqlserver&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A SQL + Python case study analyzing hotel booking cancellations, revenue impact, and demand patterns, with an interactive Streamlit dashboard for exploring the results.

**Live app:** https://hotel-booking-demand-analysis-bsaeu4bj3op7ut6osyglup.streamlit.app/
**Author:** [Samrat Koushik](https://github.com/samratkoushik)

---

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Business Recommendations](#business-recommendations)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Tech Stack](#tech-stack)
- [License](#license)

---

## Overview

This project analyzes hotel booking data to surface patterns in customer behavior, cancellation trends, and revenue optimization opportunities. SQL handles data cleaning and metric calculation; Streamlit powers an interactive dashboard that turns the analysis into actionable insights for hotel management.

## Problem Statement

Hotels lose meaningful revenue to booking cancellations. This analysis answers:

- What factors drive cancellation behavior
- How to optimize pricing and booking policies
- Which customer segments are most valuable
- What seasonal patterns affect demand

## Dataset

| | |
|---|---|
| **Source** | Hotel booking records |
| **Size** | 119,391 bookings |
| **Timeframe** | 2015 – 2017 |
| **Scope** | City and Resort hotels across 178 countries |
| **Key fields** | Booking details, customer demographics, cancellation status, pricing |

## Methodology

### 1. Data Processing (SQL)
- Data cleaning and validation
- Feature engineering (lead time categories, seasons, revenue calculations)
- Business metrics calculation
- Export queries for dashboard consumption

### 2. Analysis & Visualization (Streamlit)
- Interactive dashboard with hotel type, year, and country filters
- KPI monitoring (cancellation rate, revenue, booking trends)
- Geographic and temporal analysis
- Customer segment performance
- Live app: https://hotel-booking-demand-analysis-bsaeu4bj3op7ut6osyglup.streamlit.app/

## Key Findings

### Critical Insights
- 37% overall cancellation rate — a significant revenue risk
- Resort hotels outperform city hotels (28% vs. 42% cancellation rate)
- Lead time strongly predicts cancellations — bookings made far in advance are more likely to cancel
- Direct bookings have the lowest cancellation rates but only 12% of total volume

### Revenue Impact

| Metric | Value |
|---|---|
| Total bookings | 119,391 |
| Revenue generated | $15.1M |
| Revenue lost to cancellations | $5.6M |
| Recovery potential (10% cancellation reduction) | +$1.5M |

## Business Recommendations

1. Implement dynamic pricing based on lead time to reduce long-lead-time cancellations
2. Incentivize direct bookings through loyalty programs and exclusive offers
3. Develop retention strategies for high-risk booking segments
4. Optimize overbooking policies using predictive cancellation models

## Project Structure

```
hotel-booking-demand-analysis/
├── app.py                                          # Streamlit dashboard
├── requirements.txt                                # Python dependencies
├── data/
│   └── hotel_bookings.csv                          # Raw dataset
├── sql/
│   ├── 01_data_loading_and_setup.sql               # Database & table setup
│   ├── 02_data_cleaning_and_calculated_columns.sql # Data preprocessing
│   ├── 03_business_metrics_and_kpis.sql            # Core analysis queries
│   └── 04_dashboard_data_export_queries.sql        # Export queries
├── LICENSE
└── README.md
```

## Getting Started

```bash
# Clone the repository
git clone https://github.com/samratkoushik/hotel-booking-demand-analysis.git
cd hotel-booking-demand-analysis

# Install dependencies
pip install -r requirements.txt

# Launch the dashboard
streamlit run app.py
```

The SQL scripts in `sql/` are written for SQL Server and can be run in order (01 → 04) against a local instance to reproduce the underlying analysis.

## Tech Stack

| Layer | Tools |
|---|---|
| Data processing | SQL Server (T-SQL) |
| Analysis | Python, pandas, NumPy |
| Visualization | Plotly |
| Dashboard | Streamlit |
| Version control | Git, GitHub |

## Results & Impact

This analysis framework enables hotels to:
- Monitor booking performance through a self-service dashboard
- Identify high-risk reservations before cancellation
- Optimize pricing strategies based on demand patterns
- Improve customer retention through targeted interventions

## License

Distributed under the [MIT License](LICENSE).
