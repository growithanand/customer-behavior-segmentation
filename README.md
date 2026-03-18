# Customer Behavior Segmentation using RFM Analysis and K-Means

## 📌 Project Overview

This project performs **customer segmentation** using transactional retail data.
The goal is to group customers based on their purchasing behavior and generate actionable business insights.

We use:

* **RFM Analysis** (Recency, Frequency, Monetary)
* **Data Transformation (Log + Scaling)**
* **K-Means Clustering**
* **PCA Visualization**

---

## 🎯 Objective

Segment customers into meaningful groups such as:

* 💎 VIP Customers
* 🙂 Regular Customers
* ⚠️ At-Risk Customers
* 💤 Lost Customers

This helps businesses:

* Improve customer retention
* Target marketing campaigns
* Increase revenue

---

## 📂 Dataset

* Source: UCI Online Retail Dataset
* Contains transactional data for a UK-based online retail store

---

## 🧠 Methodology

### 1. Data Cleaning

* Removed missing `CustomerID`
* Removed negative `Quantity` and `UnitPrice`
* Created `TotalPrice = Quantity × UnitPrice`

---

### 2. Feature Engineering (RFM)

| Feature   | Description              |
| --------- | ------------------------ |
| Recency   | Days since last purchase |
| Frequency | Number of purchases      |
| Monetary  | Total amount spent       |

---

### 3. Data Transformation

* Applied **log transformation** to reduce skewness
* Applied **StandardScaler** to normalize feature scales

---

### 4. Choosing Number of Clusters

## Elbow Method

![Elbow Method](images/elbow_method.png)

* Optimal number of clusters chosen: **K = 4**

---

### 5. K-Means Clustering

* Applied K-Means with `K = 4`
* Evaluated using **Silhouette Score**

---

### 6. PCA Visualization

## Customer Segments

![Customer Segments](images/pca_clusters.png)

---

## 📊 Results & Insights

### 🟠 VIP Customers

* High frequency
* High spending
* Recent activity
  👉 Most valuable customers

---

### 🔵 Regular Customers

* Moderate activity
* Average spending
  👉 Stable customer base

---

### 🟢 At-Risk Customers

* Recently active
* Low frequency & spending
  👉 Opportunity for engagement

---

### 🔴 Lost Customers

* Inactive
* Low frequency
* Low spending
  👉 Require reactivation strategies

---

## 💡 Business Recommendations

* **VIP Customers** → Loyalty programs, exclusive offers
* **Regular Customers** → Upselling & cross-selling
* **At-Risk Customers** → Targeted promotions
* **Lost Customers** → Re-engagement campaigns

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## 🚀 How to Run

```bash
git clone <your-repo-link>
cd customer-behavior-segmentation
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

## 📈 Future Improvements

* Try **DBSCAN / Hierarchical clustering**
* Add **dashboard (Streamlit / Power BI)**
* Deploy as a web app

---

## 🙌 Author

Anand

---
