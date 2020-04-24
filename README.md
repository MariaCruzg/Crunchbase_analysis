# Crunchbase_analysis
With Crunchbase Data, developers can incorporate the latest industry trends, investment insights, and rich company data right into their applications. The purpose of this notebook is to try out a few algorithms for classification problem. 

We will start with some pre processing (scanling the data, basically) and then cover the following algorithms: Random Forest, XGBoost, Decision Tree and Keras Sequential model. For each one, We will compute the model accuracy, the Mean Absolute Error, the Mean Squared Error and the Root Mean Squared Error.
### Define the Problem: 
The company status are given the interesting challenge would be discovered if the investments and other criteria help company to be an operating / closed / acquired stage.

For this project, the problem statement is given to us on an open dataset, develop an algorithm to classify the status of the companies who has participated on investments' series from 2012 to 2017. 

 ### Gather the Data: 
The dataset is also given to us by the open dataset on:https://www.crunchbase.com/hub/database-startups
### Prepare Data for Consumption:
The normal processes in data wrangling, such as data architecture, governance, and extraction are out of scope. Thus, only data cleaning is in scope.  For this step we have employed some libraries to removing special characters and Database normalization. We will use the popular scikit-learn and teras libraries to develop our machine learning algorithms. In sklearn, algorithms are called Estimators and implemented in their own classes. For data visualization, we will use the matplotlib and seaborn library
### Perform Exploratory Analysis:
This is the meet and greet step. Get to know your data by first name and learn a little bit about it. What does it look like (datatype and values), what makes it tick (independent/feature variables(s)), what's its goals in life (dependent/target variable(s)). We started with the status of the company. 
 The graph shows the percent of each state. 86% of the companies are operating, 7.7% were acquired and 5.4% were closed.
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Statup%20Companies.png)
 > Following the analysis we describe the market of the companies. 
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/market.png)
 The most popular category is  about Software & Mobile, It maybe because these 2 categories are easily to scalable ?. The next variable to analize is relative to founding in usd.  
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/distributionoffoundinf.png)
 To undestand the problem and the numbers we will highlight the unicorns comanies as UBER, Alibaba,Cloudera and Facebook
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/unicornios.png)
### Model Data: 
Our principal objective is understood how the category and the founding affect  the status'company. We will convert categorical data to dummy variables for mathematical analysis. There are multiple ways to encode categorical variables; we will use the sklearn and pandas functions. In this step, we will also define our x (independent/features/explanatory/predictor/etc.) and y (dependent/target/outcome/response/etc.) variables for data modeling.

### Validate and Implement Data Model:
When it comes to data modeling, the beginner’s question is always, "what is the best machine learning algorithm?".  We will compare the accuracy, the  Mean Absolute Error and the  Root Mean Squared Error. 
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Comparison_model.png)
it's important we use a different subset for train data to build our model and test data to evaluate our model. *Model Performance with Cross-Validation* (CV) is basically a shortcut to split and score our model multiple times, so we can get an idea of how well it will perform on unseen data.
![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Captura%20de%20Pantalla%202020-04-23%20a%20la(s)%2019.25.44.png) 
In addition to CV, we used a customized sklearn train test splitter, to allow a little more randomness in our test scoring. Below is an image of the default CV split.


## Conclusion 
This notebook explored 4 basic machine learning algorithms. In the majority of them, the accuracy was higher in the training dataset, as expected. In the ones it was lower, the difference in not significant. The accuracy for those cases should be evaluated with a cross validation and not only with a single fold.  This dataset is very simple, so maybe we cannot note significant improvement in the algorithms.
Iteration one of the Data Science Framework, seems to converge on 0.86 submission accuracy. Using the same dataset and different implementation of severals MLA (Random Forest, XGBoost, Decision Tree and Keras Sequential model) with tuning does not exceed the 0.85 submission accuracy. Interesting for this dataset, the Sequential model  had the best default submission score and with tuning achieved the same best accuracy score. 
