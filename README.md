# Predicting Sales Values per Store 
## An analysis of the properties of Products and Stores to predict the Sales Values of the Stores 

**Author**: Warren Howarth

### Business problem:

A retailer has approached us to analyse the different characteristics of both their stores and their products which will help increase the sales in their stores. In essence they are asking us to develop and improve their sales mix in each type of store in order to increase their sales volumes throughout their business.


### Data:
 - Source

The client has provided us with the data in a csv format, and here is a description of the data features

![Dictionary](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=nZU9VvZNQKyu&line=4&uniqifier=1)

 - Format

There are 8523 rows of data and 12 columns, 7 of which are categorical and 5 numerical

![Data formats](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=BdJ4oHYOVHlj&line=1&uniqifier=1)

- Cleaning

![ItemFatContent](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=HI2yAGJyRrZs&line=1&uniqifier=1)

The feature 'Item_Fat_Content' was badly characterised, and was amended as follows:

1. The 'LF' classification was changed to 'Low Fat'
2. The 'reg' classification wsa changed to 'Regular'
3. The 'low fat' classification wsa changed to 'Low Fat'

- Duplicates

There were no duplicates in the data

- Missing Values

![MissingValues](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=y_74I4bZdh1G&line=1&uniqifier=1)

There were 1463 (17.17%) missing values in the 'Item_Weight' feature, and these were replaced with the mean (average) of the feature.

There were 2410 (28.28%) missing values in the 'Outlet_Size' feature, and these were replaced with the term 'NA'.

## Methods
After a further analysis of the data, it was determined that the following features should be ignored:

- Item_Identifier - this feature has 1559 unique values, and it was considered to be of little value in the analysis

- Outlet_Establishment_Year - this feature was also deemed to have no relevance to the analysis

In fact, when we examine the correlation between the numerical features and the sales value, there are only 2 features that seem to have a correlation coefficient of any significance:
1. Item_MRP at 0.57
2. Item_Visibility at (0.13)

![Correlation Heatmap](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=Hw3ZBog_MKwE&line=1&uniqifier=1)

An analysis was also done against the categorical features, some of the results will be discussed below.

## Results

#### Outlet Identifier
![Outlet Identifier](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=tOc99b2V4lyu&line=1&uniqifier=1)

Feature Observations

- Based on your business understanding, would you expect this feature to be a predictor of the target?
-- Yes

- Does this feature appear to be a predictor of the target?
-- Yes
> The median of the sales figures vary significantly between the different outlets

#### Outlet Type
![Outlet Type](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=jEoB19V6-aku&line=1&uniqifier=1)

Feature Observations

- Based on your business understanding, would you expect this feature to be a predictor of the target?
-- Yes

- Does this feature appear to be a predictor of the target?
-- Yes
> This feature has significant differences in mean and distribution between the outlets

### Item Visibility
![Item Visibility](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=vbzSghc7FRJI&line=1&uniqifier=1)

Feature Observations

- What type of feature is it? (Categorical (nominal), ordinal, numeric)
-- Numeric

- How many null values? What percentage? What would you do with the null values (drop the rows? drop the column? impute? if impute, with what?)
-- 0 null values.
-- No need to impute

- Is the feature constant or quasi-constant?
-- No, the highest percentage is 6.17%

- What is the cardinality? Is it high?
-- Cardinality is not taken into consideration for numeric features

- Would we know this BEFORE the target is determined?
-- Yes.

- Is there a business case/understanding reason to exclude based on our business case?
-- No, the visibility of a food item will impact the sales

![Item Visibility](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=AscrI9JBFRJJ&line=1&uniqifier=1)

Feature Observations

Based on your business understanding, would you expect this feature to be a predictor of the target?

Yes
Does this feature appear to be a predictor of the target?

Yes, but with a negative correlation, which is opposite of what I would expect

### Item MRP
![Item MRP](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=CtTZ5mZGFRm4&line=1&uniqifier=1)

Feature Observations

- What type of feature is it? (Categorical (nominal), ordinal, numeric)
-- Numeric

- How many null values? What percentage? What would you do with the null values (drop the rows? drop the column? impute? if impute, with what?)
-- 0 null values.
-- No need to impute

- Is the feature constant or quasi-constant?
-- No, the highest percentage is 0.08%

- What is the cardinality? Is it high?
-- Cardinality is not taken into consideration for numeric features

- Would we know this BEFORE the target is determined?
-- Yes.

- Is there a business case/understanding reason to exclude based on our business case?
-- No, the price will impact the sales

![Item MRP](https://colab.research.google.com/github/wmhowarth/Prediction-of-Product-Sales/blob/main/Project1_Part5.ipynb#scrollTo=DBA5Pb0YFRm4&line=1&uniqifier=1)

Feature Observations

- Based on your business understanding, would you expect this feature to be a predictor of the target?
-- Yes

- Does this feature appear to be a predictor of the target?
-- Yes, there is a strong positive correlation

## Model

Three models were applied to the data:
1. Linear Regression Base Model
2. Random Trees Model
3. Tuned Random Trees Model

I will use the Tuned Random Trees model for the purpose of solving this problem. This is because it is able to predict the sales values with more accuracy than the others.

The metrics:
1. Linear Regression:



Refer to the metrics to describe how well the model would solve the business problem

## Recommendations:

More of your own text here


## Limitations & Next Steps

More of your own text here


### For further information


For any additional questions, please contact **email**
