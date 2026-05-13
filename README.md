In this project, I developed a complete unsupervised machine learning workflow to segment credit card customers based on their usage behavior using the CC_GENERAL.csv dataset. The primary objective was to group similar customers together to help the company understand distinct behavioral segments and design more effective, targeted marketing strategies.

I performed a comprehensive Exploratory Data Analysis (EDA) to uncover underlying patterns, specifically using histograms to analyze feature distributions and correlation heatmaps to identify relationships between variables like balance, purchases, and cash advances. To ensure the data was suitable for distance-based clustering, I handled missing values in the CREDIT_LIMIT and MINIMUM_PAYMENTS columns using mean imputation and applied StandardScaler to normalize the features. This step was critical because K-Means relies on Euclidean distance, and features with larger ranges would otherwise disproportionately influence the cluster assignments.

I first used the Elbow Method and Silhouette Scores to determine the optimal number of clusters, ultimately selecting 
K=3
 as it provided the highest silhouette score (~0.25) and a clear "elbow" in the inertia plot. I then implemented the final K-Means model and leveraged Principal Component Analysis (PCA) to reduce the high-dimensional data into two components for 2D visualization.

I evaluated the segments by analyzing the mean values of each feature within the clusters, leading to the following conclusions:

Segment Diversity: The model successfully identified three distinct groups: Cash-Reliant users (high cash advances), High-Value/VIP spenders (high purchases and credit limits), and Low-Engagement users (small balances and infrequent activity).

Strategic Insight: While the Low-Engagement group is the largest, the High-Value segment offers the greatest opportunity for loyalty rewards.

Marketing Application: By identifying the specific needs of each cluster—such as offering interest rate incentives to cash users or premium perks to VIPs—the company can move from a "one-size-fits-all" approach to data-driven, personalized marketing strategies.