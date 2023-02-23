# Flu-shot-learning-predict-H1N1-and-seasonal-Flu-vaccines

### Data Cleaning and EDA 
- By utilising the median and knn imputer to fill in some columns that had 50% of the values missing, the data was biassed more in favour of one variable.
- Health Insurance had a scenario where more information was needed, with 0 denoting a lack of insurance and 1 denoting those who have it. So, post missing value imputation, all missing values are substituted with 1, which causes a critical bias in the medical domain. Hence, eliminating missing is thought to be the least significant bias as opposed to portraying a dataset with biassed data.
- Rest of the missing are filled via KNN imputer
- Categorical variables are converted into numerical variables via ordinal encoding.
- Given that every column contains a discrete variable, there are no outliers.

## Approach 1


### Feature selection 
- There are several feature selection approaches, including recursive feature elimination, which produced fewer features and less precision. As a result, Forward feature selection with Lightbgm as an estimator provided the best accuracy.

### Model Creation and selection  
- A feature selected using forward feature selection was trained using xgboost, random forest, catboost, and lightbgm, with catboost and xgboost providing the best accuracy.
- Although accuracy values are not satisfied, hyperparameter tweaking techniques like Random search cv, Generic algorithm, Hyperopt, and optuna are applied.
- When Y1 and Y2 are merged, these models provided less accurate results, resulting in a 2D array.

## Approach 2

### Feature selection 
- The optimal feature for both Y1 and Y2 is chosen using the forward feature selection technique; however, choosing different features for Y1 and Y2 makes deployment challenging.

### Model Creation and selection
- Instead of using multioutput functions during training, which some machine learning algorithms are not designed for, y1 and y2 are combined. As a result, y1 and y2 receive distinct training.
- As Y1 and Y2 were trained independently, accuracy was good.




