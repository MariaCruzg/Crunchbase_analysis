# Crunchbase_analysis

 The objective of this project is to **understand the factors that influence the company status in startups** in North America. With the [Crunchbase Data]((https://www.crunchbase.com/)), developers can incorporate the latest **industry trends**, **investment insights**, and **rich company data** right into their applications.  We have clustered the companies into 3 sets: operating, acquired and closed. In order to solve the clustering problem  classification algorithms have been employed. Classification algorithms map a set of attribute values to a categorical target value, represented by a class attribute.

We will start with some **pre-processing** (scanling the data, basically) and then cover the following algorithms: `Random Forest`, `XGBoost`, `Decision Tree` and `Keras Sequential model`. 

For each algorithm, We will compute the **model accuracy**, the **Mean Absolute Error**, the **Mean Squared Error** and the **Root Mean Squared Error**.

## Define the Problem:

It's difficult to know in which company to invest, so this project wants to have a simple visualization of the data to make the investors easier to make the decision. The purpose of this notebook is to try out a few algorithms for solving classification problems.  The algorithm presented **classify** the **status** of the **companies** who has participated on **investments**' series from 2012 to 2017. 

## Gather the Data:

The dataset is also given to us by the open dataset on [Crunchbase](https://www.crunchbase.com/)

The columns of this set are:

| Column            | Dtype   |
| -- | -- |
| permalink         | object  |
| name              | object  |
| homepage_url      | object  |
| category_list     | object  |
| market            | object  |
| funding_total_usd | int64   |
| status            | object  |
| country_code      | object  |
| state_code        | object  |
| region            | object  |
| city              | object  |
| funding_rounds    | int64   |
| founded_at        | object  |
| founded_month     | object  |
| founded_quarter   | object  |
| founded_year      | float64 |
| first_funding_at  | object  |
| last_funding_at   | object  |

## Prepare Data for Consumption:

The normal processes in **`data wrangling`**, such as **data architecture**, **governance**, and extraction are out of scope.

- For this step we have employed some libraries to removing special characters and **Database normalization**.
- We will use the popular `scikit-learn` and `teras` libraries to develop our **machine learning algorithms**.
- For **data visualization**, we will use the `matplotlib` and `seaborn` library

## Perform Exploratory Analysis:

Data analysis is the step to describe and visualize the information. Datatype and values are described. We define  the features variables (x) and find the target variables (y).

The graph shows the percent of each state. **86**% of the companies are **operating**, **7.7%** were **acquired** and **5.4%** were **closed**.

[![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/Statup%20Companies.png)]
### Top startups in market

> Following, we describe the **market of the companies**.
>
> [![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/market.png)]

### Distribution of total funding


> The most popular category is **Software & Mobile**, It maybe because these 2 categories are easily to scalable ?. The next variable to analize is relative to **founding in usd**.
> 
> [![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/distributionoffoundinf.png)](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/distributionoffoundinf.png)

### Where are the biggest companies?

> To undestand the problem and the numbers we will highlight the unicorns companies as UBER, Alibaba, Cloudera and Facebook
> 
> [![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/unicornios.png)](https://github.com/MariaCruzg/Crunchbase_analysis/blob/master/images/unicornios.png)

## Model Data:

Our main objective is to understand how the category and the founding affects the status of the company. 

We will convert `categorical data` to -> `dummy variables` for **mathematical** analysis. There are multiple ways to encode categorical variables; we will use the `sklearn` and `pandas` functions. In this step, we will also define our **`x`** (independent) and **`y`** (dependent) variables for data modeling.

## Validate and Implement Data Model:

When It comes to **data modeling**, the beginner’s question is always, "**what is the best machine learning algorithm?**". We will compare the accuracy, the Mean Absolute Error and the Root Mean Squared Error.

[![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/Comparison_model.png)]

It's important to use a `different subset` for train data to build our model and test data to evaluate our model. **Model Performance with Cross-Validation** (CV) is basically a shortcut to split and score our model multiple times, so we can get an idea of how well it will perform on unseen data.

[![img](https://github.com/MariaCruzg/Crunchbase_analysis/raw/master/images/Captura%20de%20Pantalla%202020-04-23%20a%20la(s)%2019.25.44.png)]

In addition to CV, we used a customized `sklearn` train test splitter, to allow a little more **randomness** in our *test* scoring. Below is an image of the default CV split. 
The results of the MLA are the following:

| MLA | accuracy|standard deviation| 
| --                   | --     |--|
| Random_forest        | 84.6%  |0.03% |
|Decision Tree         | 85.8%  |0.002%|
| XGBoost              | 85.8%  |0.005%|
| Sequential           |  86.7%   |0.03% |

## Conclusion

Within the data We can conclude that the most important variables to get acquired are related to fundraising and the tech industry, so If one company get a big fundraising and It's software related It's highly provable to get acquired and could be a good idea to invest in It.

The top 5 of the variables most significant are: 

| feature           | importance |
| ----------------- | ---------- |
| funding_total_usd | 0.525      |
| funding_rounds    | 0.054      |
| Curated Web       | 0.022      |
| Public Relations  | 0.008      |
| Software          | 0.008      |
| Web Hosting       |   0.007    |
