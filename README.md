# US Crime Analytics: Multi-Algorithm Clustering ⚖️🚓

## 📌 Project Overview
This project performs an unsupervised machine learning analysis on US crime statistics to segment states into distinct risk profiles. By utilizing both K-Means and Hierarchical Clustering, the model identifies specific crime signatures—ranging from high-violence rural areas to dangerous urban hubs—allowing for data-backed federal resource allocation and targeted public safety policy intervention.

## 📊 Dataset Description
The dataset contains crime statistics for 50 US states across four key dimensions.
* **Dataset Size:** 50 records, 4 variables.
* **Key Features:**
  * `Murder`: Murder arrests (per 100,000).
  * `Assault`: Assault arrests (per 100,000).
  * `UrbanPop`: Percent of the population living in urban areas.
  * `Rape`: Rape arrests (per 100,000).

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (K-Means), `scipy` (Hierarchical Clustering)
* **Data Visualization:** `matplotlib`, `seaborn`

## 🧠 Methodology
1. **Exploratory Data Analysis (EDA):** Generated a **Correlation Heatmap** to identify the link between Assault and Murder rates.
2. **Data Scaling:** Applied **StandardScaler** to normalize the data, ensuring the high magnitude of `Assault` numbers didn't dominate the clustering distance calculations.
3. **Algorithm 1: Hierarchical Clustering:** * Generated a **Dendrogram** to visualize the natural groupings.
   * Successfully segmented the 50 states into 3 distinct branches (HC_Clusters).
4. **Algorithm 2: K-Means Clustering:**
   * Utilized an **Elbow Curve** to identify the optimal number of clusters (K=4).
   * Visualized the groupings through a **Cluster Scatter Plot**.

## 📈 Key Results & Analytics Inference
The dual-model approach revealed critical insights into the relationship between urbanization and violence.

* **The Murder Gap:** Hierarchical Clustering revealed that Murder rates in the high-risk cluster (avg ~12.3) are **4x higher** than in the safe cluster (avg ~3.09).
* **Urbanization Paradox:** K-Means revealed that while Cluster 1 (High-Violence) has a lower urban population than major hubs, it suffers from the highest murder rates (~14). This proves that violent crime is not purely a result of population density.
* **Optimal K-Value:** The **Elbow Curve** confirmed K=4 as the mathematical "sweet spot" for balancing cluster cohesion and separation.

## 💼 Business Impact & Strategic Action Plan
* **Cluster 1 (High-Violence):** Action: These regions face intense violent crime challenges. Deployment should focus on high-priority violent crime intervention and community-based de-escalation.
* **Cluster 3 (Dangerous Urban Hubs):** Action: Highest Assault/Rape rates in dense cities (~76% Urban). Focus on public safety infrastructure: better street lighting and increased metropolitan patrol.
* **Cluster 0 (Stable Metro States):** Action: High urbanization (~74%) with lower violence. These are "Model States." Study their social programs for national implementation.
* **Cluster 2 (Safe Rural States):** Action: Lowest crime across all categories. Focus on maintaining current community stability and lower-intensity patrol.

