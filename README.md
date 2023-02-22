# Flu-shot-learning-predict-H1N1-and-seasonal-Flu-vaccines

### Data Cleaning and EDA 
- By utilising the median and knn imputer to fill in some columns that had 50% of the values missing, the data was biassed more in favour of one variable.
- Health Insurance had a scenario where more information was needed, with 0 denoting a lack of insurance and 1 denoting those who have it. So, post missing value imputation, all missing values are substituted with 1, which causes a critical bias in the medical domain. Hence, eliminating missing is thought to be the least significant bias as opposed to portraying a dataset with biassed data.
- Rest of the missing are filled via KNN imputer
- Categorical variables are converted into numerical variables via ordinal encoding.
- Given that every column contains a discrete variable, there are no outliers.



