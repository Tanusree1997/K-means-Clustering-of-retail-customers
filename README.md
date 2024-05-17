**Global Electronics Retailer Customer Segmentation**

**RFM Clustering**
![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/63a5605b-81ac-4d10-8264-89c919c108e4)

This project aims to do customer segmentation analysis using RFM or Recency, Frequency and Monetary Method for the Global Electronics Retailer. For this, the python libraries like Pandas, Numpy, Matplotlib, Seaborn and the machine learning models like K-means have been used. Through this clustering analysis, significant customer segments have been identified.

**Dataset Used**

For this project, I have used the Global Electronics Retailer Data from Maven Analytics. This dataset contains 5 tables: Customers, Store, Sales, Products and Exchange rates. For customer segmentation using RFM method we need Order Date, Quantity, Unit price USD, Customer Key and Order Number- all these fields are available in Sales, Products and Customers tables. Therefore, I have uploaded these three tables and merged them to get the final table for analysis.

**Dataset Link	**

https://mavenanalytics.io/data-playground?search=Global%20Electronics%20retailer

**Tool Used**: Google Colab

**Process**

Step 1: Importing the python libraries and uploading the CSV files 

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/ef5a3384-a924-463d-a5f5-90b728c8b7ff)

Uploading the Sales table first and then merging Products and Customers table with it.

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/45a43f88-29aa-4804-b21e-077bb709c7d7)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/db5a8f4f-aaec-492e-accd-72bc97936517)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/2487f6af-7acc-4d22-985e-7494d3b2552a)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/5e353de5-5d6e-418d-ae08-2bbd139dc206)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/6384aebc-2fdc-4140-82bf-ca976dd1a6ca)

Note that, there are no null values in the dataset (except Delivery Date).

Step 2: Taking the required fields for analysis:

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/90c3f3f5-033e-4775-9b0b-7ad8db9c76e4)

Step 3: Data Exploration

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/91d5c884-7e05-4fdb-b429-0fe864a86c13)

3.1. Changing the data type of Order Date column

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/9aecbbbc-1b8d-4438-9a87-74160b3d2056)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/7d8658da-5476-4c8e-b1d0-d11443a1dd50)

3.2. Changing the Unite Price USD column to make it of float data type

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/c4f1acd1-6bd0-434b-990c-041d0d9e59b2)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/a2d1eca3-db95-4264-bb77-4477237e4f96)

3.3. Descriptive Statistics

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/a6b14ccd-6b6d-4fda-a46c-ec0e0b9ec9ac)

Note that there is no negative or zero quantity or price in the dataset.

Step 4: Calculating Recency, Frequency and Monetary fields

4.1. Using Quantity and Unit Price USD to calculate the Amount field for monetary.

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/91e2b144-5eab-4f05-bdd0-c083d2154da2)

4.2. Calculating the Frequency field and merging them to form the final RFM table

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/2f97e491-ecbb-4645-876a-f4c695edc144)

4.3. Calculating the Max Order Date to get the difference between the Max Order data and Order Dates for each Order to find the Recency

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/6ed2a718-c9d9-4aff-9549-7ad605a478ac)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/b4b10d9e-0eb6-496d-9180-24ce5802c9f1)

Then Merging Recency field with the existing RFM table

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/f4cc5461-4aab-4341-9be2-b86f629564a1)

Step 5: Checking for Outliers in the RFM table and removing the same

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/ed166486-59b6-42fa-96cb-23c3b1ed3c36)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/7a4d2c1f-aa4e-4f9b-b585-e47cd9e0ae9d)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/e2420e1c-faeb-4585-a3c5-6916db3d3fbb)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/d29f29b4-5be3-4cbe-a0e2-9e5a506dfffe)

Step 6: Scaling the fields of the RFM table

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/2a8b0f14-2610-48de-ba7a-4163b35cf625)

Step 7: Checking the Clustering Tendency of the dataset using Hopkins statistics

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/4e56c914-b4e0-4fed-9cf9-360124b12249)

I used a pre-defined function for calculating Hopkins Statistics https://github.com/prathmachowksey/Hopkins-Statistic-Clustering-Tendency  

Here, the value of H is higher than 70% and thus we can say the dataset have significant clusters.

Step 8: Elbow Curve and Silhouette analysis to find optimum number of clusters

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/af1cafea-bd5a-44e1-959f-1a41664129ef)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/1e1ae4bf-2b6e-4245-a128-427cb5f12503)

I am using 3 clusters for this analysis.

Step 9: K-means Clustering

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/907f7fc6-ad01-45fa-bc48-4211ca31eab0)

Step 10: Visualization to understand the clusters

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/ee90f1ee-eb95-4c28-b446-1d4243aa40c1)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/3d967b95-0b38-48de-a2db-36954ab446c5)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/810efd41-473e-46cc-8bdc-8e2d55ee3f8d)

![image](https://github.com/Tanusree1997/K-means-Clustering-of-retail-customers/assets/164666871/e684aaa9-6590-4bcc-bde2-b98ffb17acbf)

**Findings**

Cluster 1: Low Spending, not frequent but recent customers.

Cluster 2: High Spending, frequent but not recent customers.

Cluster 3: Low spending, not frequent and not recent customers.

Clusters 1 and 2 have strong potential to become the top customer segments for the Global Electronics retailer, provided targeted marketing strategies are implemented to retain them. In contrast, Cluster 3 consists of customers who are likely churned or lost. Therefore, the company should prioritize retaining customers in Clusters 1 and 2 through effective marketing efforts.




