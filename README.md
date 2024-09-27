# Starbucks Customer Segmentation

## Overview
This project is focused on performing customer segmentation based on Starbucks customer data using clustering techniques. The dataset is processed and analyzed using various machine learning methods to classify customers into different segments based on their behavior and preferences.

## Project Structure
- **Portfolio Dataset**: Contains information about different offers, such as BOGO, discount, and informational offers.
- **Profile Dataset**: Contains demographic information about customers, such as age, gender, and income.
- **Transcript Dataset**: Logs interactions with offers, including events like offer received, offer viewed, and transaction data.

## Steps Involved

### 1. Data Loading
The data is loaded from three JSON files: `portfolio.json`, `profile.json`, and `transcript.json`. These files provide necessary data on offers, customer profiles, and transactions, respectively.

### 2. Data Preprocessing
The preprocessing involves:
- Handling missing values in the `profile` dataset.
- Scaling the `income` feature using `MinMaxScaler`.
- One-hot encoding for categorical variables like `gender` and `offer_type`.

### 3. Feature Engineering
Additional features are generated for improved customer segmentation:
- **Reward to difficulty ratio** for offers.
- **Completion rate of offers** for each customer.
- Aggregating transaction data to understand customer behavior.

### 4. Clustering and Dimensionality Reduction
The following methods are used for customer segmentation:
- **KMeans Clustering**: Customers are grouped based on patterns in their transaction history and demographic details.
- **Gaussian Mixture Models (GMM)**: An alternative to KMeans, offering more flexibility by assuming clusters follow a Gaussian distribution.
- **PCA**: Principal Component Analysis (PCA) is used to reduce dimensionality while preserving variance in the data.
- **t-SNE**: t-Distributed Stochastic Neighbor Embedding is applied to visualize high-dimensional data in two or three dimensions.

### 5. Evaluation
Silhouette score and visualization techniques are used to evaluate the quality of clustering.

## Libraries Used
- `pandas` for data manipulation.
- `numpy` for numerical operations.
- `sklearn` for machine learning tasks like clustering, scaling, and dimensionality reduction.
- `seaborn` and `matplotlib` for data visualization.

## Visualization
The project makes extensive use of visualizations to assess the clusters and understand the data better:
- PCA and t-SNE plots for cluster visualization.
- Heatmaps and bar plots to visualize feature distributions.

## How to Run
1. Clone this repository and navigate to the project directory.
2. Run the Jupyter notebook or script to execute the analysis
   ```bash
   jupyter notebook Starbucks_Customer_Segmentation.ipynb
   ```

## Conclusion

By segmenting Starbucks customers into different groups, this project provides insights into customer behavior and preferences. These insights can help inform marketing strategies, targeted offers, and customer retention efforts.

