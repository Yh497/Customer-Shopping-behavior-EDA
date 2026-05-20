# 📊 E-Commerce Customer Shopping Behavior Analysis & Insights

An end-to-end Exploratory Data Analysis (EDA) and data preprocessing pipeline analyzing 5,000 unique customer transaction profiles. This project focuses on cleaning raw transactional anomalies, transforming features for relational database (SQL) compatibility, and uncovering actionable, data-driven strategies to boost e-commerce revenue and customer retention.

---

## 🚀 Project Overview

The goal of this project is to take unrefined, messy transactional data, establish a rigorous preprocessing workflow, and translate raw numbers into high-level business intelligence. By diving deep into product categories, demographics, seasonal cycles, and rating variances, this repository uncovers hidden revenue leaks and provides an executive playbook for retail growth.

## 🛠️ Data Pipeline & Workflow

### 1. Data Cleaning & Standardization
* **Mapping Corrections:** Fixed structural column mapping inconsistencies to prevent skewed metrics.
* **Missing Value Imputation:** Addressed hundreds of missing entries for sizes and purchase amounts (e.g., using mode imputation for categorical columns like `Clothing`).
* **Feature Normalization:** Cleaned the `Review Rating` field by rounding values to 2 decimal places to eliminate long floating-point anomalies.
* **Deduplication:** Identified and eliminated 50 absolute duplicate transactions that inflated revenue metrics.
* **SQL Optimization:** Renamed columns to remove whitespaces and special characters, ensuring the dataset is fully prepared for effortless relational database schema mapping (SQL-friendly naming conventions).

### 2. Exploratory Data Analysis (EDA)
* **Univariate Analysis:** Analyzed individual metrics like product category distributions, transaction values, and customer gender splits using custom Seaborn charts and pie proportions.
* **Bivariate Analysis:** Tracked seasonal sales velocity trends, pricing distributions across main lines, and distribution outliers using boxplots and countplots.
* **Multivariate Analysis:** Uncovered complex feature interactions via 3-way `FacetGrid` breakdowns, multi-feature correlation matrices (`Pairplots`), and pivot table heatmaps matching `Season × Category`.

---

## 📈 Executive Summary: Strategic Business Recommendations

Following a deep dive into the 5,000 clean transactional profiles, five critical operational quick-wins and revenue opportunities were uncovered:

### 1️⃣ Fix the "High Revenue, Low Satisfaction" Vulnerability
* **The Insight:** Groupby aggregates show that **Bags** (averaging $\approx \$735$ per purchase) and **Headphones** (averaging $\approx \$831$ per purchase) generate the highest transaction values but hold the **lowest review ratings** in the store (Bags: $3.16/5$, Headphones: $3.07/5$), significantly below the store average of $3.66/5$.
* **The Playbook:** Immediately audit supplier quality and shipping timelines for Electronics and Bags. Customers are willing to spend premium dollars here, but quality defects or false expectations are threatening long-term retention.

### 2️⃣ Personalize Marketing for High-Spending Demographics
* **The Insight:** Gender distribution highlights a large gap in spending. While male customers spend an average of $\$130.79$, female customers spend significantly more at **$\$213.48$**, and customers identifying as "Other" average an outstanding **$\$693.80$** per transaction.
* **The Playbook:** Shift advertising spend away from generic campaigns and reallocate budget to hyper-personalized email loops, premium lookbooks, and high-tier curation tailored around these dominant-spending segments.

### 3️⃣ Restructure Pricing Tiers for Core Categories
* **The Insight:** Category boxplots for Clothing, Accessories, and Footwear reveal that the middle 50% of shoppers spend under $\$100$. However, a dense wall of outlier transactions stretches all the way to **$\$1,500$**.
* **The Playbook:** Formally split inventory structures into "Everyday Essentials" and "Premium/Luxury" tiers. Mixing $\$1,500$ outlier transactions in the same bucket as sub-$\$100$ volume skews financial forecasting models.

### 4️⃣ Optimize Seasonal Stock Matching
* **The Insight:** Pivot table heatmaps (`Season × Category`) indicate highly predictable, wave-like purchase patterns depending on the time of year.
* **The Playbook:** Synchronize supply chains with the seasonality heatmap. Bundle lower-rated or slower-moving stock (e.g., pairing a low-rated Bag with a highly-rated pair of Boots or Gloves) right before transition periods to clear warehouse space.

### 5️⃣ Upgrade Data Validation Rules
* **The Insight:** The manual data cleaning phase revealed structural data loss—such as text typos mapping Laptops into Clothing lines and missing checkout attributes.
* **The Playbook:** Upgrade the platform's front-end input fields to use structured drop-down menus rather than free-form text input. Implement automated deduplication steps directly at checkout to keep downstream business intelligence reliable.

---

## 💻 Tech Stack & Environment

* **Language:** Python 3.x
* **Libraries Used:** * `pandas` - For structured data frame manipulation and cleaning
  * `numpy` - For mathematical and vectorized operations
  * `matplotlib` - For foundational visualization elements
  * `seaborn` - For advanced statistical plots, heatmaps, and FacetGrids

---

## 🏃‍♂️ How to Run

1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
