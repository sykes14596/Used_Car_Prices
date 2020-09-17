# Predicting Used Car Prices

The goal of this project was to be able to accurately predict the sale price of a range of used cars, as well as to practice skills and techniques learned through the completion of Jose Portilla's "Python for Data Science Bootcamp" on [Udemy](https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/learn/lecture/17739846?start=0). 

A wide range of models were implemented and the effect of scaling data was investigated. The most accurate model, based on its Root Mean Squared Error (RMSE), was a Random Forest Regressor trained and tested on the scaled version of the dataset. The model achieved an R2 score of 96.4% and a RMSE of £1858.

## Table of Contents

* [Technologies](#technologies)
* [Data Cleaning](#data_cleaning)
* [Exploratory Data Analysis](#exploratory_data_analysis)
* [Data Preprocessing](#data_preprocessing)
* [Model Building](#model_building)
* [Model Performance](#model_performance)
* [Conclusions](#conclusions)

## Technologies

This project was completed using a Jupyter Notebook with the following packages installed.


* Python: 3.7.7
* Numpy: 1.19.1
* Pandas: 1.1.0
* Seaborn: 0.10.1
* Scikit-Learn: 0.23.1
* Matplotlib: 3.2.2
* Tensorflow: 2.1.0
* Keras: 2.3.1

## Data Cleaning

Before exploring and analysing the data, there were certain data points that did not seem to be correct. There were vehicles within the dataset which had a recorded engine size of 0.0, some which had supposedly been registered in the future as well as other strange occurences. These data points were identified and removed from the dataset.

## Exploratory Data Analysis

I analysed the correlation between the numerical variables and our target variable. As well as this, I investigated the distribution of each numerical variable and observed significant amounts of skewness. I investigated the relationships between the categorical variables and the dependent variable. Some of the highlights of the EDA can be seen below.

![alt text](https://github.com/sykes14596/Used_Car_Prices/blob/master/Images/Correlation_Matrix.png "Correlation Matrix")
![alt text](https://github.com/sykes14596/Used_Car_Prices/blob/master/Images/manufacturer_boxplot.png "Manufacturer Boxplot")
![alt text](https://github.com/sykes14596/Used_Car_Prices/blob/master/Images/numerical_variables_pairplot.png "Numerical Variables Pairplot")

## Data Preprocessing

The skewed variables were normalised by applying the logarithm to each value using the inbuilt Numpy function. The categorical variables were converted into numeric variables using dummy variables. Training and testing sets were created with a test size of 25%.

## Model Building

In total, eight different models were created. Five of these were implemented using the non-scaled dataset, with the remaining 3 being implemented on the scaled version. The scaling was completed using the Standard Scaler from within the Scikit-Learn library. The models implemented are shown below.

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Support Vector Regression
* MLP Regressor

## Model Performance

The models were analysed using 2 values. The first metric observed was the R2 score, which shows the amount of variance of the dependent variable explained by the model. The second metric utilised for analysis was the Root Mean Squared Error. Full results for each model implementation are shown below.

#### Non-Scaled Data Models

* Linear Regression: R2 Score = 90.6%, RMSE = £3008.
* Decision Tree Regressor: R2 Score = 93.7%, RMSE = £2460
* Random Forest Regressor: R2 Score = 96.4%, RMSE = £1870
* Support Vector Regression: R2 Score = 87.4%, RMSE = £3498
* MLP Regressor: R2 Score = 93.7%, RMSE = £2472

#### Scaled Data Models

* Decision Tree Regressor: R2 Score = 93.7%, RMSE = £2489
* Random Forest Regressor: R2 Score = 96.4%, RMSE = £1859
* Support Vector Regression: R2 Score = 94.3%, RMSE = £2354


## Conclusions

I was able to acheive relatively good model performance within this project. It can be see that scaling the data has differing effects on model performance based on the type of model implemented. Support vector regression showed a significant improvement as a result of using scaled data.

Finally, I was able to further practice and develop my data science techniques and produce a thorough explanation of my methods within the Jupyter Notebook.