# RBAC 2025 - Round 02: Colgate-Palmolive Case Study 🦷

**Theme:** Enhancing Toothbrush Manufacturing Throughput: A Focus on Downtime and Quality Control.

This repository contains the analysis and solution for **Round 2 of the RMIT Business Analytics Champion 2025 (RBAC)** competition. In this case study, our team acts as Business Analysts reporting to the Head of Department at **Colgate-Palmolive**, aiming to optimize operational efficiency in their primary toothbrush manufacturing facility.

## 📋 Project Overview

Colgate-Palmolive is facing financial losses due to significant machine downtime and product defects. The management requires a data-driven analysis to pinpoint critical bottlenecks, identify root causes of inefficiencies, and quantify their impact on production potential.

**Objective:**
To interpret one year of production and machine data to provide evidence-based recommendations that improve machine uptime, reduce waste, and enhance product quality.

## ❓ Business Questions

The project addresses four key business requirements:

1.  **Performance Overview:** Develop a comprehensive dashboard tracking key metrics such as Overall Equipment Effectiveness (OEE), Defect Rate, and Production Throughput Yield.
2.  **Root Cause Analysis:** Identify primary drivers of downtime and defects (specific machines, shifts, or product types) and categorize them into systemic vs. emerging issues.
3.  **Impact Quantification:** Calculate potential production units lost due to downtime and material loss from defective units, including indirect impacts like customer satisfaction.
4.  **Strategic Recommendations:** Propose three actionable, data-driven strategies to mitigate inefficiencies and increase throughput.

## 📂 Dataset Description

The analysis is based on three provided datasets covering hypothetical production figures:

### 1. `production_log.csv` (Daily Operational Data)
Contains daily records of production runs, shifts, and line performance.
* **Key Columns:** `DOWNTIME`, `RUN_TIME`, `GOOD_PRODUCTION_QTY`, `REJECT_PRODUCTION_QTY`, `UTIL_REASON_DESCRIPTION` (Reason for downtime).
* **Metrics:** Used to calculate OEE components (Availability, Performance, Quality).

### 2. `maintenace_order.csv` (Maintenance Records)
Contains static data regarding maintenance orders for specific equipment.
* **Key Columns:** `ORDER_TYPE`, `DESCRIPTION`, `BASIC_START_DATE`, `EQUIPMENT_ID`.
* **Purpose:** To analyze the relationship between maintenance schedules and unplanned downtime.

### 3. `cross_reference.csv` (Mapping Table)
A bridge table linking physical equipment to operational production lines.
* **Key Columns:** `EQUIPMENT_ID`, `LINE_NAME`.

*> **Note:** All data used in this project is hypothetical and does not represent real business figures for Colgate-Palmolive. For datasets, please contact with the owner of this repository.*

## 🛠️ Methodology & Analytical Approach

Our team adopted a rigorous statistical approach to move beyond surface-level observations:

### 1. Data Processing & Feature Engineering
* **Data Cleaning:** Handled missing values and standardized categorical variables (e.g., Shift names, Line names).
* **EDA:** Conducted Exploratory Data Analysis (EDA) to find initial trends in downtime seasonality and defect distribution.
* **OEE Modeling:** Engineered comprehensive features for Availability, Performance, and Quality 
* **Category Clustering:** Regrouped fragmented downtime descriptions (e.g., specific jam types) into higher-level operational clusters 

### 2. Statistical Hypothesis Testing
To isolate true root causes, we applied statistical tests instead of relying solely on visual trends

### 3. Root Cause Analysis
* Identified the "Vital Few" reasons contributing to the majority of downtime (e.g., Mechanical Failure vs. Material Shortage).
* We drilled down into "Unplanned Downtime" (accounting for ~15% of losses) for material handling error, error-product frequency investigation
  
### 4. Strategic Recommendations
Formulated three pillars of improvement focused on:
1.  Predictive Maintenance optimization.
2.  Workforce training based on Crew performance gaps.
3.  Process standardization for high-defect product types.

*> **Note:** A descriptions of notebooks' purposes will also be included*

## 📊 Deliverables

* **Executive Report:** A 15-slide presentation summarizing key insights and strategic roadmaps.
* **Source Code:** Jupyter Notebooks / R Scripts documenting the analysis process.
* **Dashboard:** Interactive visualizations of factory performance.

## 📁 Repository Structure

```text
├── Datasets/                   # Raw and clean CSV files
├── Notebooks/              # Jupyter notebooks for EDA and Modeling
├── THE TORTURED ANALYST DEPARTMENT_Round 2_RBAC 2025.pdf           # Final PDF Report and Slides
└── README.md               # Project documentation
