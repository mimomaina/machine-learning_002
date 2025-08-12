# Customer Personality Analysis Using K-Means Clustering

This repository contains a Jupyter notebook that performs customer segmentation using **K-Means clustering** on a customer personality dataset. The goal is to group customers into distinct segments based on demographic and behavioral characteristics.

## Dataset

The dataset contains information about customers, including demographics, purchase behavior, and spending patterns.  
Typical columns include:
- **Demographics:** Age, Education, Marital Status, Income
- **Purchase Behavior:** Spending on different product categories, total purchases
- **Marketing Response:** Acceptance of campaigns, web purchases, catalog purchases
- **Other Features:** Number of children, tenure, etc.

## Analysis Workflow

1. **Data Preprocessing**
   - Loaded the dataset and inspected data structure.
   - Handled missing values.
   - Encoded categorical variables.
   - Scaled numerical features using `StandardScaler`.

2. **Feature Engineering**
   - Created aggregated features such as total spending and total purchases.
   - Selected relevant features for clustering.

3. **Modeling**
   - Used the **Elbow method** to determine the optimal number of clusters.
   - Applied **K-Means clustering**.
   - Evaluated cluster separation using the silhouette score.

4. **Cluster Profiling**
   - Analyzed each cluster’s demographic and behavioral characteristics.
   - Compared spending habits across clusters.

5. **Visualization**
   - Reduced dimensions using **PCA** for visualization.
   - Plotted clusters to show separation.

## Results

The clustering process produced **n** distinct customer segments, each representing a group with similar spending behavior and demographics.  
Key takeaways include:
- Identification of high-value customers.
- Recognition of low-engagement segments.
- Insights into targeted marketing opportunities.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage

1. Clone this repository:
   ```bash
   git clone <repo-url>
   
## Install dependencies:


pip install -r requirements.txt

## Open the Jupyter notebook:


jupyter notebook Customer_personality.ipynb

## License
This project is licensed under the MIT License.


