
# Quantium Data Analytics Virtual Experience

This repository contains my completion of the Quantium Data Analytics Virtual Experience. The project focuses on analyzing retail data to uncover customer insights, conducting experimentation/uplift testing, and delivering commercial recommendations.

## 📋 Project Overview

The goal of this project was to analyze chip purchasing behavior for a large retail brand (Quantium) to help the Category Manager make data-driven decisions regarding store performance and customer segmentation.

### 1. Data Preparation and Customer Analytics

* **Objective:** Clean the transaction and customer data to identify purchasing patterns.
* **Key Actions:**
* Cleaned data by removing outliers (e.g., a customer making 200-pack purchases).
* Engineered new features: `Pack Size` and `Brand Name` from product descriptions.
* Merged transaction data with customer segments (`Lifestage` and `Premium Type`).


* **Key Insight:** Mainstream Young Singles/Couples and Mainstream Retirees are the highest contributors to sales.

### 2. Experimentation and Uplift Testing

* **Objective:** Evaluate the performance of store trials in Stores 77, 86, and 88.
* **Key Actions:**
* Selected "Control Stores" using Correlation and Magnitude Distance metrics.
* Compared trial store performance against control stores during the trial period.
* Calculated t-values and 95% confidence intervals to ensure statistical significance.


* **Key Insight:** Store 77 and 88 showed significant uplift in sales and customer traffic, while Store 86's results were more varied.

### 3. Commercial Reporting

* Summarized findings into a professional report for stakeholders, focusing on the "Why" behind the data.

---

## 🛠️ Tech Stack

* **Language:** Python
* **Libraries:** * `pandas` & `numpy` (Data Manipulation)
* `matplotlib` & `seaborn` (Data Visualization)
* `scipy.stats` (Statistical Testing)
* `datetime` (Time-series analysis)



---

## 📂 Repository Structure

```text
├── Data/
│   ├── QVI_transaction_data.xlsx    # Raw transaction records
│   └── QVI_purchase_behaviour.csv   # Customer segment data
├── Notebooks/
│   ├── Task_1_EDA.ipynb             # Cleaning & Segment analysis
│   └── Task_2_Experimentation.ipynb # Trial vs Control store analysis
└── README.md

```

---

## 🚀 Key Findings

1. **Top Segment:** "Mainstream - Young Singles/Couples" are a major growth lever. They are more likely to buy 175g packs and specific brands like Tyrells or Kettle.
2. **Brand Preference:** Customers are loyal to specific brands, and pack size significantly influences the "Price per unit."
3. **Trial Success:** The layout changes in Trial Stores 77 and 88 successfully drove higher transaction volumes.

---

## 📈 How to Use

1. **Clone the repo:**
```bash
git clone https://github.com/Mridul-dhungana/Quantium-Data-Analytics.git

```


2. **Install dependencies:**
```bash
pip install pandas matplotlib seaborn scipy

```

3. **Run the Notebooks:** Open Jupyter Lab/Notebook and run the `.ipynb` files in sequence to see the full analysis.

---


