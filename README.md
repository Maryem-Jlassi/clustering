# Customer Segmentation and Clustering

This notebook performs customer segmentation on a marketing campaign dataset to identify distinct groups of customers based on their spending behavior and demographic features. The dataset contains 2,240 rows and 29 features, including customer demographics, campaign responses, and purchase behavior. The main goal of the analysis is to cluster customers into different segments to help the company optimize marketing strategies.
##  Dataset Overview
The dataset "marketing_campaign.csv" contains the following features:

ID: Customer identifier

Year_Birth: Birth year of the customer

Education: Education level of the customer

Marital_Status: Marital status of the customer

Income: Annual income of the customer

Kidhome: Number of kids in the household

Teenhome: Number of teenagers in the household

Dt_Customer: Date the customer registered in the database

Recency: Number of days since the customer last made a purchase

MntWines: Amount spent on wine

MntFruits: Amount spent on fruits

MntMeatProducts: Amount spent on meat products

MntFishProducts: Amount spent on fish products

MntSweetProducts: Amount spent on sweet products

MntGoldProds: Amount spent on gold products

NumDealsPurchases: Number of deals purchased

NumWebPurchases: Number of web purchases

NumCatalogPurchases: Number of catalog purchases

NumStorePurchases: Number of store purchases

NumWebVisitsMonth: Number of web visits per month

AcceptedCmp1-5: Number of times the customer accepted various campaigns

Complain: Whether the customer made a complaint (binary)

Z_CostContact: Cost of contact with the customer

Z_Revenue: Revenue generated from the customer

Response: Whether the customer responded to the campaign (binary)

## Steps Performed

### Data Preprocessing & Feature Engineering
**1.Missing Values:** Dropped missing values from the dataset.

**2.Feature Creation:**

-Created a new feature, "Customer_For," indicating the number of days a customer has been registered with the company.

-Extracted the customer's Age from their birth year.

-Created the Spent feature, representing the total amount spent across various product categories.

-Created the Children feature, indicating the total number of children in a household.

-Simplified the Education feature into three categories based on the value counts.

**3.Feature Scaling:**

-Performed label encoding on categorical variables.

-Applied Standard Scaling to the numerical features for model consistency.

**4.Dimensionality Reduction:**

Reduced the dimensions of the dataset to three using PCA for better clustering visualization.
### Clustering

**1.Elbow Method:** Used the Elbow Method to determine the optimal number of clusters for customer segmentation.

**2.Clustering Algorithms:**

-Performed K-Means Clustering to partition the dataset into distinct groups based on spending behavior and income.

-Applied Agglomerative Clustering to validate the clustering results.

**3.Cluster Analysis:**

Analyzed the clusters based on spending behavior and income. The customer segments were categorized as follows:

-Group 0: High spending & Average income

-Group 1: High spending & High income

-Group 2: Low spending & Low income

-Group 3: High spending & Low income

### Insights & Conclusions
***Key Insights:***

Group 1 (High spending & High income) and Group 2 (Low spending & Low income) are the most distinct customer segments.

Group 0 and Group 3 are also significant, with Group 3 showing high spending despite lower income.

The last marketing campaign appears to have been successful, attracting a diverse set of customers across various income levels, particularly those in Group 4 (High spending & Low income), which could be further targeted in future campaigns.

***Recommendations:***
Marketing campaigns should focus not only on Group 2 (High spending, High income) but also on Group 4 (High spending, Low income) as they show significant loyalty despite lower income.

## Requirements
To run this notebook, you need the following Python packages:

pandas

numpy

matplotlib

seaborn

scikit-learn

Install the necessary packages using pip:

pip install pandas numpy matplotlib seaborn scikit-learn

## License
This project is licensed under the MIT License - see the LICENSE file for details.

