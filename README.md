# Crunchbase_analysis
With Crunchbase Data, developers can incorporate the latest industry trends, investment insights, and rich company data right into their applications. The purpose of this notebook is to try out a few algorithms for classification problem. We will start with some pre processing (scanling the data, basically) and then cover the following algorithms: Random Forest, XGBoost, Decision Tree and Keras Sequential model. For each one, We will compute the model accuracy, the Mean Absolute Error, the Mean Squared Error and the Root Mean Squared Error.
### Define the Problem: 
For this project, the problem statement is given to us on a open dataset, develop an algorithm to classify the status of the 
companies who has participated on investments series from 2012 to 2017.  The investments series at a company level are given. The company status are given  the interesting challenge would be discover if the investments and other criteria help company to be a operating / closed / acquired stage
 ### Gather the Data: 
The dataset is also given to us by the open dataset on:https://www.crunchbase.com/hub/database-startups
### Prepare Data for Consumption:
The  normal processes in data wrangling, such as data architecture, governance, and extraction are out of scope. Thus, only data cleaning is in scope.  For this step we have employed some libraries to removing special characters and Database normalization. We will use the popular scikit-learn and teras libraries to develop our machine learning algorithms. In sklearn, algorithms are called Estimators and implemented in their own classes. For data visualization, we will use the matplotlib and seaborn library
### Perform Exploratory Analysis:
This is the meet and greet step. Get to know your data by first name and learn a little bit about it. What does it look like (datatype and values), what makes it tick (independent/feature variables(s)), what's its goals in life (dependent/target variable(s)). We started with the status of the company. 
> The graph show the percent of each state. 86% of the companies are operating, 7.7% were aquaried and 5.4% were closed. 

![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Statup%20Companies.png)
 > Following the analysis we describe the market of the companies. 
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/market.png)
> The most popular category is  about Software & Mobile, It maybe because these 2 categories are easily to scalable ?. The next variable to analys is founding.  
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/distributionoffoundinf.png)
> To undestand the problem and the numbers we will highlight the unicorns comanies as UBER, Alibaba,Cloudera and Facebook
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/unicornios.png)
### Model Data: 


### Validate and Implement Data Model:
## Conclusion 
This notebook explored 6 basic machine learning algorithms. In the majority of them, the accuracy was higher in the training dataset, as expected. In the ones it was lower, the difference in not significant. The accuracy for those cases should be evaluated with a cross validation and not only with a single fold. Using cross validation will probably result in higher accuracy for all algorithms. This dataset is very simple, so maybe we cannot note significant improvement in the algorithms.
