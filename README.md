# 🚀 Indian Startup Funding — Data Analysis using Python

An in-depth exploratory data analysis of Indian startup funding data, uncovering year-wise funding trends, top cities, investment types, leading industries, and the most-funded startups like Ola, Flipkart, Paytm, and BYJU'S.

---

## 📌 Project Overview

This project analyzes Indian startup funding records to answer key business questions about where startups are thriving, which investment types dominate, which industries attract the most capital, and which startups have raised the most money and funding rounds. It involves heavy data cleaning before deriving meaningful insights.

---

## 📂 Dataset

- **Source:** [Kaggle — Indian Startup Funding Dataset](https://www.kaggle.com/datasets/sudalairajkumar/indian-startup-funding)
- **File used:** `startup_funding.csv`
- **Key columns:** `Date`, `Startup Name`, `Industry Vertical`, `City`, `Investment Type`, `Amount in USD`

---

## 🧹 Data Cleaning

- Renamed messy column names (`Date dd/mm/yyyy` → `Date`, `City  Location` → `City`)
- Fixed **3 incorrectly formatted dates** at specific row indices
- Removed commas and `+` signs from `Amount in USD` and converted to numeric
- Dropped rows with `Undisclosed` / `Unknown` funding amounts
- Imputed remaining null amounts with **column mean**
- Standardised **city names** — fixed 30+ spelling variants (e.g., `Bengaluru` → `Bangalore`, `Delhi` → `New Delhi`, `Gurgaon` variants)
- Standardised **investment types** — merged 20+ variants into 4 clean categories
- Standardised **industry names** — unified all Ecommerce spelling variants
- Standardised **startup names** — corrected Ola, Flipkart, Oyo, Paytm, BYJU'S

---

## 🔍 Analysis Breakdown

### 📅 Year-wise Funding Trends
- Extracted year from `Date` column
- Line plot of number of fundings per year
- Printed year-wise funding counts in ascending order

### 🏙️ City-wise Analysis
- Top 15 cities by number of startups
- Top 10 cities by total funding received
- Percentage share of funding for each top city
- Pie chart of top 10 cities by startup count

### 💰 Investment Type Analysis
- Standardised into 4 types: **Private Equity, Seed Funding, Debt Funding, Crowd Funding**
- Percentage of total amount funded per investment type
- Pie chart visualisation of funding share by type

### 🏭 Industry Vertical Analysis
- Top 5 industries by total funding amount
- Percentage share of funding among top 5 industries

### 🦄 Top Startups
- **Top 5 startups by total funding amount received**
- **Top 5 startups by number of funding rounds received**

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading, cleaning & aggregation |
| NumPy | Conditional value replacement (`np.where`) |
| Matplotlib | Pie charts & line plots |
| Seaborn | Line plots |
| Google Colab | Development environment |

---

## 🚀 How to Run

### Option 1 — Open in Google Colab
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

*(Replace with your actual Colab notebook link)*

### Option 2 — Run Locally
```bash
git clone https://github.com/anshu1516/Indian-Startup-Funding-Analysis.git
cd Indian-Startup-Funding-Analysis

pip install pandas numpy matplotlib seaborn

jupyter notebook Case_Study_Startup_Dataset.ipynb
```

> **Note:** Download `startup_funding.csv` from Kaggle and place it in the same directory before running.

---

## 💡 Key Insights

- 📈 Startup funding in India peaked around **2017-2018** before stabilising
- 🏙️ **Bangalore** dominates as India's startup capital by both count and funding received
- 💸 **Private Equity** accounts for the largest share of total funding amount
- 🛒 **Ecommerce** and **Consumer Internet** are the top funded industries
- 🦄 **Flipkart**, **Ola**, and **Paytm** rank among the highest funded Indian startups

---

## 👤 Author

**Anshu** — [GitHub](https://github.com/anshu1516)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
