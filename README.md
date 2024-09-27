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
## My findings 

-(We will refer to data points as "segments" where applicable)

-One segment represented users who were active and frequent in their interactions with our system. These users provide us with consistent engagement and represent high-value customers. They are responsive to most updates, frequently exploring new features and services. Since they are already integrated into our ecosystem, we may not need to overwhelm them with new prompts, instead focusing on retaining them through minor, tailored enhancements.

-Another segment comprised users who were more sporadic in their usage but engaged strongly with discounts and promotional offers. However, they were less responsive to offers requiring more than a basic interaction (e.g., multiple feature use in a single session). A possible strategy would be to highlight simple, direct offerings for this group, encouraging them to interact without adding too many complex steps.

-A third segment was identified as users who only engaged during promotional periods. Their usage patterns suggest that small but frequent incentives could turn them into regular users. By offering them periodic reminders and targeted promotions over the weekends, we may convert their occasional interest into long-term engagement.

-Another interesting cluster featured users who did not show significant responsiveness to any particular kind of interaction or incentive. These could represent either a more cost-sensitive group or users who are simply not interested in the current offerings. An effective strategy might involve introducing a more basic tier of features or experimenting with simplified user flows to cater to them.

-A notable segment reflected users who had moderate interactions and steady usage patterns. They didn't seem to require constant updates or promotions but could benefit from more customized features that align with their steady, reliable use of the system.

-Finally, one segment displayed no regular pattern of interaction and was composed of users who visited the platform once or twice but never returned. This group is a reminder that not every user will follow a predictable journey, and it's important to recognize that not all mathematical patterns directly translate into practical actions. Some users simply may not be our target audience, and forcing engagement here may not be a productive focus.


## Conclusion

By segmenting Starbucks customers into different groups, this project provides insights into customer behavior and preferences. These insights can help inform marketing strategies, targeted offers, and customer retention efforts.

