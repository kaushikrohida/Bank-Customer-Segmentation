# Bank Customer Churn and Segmentation Analysis

## Overview

This repository contains a comprehensive analysis of bank customer churn and segmentation. It consists of two main files:
1. **Bank Churn Dataset (`Bank_Churn.csv`)**: A dataset with detailed information about bank customers, including demographic, financial, and activity-based features. The dataset also includes a label indicating whether a customer has exited (churned) from the bank.
2. **Bank Customer Segmentation Notebook (`Bank Customer Segmentation.ipynb`)**: A Jupyter Notebook that applies machine learning techniques to segment bank customers into groups based on their behavior, allowing for a better understanding of the customer base and more informed strategic decisions.

## Dataset: Bank Churn

The `Bank_Churn.csv` file contains 10,000 records of customers from a bank. The dataset captures various attributes that can help in predicting customer churn and understanding customer behavior. 

### Columns:
- **CustomerId**: Unique identifier for each customer.
- **Surname**: Customer’s surname.
- **CreditScore**: Customer’s credit score, used to evaluate creditworthiness.
- **Geography**: The country where the customer resides (e.g., France, Spain, Germany).
- **Gender**: Gender of the customer.
- **Age**: Customer's age.
- **Tenure**: The number of years the customer has been with the bank.
- **Balance**: Current account balance of the customer.
- **NumOfProducts**: The number of financial products the customer has with the bank (e.g., savings accounts, loans, etc.).
- **HasCrCard**: Whether the customer has a credit card (1 = Yes, 0 = No).
- **IsActiveMember**: Whether the customer is considered an active member of the bank (1 = Yes, 0 = No).
- **EstimatedSalary**: The estimated annual salary of the customer.
- **Exited**: The target variable indicating if the customer has churned (1 = Yes, 0 = No).

### Key Insights:
- **Churn Prediction**: The target variable `Exited` can be used to predict which customers are likely to churn. This allows for proactive engagement with at-risk customers.
- **Credit Score Analysis**: Understanding the distribution of `CreditScore` helps assess how customer creditworthiness correlates with churn.
- **Demographics**: Features like `Geography`, `Gender`, and `Age` are important to segment the customers based on different demographic factors.
- **Customer Activity**: Variables like `NumOfProducts`, `HasCrCard`, and `IsActiveMember` provide insights into customer engagement with the bank, which is important for understanding retention strategies.

## Notebook: Bank Customer Segmentation

The `Bank Customer Segmentation.ipynb` notebook demonstrates how to segment the bank's customers using clustering techniques. The goal of segmentation is to group customers into similar clusters to tailor marketing efforts, improve customer service, and minimize churn.

### Steps Involved:

#### 1. Data Preprocessing:
- **Handling Missing Data**: Ensures the dataset is clean by dealing with any missing values.
- **Normalization**: Some variables like `EstimatedSalary` and `Balance` may have different scales, so normalization is applied to ensure that clustering is not biased by the magnitude of different features.
- **Feature Selection**: Key features such as `Age`, `Balance`, `NumOfProducts`, `EstimatedSalary`, and `CreditScore` are selected as inputs for the clustering model.

#### 2. Clustering Analysis:
- **KMeans Clustering**: This algorithm is used to create customer segments. The KMeans algorithm groups customers into clusters based on their similarities. The number of clusters (`k`) is determined using the **Elbow Method**, which helps find the optimal `k` by plotting the within-cluster sum of squares for different values of `k`.
  
- **Silhouette Score**: The notebook also calculates the Silhouette Score to evaluate the quality of clustering. A higher silhouette score indicates better-defined clusters.

#### 3. Visualization:
- **Cluster Visualization**: After fitting the KMeans model, the clusters are visualized using scatter plots. This provides an intuitive view of how different customers are grouped based on key variables like `Age`, `CreditScore`, and `Balance`.
  
- **Cluster Profiles**: Each cluster is analyzed to identify distinguishing characteristics, such as high-spending customers or younger customers with lower engagement. These insights help the bank design targeted retention or marketing strategies.

### Example Clustering Output:

| Cluster | Key Characteristics                              | Recommendations                          |
|---------|--------------------------------------------------|------------------------------------------|
| 0       | Young customers, low balance, low tenure         | Offer retention incentives, educational programs for financial literacy |
| 1       | Older customers, high balance, long tenure       | Strengthen loyalty programs, focus on high-value services |
| 2       | Mid-aged, high credit score, multiple products   | Cross-sell additional products like loans, insurance |
| 3       | Low credit score, minimal engagement, at risk    | Focus on reducing churn with targeted offers, credit-building programs |

### Business Use Cases:
- **Customer Retention**: By identifying customers who are more likely to churn, the bank can take proactive steps to engage these customers before they leave.
- **Targeted Marketing**: Segments with high potential can be offered exclusive products, while segments that are more likely to churn can be offered incentives to stay.
- **Improved Customer Experience**: Personalizing communication based on customer segments helps improve satisfaction and loyalty.


## Insights and Outcomes
This analysis enables a comprehensive understanding of:
- **Customer Churn**: Predicting churn allows for better retention strategies and customer engagement.
- **Customer Segmentation**: Grouping customers based on their financial and demographic characteristics enables personalized marketing and service strategies.
- **Key Performance Metrics**: Measures such as customer lifetime value (CLV) can be computed using these segments, allowing for an optimized focus on high-value customers.

## Next Steps
- **Expand the analysis** by testing other clustering algorithms such as Hierarchical Clustering or DBSCAN.
- **Perform predictive modeling** (e.g., Logistic Regression, Random Forest) to predict customer churn based on the available features.
- **Integrate more external features** (e.g., economic indicators, social media engagement) to improve customer segmentation and churn prediction models.

## Conclusion
The analysis of bank customer churn and segmentation provides valuable insights into customer behavior and preferences. By leveraging machine learning techniques, the bank can identify at-risk customers, tailor marketing strategies, and enhance customer engagement. This project not only highlights the importance of data-driven decision-making but also sets the foundation for future enhancements in customer relationship management. The insights gained can lead to improved customer satisfaction, increased retention rates, and ultimately, a more profitable banking operation.

## Contributing

Contributions are welcome! If you have ideas for improving the project, feel free to fork the repository and submit a pull request.

## Contact

For questions or suggestions, please contact [Kaushik Rohida](mailto:rohidakaushik@gmail.com).

