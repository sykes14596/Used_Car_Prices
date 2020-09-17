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

