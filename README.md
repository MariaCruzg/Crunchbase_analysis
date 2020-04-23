# Crunchbase_analysis
#Introduction*
The purpose of this notebook is to try out a few algorithms for classification problems. I will start with some pre processing (scanling the data, basically) and then cover the following algorithms: Random Forest, XGBoost, Decision Tree and keras. For each one, I will compute the model accuracy both for the test and train dataset.

#Information 
The investments series at a company level are given. The company status are given - the interesting challenge would be discover if the investments and other criteria help company to be a operating / closed / acquired stage

![](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/Statup%20Companies.png)

*Conclusion*
This notebook explored 5 basic machine learning algorithms. In the majority of them, the accuracy was higher in the training dataset, as expected. In the ones it was lower, the difference in not significant. The accuracy for those cases should be evaluated with a cross validation and not only with a single fold. Using cross validation will probably result in higher accuracy for all algorithms. This dataset is very simple, so maybe we cannot note significant improvement in the algorithms.
