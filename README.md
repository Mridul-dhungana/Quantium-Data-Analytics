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

* **Objective:** Evaluate whether a new chip-aisle layout in stores 77, 86, and 88 raised sales during February–April 2019, beyond what those stores would have done anyway.
* **Key Actions:**
  * Kept the 259 stores that were open for all 12 months from July 2018 through June 2019.
  * Counted distinct transactions (`TXN_ID`), because some transactions contain more than one product line.
  * Matched each trial store to a control on pre-trial total sales, customers, and transactions per customer, using correlation and magnitude distance. The pairs are 77→233, 86→138, and 88→201.
  * Scaled each control to its trial store's pre-trial level, then tested whether the February–April percentage gap was larger than the gap those two stores already had from July 2018 through January 2019.
* **Key Insight:** Store 77's sales (+33%, p = 0.002) and customers (+31%, p < 0.001) beat store 233 in March and April, then the sales gap is −16% in May. Transactions per customer do not move. Store 86's average gap is a February spike and fades by March. Store 88 shows no uplift once its 14% pre-trial size advantage over store 201 is removed.

### 3. Commercial Reporting

* Summarized findings into a professional report for stakeholders, focusing on the "Why" behind the data.

---

## 🛠️ Tech Stack

* **Language:** Python
* **Libraries:**
  * `pandas` and `numpy` for data manipulation
  * `matplotlib` and `seaborn` for visualization
  * `scipy.stats` for the uplift t-test

---

## 📂 Repository Structure

```text
├── QVI_transaction_data.csv          # Raw transaction records
├── QVI_purchase_behaviour.csv        # Customer segment data
├── merged_data.csv                   # Cleaned transaction and customer merge
├── Data Analytics.ipynb              # Cleaning and customer-segment analysis
├── Trial and Control stores.ipynb    # Trial vs control uplift test
├── Chips Analytics Report.pdf        # Stakeholder report
├── Quantium Data Analytics.twbx      # Tableau workbook
└── README.md
```

---

## 🚀 Key Findings

1. **Top Segment:** "Mainstream - Young Singles/Couples" are a major growth lever. They are more likely to buy 175g packs and specific brands like Tyrells or Kettle.
2. **Brand Preference:** Customers are loyal to specific brands, and pack size significantly influences the "Price per unit."
3. **Trial result:** Do not roll the new chip layout out. Store 77 is the only store with a trial-window lift in sales and customers, that lift ends in May, and part of the March–April gap is store 233 falling. Store 86 does not sustain a lift. Store 88 does not have one.

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

3. **Run the notebooks:** Open `Data Analytics.ipynb` first, then `Trial and Control stores.ipynb`. The trial notebook reads `merged_data.csv` from this folder.

---
