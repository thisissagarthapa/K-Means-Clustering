# Football Data Clustering using K-Means

This project applies the **K-Means clustering algorithm** to group football players based on their performance statistics. We use a dataset containing various attributes like Goals, Assists, Tackles, Pass Accuracy, and more. The clustering helps to identify patterns and similarities among players based on their game performance.

## Dataset Overview

The dataset used (`football_data.csv`) includes the following columns:

| Player Name        | Position   | Goals | Assists | Tackles | Pass Accuracy | Dribbles per Game | Interceptions | Shots per Game | Yellow Cards | Red Cards |
|--------------------|------------|-------|---------|---------|---------------|------------------|---------------|----------------|--------------|-----------|
| Neymar             | Midfielder | 17    | 10      | 103     | 84.20         | 4.11             | 0             | 4.16           | 3            | 1         |
| Kevin De Bruyne    | Forward    | 23    | 13      | 118     | 97.83         | 3.78             | 49            | 0.18           | 0            | 0         |

The dataset contains statistics for various football players over different matches. For clustering, the following features are selected:
- **Goals**
- **Assists**
- **Tackles**
- **Pass Accuracy**

## Project Steps

1. **Importing Libraries**
   - Libraries such as `NumPy`, `Pandas`, `Seaborn`, and `Matplotlib` are used for data manipulation, visualization, and plotting.
   
2. **Loading and Visualizing Data**
   - The dataset is loaded using `pandas`, and we explore it using `head()` to view the first few rows.
   - `sns.pairplot()` is used to visualize relationships between selected features.

3. **Data Preprocessing**
   - Data scaling is performed using `StandardScaler()` to standardize the features before clustering.

4. **Elbow Method**
   - The Elbow Method is applied to find the optimal number of clusters by calculating the **Within-Cluster Sum of Squares (WCSS)** for different values of `k` (from 2 to 21). 
   - The plot of WCSS helps identify the "elbow point" where adding more clusters does not significantly reduce WCSS.

5. **K-Means Clustering**
   - K-Means clustering is applied to the scaled data, choosing 4 clusters.
   - The model is fit on the data, and predictions (cluster labels) are added as a new column in the dataset.

6. **Visualization**
   - Clustered data is visualized using `seaborn.pairplot()` with `hue="predict"` to distinguish between clusters.

## How to Run

1. **Install the necessary libraries**:
   Make sure you have the required libraries installed. You can install them using `pip`:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   
## Screenshots
![Screenshot (137)](https://github.com/user-attachments/assets/098b4994-5349-433e-a15e-45c9c8756716)


![Screenshot (138)](https://github.com/user-attachments/assets/64cf574a-a1f6-4b91-b322-08ad7b3ce9bd)


![Screenshot (139)](https://github.com/user-attachments/assets/c4d56ce8-f16a-4042-8a81-826d8f4a0eeb)
