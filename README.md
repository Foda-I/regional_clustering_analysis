# 🌍 Regional Data Clustering Analysis

## 📌 Project Overview
This project applies unsupervised machine learning techniques to segment countries into distinct clusters based on key demographic and socioeconomic indicators (birth rate, death rate, life expectancy, income, etc.). The goal is to identify natural groupings within the data and evaluate the clustering performance using rigorous statistical validation metrics.

To demonstrate technical versatility, **this repository contains two parallel implementations of the exact same analysis pipeline**: one written in **Python** and one written in **R**.

## 🛠️ Tech Stack
- **Languages:** Python, R
- **Python Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `scipy`
- **R Libraries:** `factoextra`, `cluster`, `NbClust`, `vegan`, `ggplot2`
- **Tools:** Jupyter Notebook, R Markdown, Git/GitHub

## 🔍 Methodology & Analyses Performed
Both implementations follow the same rigorous data science workflow:
1. **Data Preprocessing:** Handled missing values (e.g., `-9999` codes) and standardized features using Z-score normalization.
2. **Clustering Tendency:** Applied the **Hopkins Statistic** to verify if the dataset possesses a natural clustering structure.
3. **Optimal Cluster Determination:** 
   - Used the **Elbow Method** (Within-Cluster Sum of Squares) to find the optimal number of clusters.
   - Applied **NbClust** (in R) to evaluate 30 different clustering indices.
4. **Hierarchical Clustering:** 
   - Tested multiple linkage methods (Single, Complete, Average, Centroid, Ward.D2).
   - Used the **Mantel Criterion** (Cophenetic Correlation) to select the most accurate linkage method.
5. **K-Means Clustering:** Implemented K-Means with optimized parameters and evaluated cluster quality using **Silhouette Analysis**.
6. **Visualization:** Generated dendrograms, elbow plots, and cluster scatter plots with confidence ellipses.

## 📂 Repository Structure
- `python/regional_clustering_analysis.ipynb`: The complete analysis pipeline written in Python.
- `r/regional_clustering_analysis.Rmd`: The complete analysis pipeline written in R.

*(Note: The dataset is embedded directly inside both scripts to ensure the code runs out-of-the-box without requiring external file dependencies!)*

## 💡 Key Insights
- The Hopkins statistic confirmed a strong clustering tendency in the demographic data.
- The Mantel criterion identified **Complete Linkage** as the most accurate hierarchical method for this dataset.
- K-Means clustering successfully partitioned the countries into 4 distinct socioeconomic groups, validated by a high average Silhouette width.

## 💻 How to Run

### Python
1. Open `python/regional_clustering_analysis.ipynb` in Jupyter Notebook or VS Code.
2. Run the cells sequentially to generate the visualizations and metrics.

### R
1. Open `r/regional_clustering_analysis.Rmd` in RStudio.
2. Install required packages if prompted, then click **Knit** to generate the HTML report, or run the chunks sequentially.

##  Contact
- **Email:** ibrahim.fadyy@gmail.com
- **LinkedIn:** linkedin.com/in/ibrahim-fady
