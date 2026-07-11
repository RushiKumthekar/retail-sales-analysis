# Retail Sales & Distribution Analysis

A comprehensive data analytics project featuring exploratory data analysis (EDA), data cleaning, and an interactive business intelligence dashboard to evaluate warehouse performance, retail sales behavior, and supplier distributions between 2017 and 2020.

---

## 📌 Project Overview

This project uncovers sales trends, inventory movement, and retail metrics for a large-scale distributor. Utilizing Python for data manipulation and Power BI for executive reporting, it offers data-backed answers to core product performances, distribution challenges, and supplier analysis.

### Core Goals:

* **Data Standardization:** Clean and format large-scale operational records containing transactional inconsistencies.
* **Trend Spotting:** Analyze performance variations across multiple item types (Wine, Liquor, Beer, Kegs, etc.).
* **Strategic Visualization:** Build a dynamic Power BI report to track **Retail Sales**, **Warehouse Sales**, and **Retail Transfers**.

---

## 📂 Repository Structure

```text
├── dataEDA.ipynb          # Jupyter Notebook containing Data Cleaning & EDA
├── retailAnalysis.pbix    # Interactive Power BI Dashboard file
└── README.md              # Project documentation

```

---

## 📊 Dataset Specifications

The analysis is built around the **Warehouse and Retail Sales** tracking system, containing **307,645 rows** across 9 key features:

| Column Name | Data Type | Description |
| --- | --- | --- |
| **YEAR** | `int64` | Transaction year (2017 - 2020) |
| **MONTH** | `int64` | Transaction month (1 - 12) |
| **SUPPLIER** | `string` | Name of the supply vendor (396+ unique suppliers) |
| **ITEM CODE** | `string` | Unique identifier for individual products |
| **ITEM DESCRIPTION** | `string` | Detailed product title & volume packaging |
| **ITEM TYPE** | `string` | Product category classification (Wine, Liquor, Beer, etc.) |
| **RETAIL SALES** | `float64` | Total volume sales at retail outlets |
| **RETAIL TRANSFERS** | `float64` | Volume of stock transferred out to retail points |
| **WAREHOUSE SALES** | `float64` | Total volume sales directly from warehouses |

*Dataset Source:* [Kaggle - Retail Sales Analysis by Sahir Maharaj](https://www.kaggle.com/datasets/sahirmaharajj/retail-sales-analysis/code)

---

## ⚙️ Data Pipeline & Exploratory Analysis (`dataEDA.ipynb`)

The Jupyter Notebook captures a complete lifecycle of structural evaluation and pipeline cleaning using `pandas` and `numpy`:

1. **Structural Auditing:** Explored missing value maps showing sparse rows missing `SUPPLIER`, `ITEM TYPE`, and `RETAIL SALES` attributes.
2. **Anomaly Treatment:** - Addressed item categorization anomalies by filling undefined `ITEM TYPE` entries with `"Unknown"`.
* Cleared broken/empty rows mapping to missing sales targets (`dropna`).


3. **Distribution Profiles:** Investigated distribution curves which revealed massive volume counts dominated by **Wine** (187k+ transactions) followed by **Liquor** (64k+) and **Beer** (42k+).
4. **Sales Volume Imbalances:** Identified that warehouse transaction volume drastically outperforms retail sales velocity, with warehouse-to-retail distribution ratios scaling past `3.6x`.

---

## 📈 Business Intelligence Dashboard (`retailAnalysis.pbix`)

The accompanying **Power BI dashboard** provides a visual analytics layer designed to convert the granular rows of the cleaned dataset into actionable management insights:

* **Volume Performance Matrix:** Monitors total operational output through dedicated KPI indicators for Warehouse Shipments vs. Retail Sales.
* **Product Tier Breakdown:** Visualizes categorical breakdowns showing performance hierarchies within Wine, Beer, and Keg sales.
* **Supplier Distribution Share:** Highlights high-volume supply partners to help isolate reliance on key suppliers.
* **Temporal Analysis:** Maps seasonal shifts and yearly distributions from 2017 to 2020 to track operational trajectory over time.

---

## 🚀 How to Replicate This Project

### 1. Requirements & Prerequisites

Ensure you have the following installed on your machine:

* Python 3.8+
* Jupyter Notebook or VS Code Jupyter Extension
* Power BI Desktop (for `.pbix` visualization)

### 2. Setup & Execution

1. Clone this repository to your local system:
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME

```


2. Download the source file `Warehouse_and_Retail_Sales.csv` from the [Kaggle Dataset Link](https://www.kaggle.com/datasets/sahirmaharajj/retail-sales-analysis/code).
3. Open `dataEDA.ipynb` and update the file path in the third cell to point to your local dataset location:
```python
data = pd.read_csv("your_local_path/Warehouse_and_Retail_Sales.csv")

```


4. Run all cells to process the data and output the standardized export file (`cleaned_retail_sales_analysis.csv`).
5. Launch **Power BI Desktop**, open `retailAnalysis.pbix`, and redirect the dataset source to point to either the original source or your newly cleaned `.csv` output to play with the dashboard.

👨‍💻 About the Author
Hrushikesh Nitin Kumthekar 🎓 MSc in Data Analytics | National College of Ireland (Dublin, Ireland)
💻 Computer Engineering Graduate I design structured analytics pipelines, conduct exploratory data analysis, and transform messy datasets into clear, structured insights. This repository serves as a hands-on demonstration of my skills in Python-based data manipulation, cleaning, and extracting content metrics to uncover strategic business patterns.

🚀 Connect With Me
LinkedIn: linkedin.com/in/rnk89
GitHub: github.com/RushiKumthekar
