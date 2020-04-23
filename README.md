# Crunchbase_analysis
With Crunchbase Data, developers can incorporate the latest industry trends, investment insights, and rich company data right into their applications. The purpose of this notebook is to try out a few algorithms for classification problem.I will start with some pre processing (scanling the data, basically) and then cover the following algorithms: Random Forest, XGBoost, Decision Tree and Keras Sequential model. For each one, I will compute the model accuracy, the Mean Absolute Error, the Mean Squared Error and the Root Mean Squared Error.

# #A Data Science Framework
# # #Define the Problem: 
For this project, the problem statement is given to us on a open dataset, develop an algorithm to classify the startus of the 
companies who has participated on  investments series since 2012 to 2017.  The investments series at a company level are given. The company status are given  the interesting challenge would be discover if the investments and other criteria help company to be a operating / closed / acquired stage

# # # Gather the Data: 

![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Statup%20Companies.png)

# # # Prepare Data for Consumption:

# # # Perform Exploratory Analysis:
# # # Model Data: 

# # # Validate and Implement Data Model:
# #Conclusion 
This notebook explored 5 basic machine learning algorithms. In the majority of them, the accuracy was higher in the training dataset, as expected. In the ones it was lower, the difference in not significant. The accuracy for those cases should be evaluated with a cross validation and not only with a single fold. Using cross validation will probably result in higher accuracy for all algorithms. This dataset is very simple, so maybe we cannot note significant improvement in the algorithms.
