# kbs_FinalProject
Group Name - Cartilage

Members: Vamsi Pogula - vpogula@uncc.edu Sayan Bhattacharya - sbhatt11@uncc.edu Mohammad Turab Ali - mohamma@uncc.edu

Dataset - https://www.kaggle.com/c/ga-customer-revenue-prediction/data

Research Question: We used customer data from Google’s Merchandise Store (G-Store) available on Kaggle to derive essential insights to help marketing teams make better use of their budgets. Specifically, we wish to aid a firm to use their data as a guiding tool for decision-making. To help G-Store marketing teams to take actionable operational changes by knowing the current business trend, We will be analyzing a Google Merchandise Store customer dataset to predict revenue per customer and identifying the features which are influencing most in revenue generation.

Data Size: This data set contains user transactions from August 1st, 2016 to April 30th, 2018 with 1708337 rows and 13 columns.

Domain: fullVisitorId- A unique identifier for each user of the Google Merchandise Store. The only way we can identify the user in the dataset. channelGrouping - The channel via which the user came to the Store. date - The date on which the user visited the Store. device - The specifications for the device used to access the Store. geoNetwork - This section contains information about the geography of the user. socialEngagementType - Engagement type, either "Socially Engaged" or "Not Socially Engaged". totals - This section contains aggregate values across the session. trafficSource - This section contains information about the Traffic Source from which the session originated. visitId - An identifier for this session. This is part of the value usually stored as the _utmb cookie. This is only unique to the user. For a completely unique ID, you should use a combination of fullVisitorId and visitId. visitNumber - The session number for this user. If this is the first session, then this is set to 1. visitStartTime - The timestamp (expressed as POSIX time). hits - This row and nested fields are populated for any and all types of hits. Provides a record of all page visits. customDimensions - This section contains any user-level or session-level custom dimensions that are set for a session. This is a repeated field and has an entry for each dimension that is set.

Pre-Processing : Flattening JSON columns: Columns such as device, geoNetwork, totals, trafficSource were JSON columns. We have to flatten these columns. Handling Missing values: Columns with more than 70% of missing values will be removed. Remaining Numerical columns with Null values will be replaced with value ‘0’. Removing unique value columns : Columns with unique value in it were removed. These columns will be useless for modelling as there was no variation in the data. Data-type conversion: Some columns should be converted from float type to object. Handling Categorical Data: Some Categorical column values such as '(not set)', 'not available in demo dataset', '(not provided)', 'unknown.unknown', '/' in the categorical columns will be replaced with ‘nan’. Normalization: Some Numerical columns should be normalized to bring all the attributes on the same scale using Min-Max Normalization to avoid dilution in effectiveness of an equally important attribute on lower scale because of other attribute having values on larger scale.


User Dashboard:

The below dashboard shows the channel grouping by which the user came to the Store

![alt text](https://github.com/riemannzeta1191/kbs_FinalProject/blob/master/Images/Image2.png)

The below dashboard shows the device information

![alt text](https://github.com/riemannzeta1191/kbs_FinalProject/blob/master/Images/Image1.png)

The below dashboard shows the Histogram of log of visit numbers per session since per session data is also huge.
![alt text](https://github.com/riemannzeta1191/kbs_FinalProject/blob/master/Images/Image3.png)

Tentative plan for Analysis on GCP: We will use PySpark and Jupyter notebook for pre-processing and showing analysis on the dataset. We will use BigQuery ML to build models for Multiple Linear Regression, K-Nearest Neighbours and Random Forest Regression. After evaluating the results on those models, we will select the model which is more accurate. We will use Visual Studio on GCP to do Exploratory Data Analysis and build Dashboards.


Research Citation:

1) Predictive analytics using big data for increased customer loyalty: Syriatel Telecom Company case study
Wissam Nazeer Wassouf, Ramez Alkhatib, Kamal Salloum and Shadi Balloul 

2)Machine-Learning Techniques for Customer Retention: A Comparative Study,Sahar F. Sabbeh

3)Analysis of Customer Churn prediction in LogisticIndustry using Machine Learning
Pradeep B, Sushmitha Vishwanath Rao and Swati M PuranikAkshay Hegde
