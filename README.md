# Flipkart-Customer-Support-Satisfaction-Analysis
This project aims to evaluate Flipkart’s customer satisfaction through an end-to-end machine learning pipeline. The dataset comprises over 85,000 support tickets with attributes such as channel, category, sub-category, item price, resolution time, CSAT score, and customer remarks.

The project begins with data cleaning and exploration, revealing high levels of missing values, especially in customer remarks and item prices. Missing item_price values were imputed with the column mean to maintain numeric consistency. Columns were standardized by stripping and replacing spaces with underscores for code clarity.

The EDA phase examined support volume per category, CSAT score distributions, resolution times, and the performance of top agents. These visualizations uncovered critical insights: categories like “Order Related” and “Product Queries” dominate volume, while resolution time directly impacts CSAT scores. This analysis was visualized with count plots, bar charts, and box plots under the UBM structure.

A sentiment analysis of customer remarks using VADER identified the distribution of customer sentiments into Positive, Neutral, and Negative, providing another dimension to measure service satisfaction and correlate textual feedback with CSAT scores.

In feature engineering, categorical columns were label encoded and standard scaling was applied. Resolution time was engineered as a new feature from timestamp columns. For unsupervised learning, PCA followed by KMeans clustering (k=5) visualized interaction patterns, potentially segmenting user behaviors or service challenges.

For supervised learning, CSAT score (1–5) was predicted using multiple classification models:

Logistic Regression achieved 70% test accuracy but poorly classified low satisfaction scores.

SVM (RBF, Poly) consistently predicted class 5 well but underperformed on others, showing class imbalance.

Evaluation metrics like precision, recall, and F1-scores were plotted for interpretability.

The best models were saved using joblib, and loaded again for deployment sanity checks, completing the deployment-readiness aspect of the capstone. The pipeline is scalable, replicable, and aligned for production use.

🧩 Problem Statement
To identify and analyze key factors influencing Flipkart’s customer satisfaction with support services, uncover sentiment trends, and build predictive models that help in improving service experience and operational efficiency.
