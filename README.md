# 🛍️ Customer Segmentation Project

A machine learning project that applies **K-Means Clustering** to segment mall customers into distinct behavioral groups based on their annual income and spending score — enabling data-driven, targeted marketing strategies.

---

## 📌 Project Overview

This project analyzes a dataset of 200 mall customers and groups them into meaningful segments using unsupervised machine learning. The goal is to help businesses understand their customer base and tailor marketing efforts to each group.

---

## 📁 Project Structure

```
Lab_Customer_Segmentation_Project.ipynb   # Main Jupyter Notebook
README.md                                 # Project documentation
```

---

## 📊 Dataset

The dataset is synthetically generated to simulate real-world mall customer data and contains **200 customers** with the following features:

| Feature             | Description                              |
|---------------------|------------------------------------------|
| `CustomerID`        | Unique identifier (1–200)                |
| `Age`               | Customer age (18–70 years)               |
| `Annual_Income_k`   | Annual income in thousands of dollars    |
| `Spending_Score`    | Mall-assigned score (1–100) based on behavior |

**Key Statistics:**
- Age range: 18 to 70 years (avg ~39)
- Income range: $15k to $137k (avg ~$60k)
- Spending Score range: 1 to 99 (avg ~50)
- No missing values — data is clean and ready to use

---

## 🧰 Tech Stack & Libraries

| Library        | Purpose                             |
|----------------|-------------------------------------|
| `pandas`       | Data loading and manipulation       |
| `numpy`        | Numerical computations              |
| `matplotlib`   | Data visualization                  |
| `seaborn`      | Correlation heatmaps                |
| `scikit-learn` | KMeans, StandardScaler, PCA, Silhouette Score |

---

## ⚙️ Workflow

### 1. 📥 Data Preparation
- Dataset created in-memory with 200 customers
- Verified for null values and correct data types
- Descriptive statistics computed for each feature

### 2. 📈 Exploratory Data Analysis (EDA)
- **Distribution plots** for Age, Income, and Spending Score
- **Scatter plot** of Income vs. Spending Score (reveals natural groupings)
- **Correlation heatmap** — confirms features are largely independent

### 3. ⚖️ Feature Scaling
- Selected `Annual_Income_k` and `Spending_Score` for clustering
- Applied `StandardScaler` to normalize both features to the same scale

### 4. 🔍 Finding Optimal K
Two methods used to determine the best number of clusters:

- **Elbow Method** — plots inertia (WCSS) for K = 2 to 10; elbow observed at **K = 5**
- **Silhouette Score** — measures cluster cohesion and separation; highest score confirmed at **K = 5**

### 5. 🤖 K-Means Clustering
- Trained `KMeans` with K = 5, `random_state=42`, `n_init=10`
- Assigned cluster labels to each customer
- Visualized segments with color-coded scatter plots and centroids

### 6. 🔬 PCA Visualization
- Applied `PCA` (2 components) for an alternate visual perspective of clusters
- All variance captured since only 2 input features were used

### 7. 🏷️ Segment Naming & Business Insights
- Each cluster labeled based on average income and spending levels
- Actionable marketing strategy defined for each segment

---

## 👥 Customer Segments Discovered

| Cluster | Segment Profile                        | Strategy Priority          |
|---------|----------------------------------------|----------------------------|
| 0       | Low Income, Low Spenders               | Engage with value offers   |
| 1       | Low Income, High Spenders              | Maintain loyalty           |
| 2       | Medium Income, Moderate Spenders       | Grow to higher segments    |
| 3       | High Income, Low Spenders              | Activate spending          |
| 4       | High Income, High Spenders (VIPs)      | Retain and expand          |

> Cluster boundaries are determined dynamically based on cluster center averages.

---

## 📢 Marketing Recommendations

| Segment              | Key Actions                                               |
|----------------------|-----------------------------------------------------------|
| 💎 VIP Customers      | VIP memberships, early product access, 2x loyalty points  |
| 🎯 Potential Spenders | Personalized deals, flash sales, premium product nudges   |
| ⭐ Enthusiastic Shoppers | Bundles, installment plans, budget loyalty rewards     |
| 📊 Budget Conscious   | Clearance alerts, essential items, basic rewards          |
| 📈 Middle Market      | Seasonal campaigns, cross-sell and upsell opportunities   |

---

## 📉 Model Evaluation

| Metric           | Value    |
|------------------|----------|
| Algorithm        | K-Means  |
| Optimal K        | 5        |
| Silhouette Score | ~0.55+   |
| Features Used    | Annual Income, Spending Score |

---

## 🚀 How to Run

1. **Clone or download** this repository
2. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. **Open the notebook:**
   ```bash
   jupyter notebook Lab_Customer_Segmentation_Project.ipynb
   ```
4. **Run all cells** from top to bottom

---

## ✅ Key Takeaways

- Customers naturally form **5 distinct behavioral groups**
- **Income and spending behavior** are the most useful segmentation features
- The **VIP segment** (high income + high spending) represents the highest business value
- The **High Income, Low Spending** group presents the greatest growth opportunity
- Each segment demands a **unique marketing approach** for maximum ROI

---

