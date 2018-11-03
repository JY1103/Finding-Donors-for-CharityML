# Finding-Donors-for-CharityML

### 1. Installation
The libraries needed for this project are simply numpy, pandas and matplotlib. Moreover, the python 3.6.5 is used here.

### 2. Project Motivation
The purpose of the project is to model individuals' income using data collected from the 1994 U.S. Census. Specifically, the goal is to construct a model that accurately predicts whether an individual makes more than $50,000. It has greate value for non-profit organizations. Understanding an individual's income can help a non-profit better understand how large of a donation to request, or whether or not they should reach out to begin with. While it can be difficult to determine an individual's general income bracket directly from public sources, we can infer this value from other publically available features.

### 3. File Descriptions
* **README.MD**  <br/>
* **FindingDonorsforCharityML.ipynb**: <br/>
The notebook includes necessary codes for the project. <br/>
* **census.csv**: <br/>
The dataset for this project originates from the UCI Machine Learning Repository. The data here consists of small changes to the original dataset, such as removing the 'fnlwgt' feature and records with missing or ill-formatted entries. The detailed explaination of data can be found [here](https://archive.ics.uci.edu/ml/datasets/Census+Income) <br/>

### 4. Project Details
The project is dived into 4 parts. <br/>
**1. Data Exploration** <br/>
The data has 45222 records with 13 features. And, there are 24.78% of people earn more than $50000. <br/>

**2. Data Preprocess** <br/>
* After checking the distribution of all numerical features, 'capital-gain' and 'capital-loss' seem to be quite skewed. log function is applyied to remove skewness in these two features. <br/>
* All numerical features are normalized by MinMaxScaler. <br/>
* All catogorized features are converted into dummy vairables. <br/>
Finally there are 103 feature variables. <br/>

**3. Algorithm Application** <br/>
**Step 1:** Three candidate models are applied. They are Logistic Regression, Support Vector Machine and Gradient Boost Tree.<br/>
**Step2:** The performance results including training time, predicting time, accuracy score on train and test set and f-score on train and test set are evaluated to find the best model. It seems that Gradient Boost Tree is the best model as it provides relatively high accuracy with relatively low computational time. <br/>
**Step 3:** Different parameter sets are used to tune the chosen Gradient Boost Tree model to find the best model. Finally, the best model can achieve accuracy score 0.8681 and F-score 0.7463 on testing data. <br/>

**4. Insight Generation** <br/>
Finally, top 5 features which are most important at predicting individuals' income are found. They are capital-gain, capital-loss, age, hours-per-week and martial-status. These features can be served as top indicators for non-profits to figure out how much potantial donators can earn.

### 5. Authors
Jiayi Chen

