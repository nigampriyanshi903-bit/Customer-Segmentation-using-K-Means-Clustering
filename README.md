# Customer-Segmentation-using-K-Means-Clustering
Predicting house prices using Linear Regression and XGBoost. Focuses on feature engineering, log transformation of the target variable, and achieving 90% R-squared score

##  Project Goal

The primary objective of this project was to leverage **Unsupervised Learning (K-Means Clustering)** to divide mall customers into distinct groups (segments) based on their demographics (Age) and purchasing behavior (Annual Income and Spending Score). This segmentation provides actionable insights for creating highly targeted and effective marketing strategies.

##  Key Methodology: K-Means Clustering

1.  **Data Preprocessing:**
    * Irrelevant identifier (`CustomerID`) was dropped.
    * Categorical feature (`Gender`) was converted into numerical format using **One-Hot Encoding**.
    * All features were standardized using **StandardScaler** to ensure equal influence on the distance-based clustering algorithm.
2.  **Optimal K Selection:** The **Elbow Method** was employed, which indicated **K=5** as the optimal number of clusters by observing where the **WCSS (Within-Cluster Sum of Squares)** curve significantly flattens.
3.  **Clustering:** A K-Means model was trained with $K=5$, successfully partitioning the 200 customers into 5 distinct groups.

---

##  Final Segments and Business Interpretation

The 5 segments were primarily defined by the intersection of **Annual Income** and **Spending Score**:

| Segment ID | Business Name | Avg Annual Income (k\$) | Avg Spending Score | Key Marketing Strategy |
| :---: | :--- | :---: | :---: | :--- |
| **0** | **The Spending Elite** | $86.5 | **82.1** | **Retention & Exclusivity.** Focus on premium products and high-tier loyalty rewards. |
| **1** | **The Careful Elite** | **$89.5** | **18.0** | **Conversion.** Target with personalized high-value offers and focus on overcoming their reluctance to spend. |
| **2** | **The Mid-Segment** | $49.2 | $40.1 | **Standardization.** General promotions and seasonal sales. |
| **3** | **Young Spenders** | $39.7 | $61.2 | **Impulse Generation.** Use discounts, trending items, and social media marketing to encourage immediate purchases. |
| **4** | **The Conservatives** | $53.7 | $36.8 | **Reliability.** Focus on brand trust, value-for-money, and simple, direct promotions. |

---

## Repository Contents

* `Mall_Customer_Segmentation.ipynb`: The complete notebook detailing all steps from data loading to final cluster visualization and interpretation.
* `README.md`: This project summary.
* `requirements.txt`: Necessary Python dependencies.

**Dependencies:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.
