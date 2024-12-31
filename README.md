# Data-Clustering-Using-Credit-Card-Dataset

### Dataset Description
This dataset was derived and simplified for learning purposes. It includes usage behavior of about 9000 active credit card holders during a 6-month period. This case requires developing a customer segmentation to define a marketing strategy.

### Dataset Link
(https://drive.google.com/file/d/1Yb4ljRXRQfTmcLOac_5w-pLpvPdFPvnc/view)

### Columns Explanation
- **CUST_ID**: Identification of Credit Card holder (Categorical)
- **BALANCE_FREQUENCY**: How frequently the balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
- **PURCHASES**: Amount of purchases made from the account
- **CASH_ADVANCE**: Cash in advance given by the user
- **CREDIT_LIMIT**: Limit of Credit Card for user
- **PAYMENTS**: Amount of payment done by the user

## Steps
1. **Import Data and Perform Basic Data Exploration**
2. **Data Preparation Steps**
   - Handle corrupted and missing values.
   - Encode categorical data, if applicable.
   - Identify and handle outliers.

3. **Hierarchical Clustering**
   - Use hierarchical clustering to identify inherent groupings within the data.
   - Select two features (e.g., 'PURCHASES' and 'CREDIT_LIMIT') for clustering.
   - Plot the resulting clusters.

4. **Partitional Clustering with K-Means**
   - Apply the K-means algorithm to perform clustering.
   - Plot the resulting clusters.

5. **Optimize Clustering**
   - Find the best value for *k* (number of clusters).
   - Re-run K-means with the optimized *k*.
   - Plot and interpret the updated clusters.

---

## Results Interpretation
### Cluster Analysis
- **Cluster Centers**:
  ```
  [[ 0.29885371  0.89756034  1.26174224  1.50710916  1.06446513]
   [-0.05830221 -0.17510157 -0.24614841 -0.29401609 -0.20766238]]
  ```

- **Cluster Sizes**:
  ```
  [1457, 7493]
  ```

### Meaning of the Clustering Result
The clustering results reveal insights about customer behavior patterns and their credit card usage. 
1. **Cluster Centers**:
   - The two clusters represent two distinct groups of credit card users based on standardized feature values (e.g., balance frequency, purchases, payments, credit limit, and cash advance).
   - **Cluster 1 (Higher values)**: Customers in this group generally have higher purchases, payments, credit limits, and cash advances. They are likely high-spending individuals who actively use their credit cards and may have higher creditworthiness or engagement.
   - **Cluster 2 (Lower values)**: Customers in this group exhibit lower values for purchases, payments, and credit utilization. They may be more conservative users or have limited engagement with their credit cards.

2. **Cluster Sizes**:
   - Cluster 1 contains **1457 customers**: Represents a smaller, high-activity group with distinct financial behavior, possibly the "premium" or "power users."
   - Cluster 2 contains **7493 customers**: Represents the majority of the dataset, likely standard or low-usage credit card holders.

3. **Implications**:
   - **Marketing Strategies**:
     - Cluster 1 can be targeted with premium offers, loyalty rewards, and personalized financial products to enhance engagement further.
     - Cluster 2 may benefit from educational campaigns to encourage increased usage or lower-risk product offerings to meet their needs.
   - **Risk Assessment**:
     - High activity in Cluster 1 might indicate potential risks if payments do not keep up with purchases or credit limits. Monitoring is crucial.
     - Cluster 2's low activity suggests lower immediate financial risk but may present opportunities for growth.

4. **Segmentation Value**:
   - By understanding these clusters, financial institutions can tailor strategies to maximize customer satisfaction, improve credit utilization, and minimize risks. It also allows for better resource allocation toward high-value customers.
