# 📊 Customer Segmentation using PCA & K-Means

A machine learning project focused on unsupervised customer segmentation. This repository demonstrates end-to-end data preprocessing, outlier removal, feature standardization, and dimensionality reduction via **Principal Component Analysis (PCA)** on marketing campaign data.

---

## 📌 Project Overview

Understanding customer behavior is essential for targeted marketing strategies. This project cleans and transforms raw customer demographics and campaign response data into a low-dimensional feature space optimized for cluster analysis.

### Key Pipeline Steps:
* **Data Cleaning & Imputation:** Dropped non-predictive tracking columns (`ID`, `Dt_Customer`, `Z_CostContact`, `Z_Revenue`) and imputed missing `Income` values using the median.
* **Outlier Mitigation:** Applied 1.5 × IQR filtering to eliminate extreme variance across numeric features.
* **Feature Standardization:** Scaled continuous variables using `StandardScaler` ($\mu = 0$, $\sigma = 1$).
* **Dimensionality Reduction:** Compressed 23 continuous features into **12 Principal Components**, preserving **95.61%** of total dataset variance while removing redundant noise.

---

## 🛠️ Tech Stack & Dependencies

* **Language:** Python 3.8+
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

Install all required packages via pip:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn notebook


📂 Project Structure
├── data/
│   └── marketing_campaign.csv
├── notebooks/
│   └── customer_segmentation.ipynb
├── .gitignore
└── README.md

Clone the repository:
git clone [https://github.com/your-username/customer-segmentation-pca-kmeans.git](https://github.com/your-username/customer-segmentation-pca-kmeans.git)
cd customer-segmentation-pca-kmeans

Prepare the Data:
Place marketing_campaign.csv inside the data/ folder. Ensure the loading path in the notebook points to the correct relative path:
df = pd.read_csv('./data/marketing_campaign.csv', sep='\t')

Run the Notebook:
Launch Jupyter Notebook or VS Code to run customer_segmentation.ipynb:
jupyter notebook notebooks/customer_segmentation.ipynb
