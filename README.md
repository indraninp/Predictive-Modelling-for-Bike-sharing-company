# Predictive-Modelling-for-Bike-sharing-company
Build a multiple linear regression model for the prediction of demand for shared bikes with the available independent variables by using Linear Regression method. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

## Introduction
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues and have decided to come up with a mindful business plan to be able to accelerate its revenue. In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people. They have planned this to prepare themselves to cater to the people's needs and stand out from other service providers and make huge profits.

Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands.

The model will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

## Project Description
The data is cleaned, wrangled and then Exploratory Data Analysis & Outlier treatment is performed using python and its libraries. The relationship between the target variable and the input variables, and multicollinearity between different numeric variables is explored. Univariate and Bivariate analysis is performed, and dummy variables for the categorical variables. To perform Data Modelling, the data is divided into Training and Testing data. The X (feature variables) and y (target variable) are determined and are scaled. Using RFE: Recursive feature elimination technique, selected the top 15 variables and a Linear Regression Model is built using the selected variables. 

Then we drop one variable at a time.The general rule of thumb to be followed for dropping variables is in this order:

   i) first drop the features with both high p-value(>0.05) and high VIF(>5) 

   If p-value and VIF are both not high (condition i is not satisfied) , then dropping preference is in the below order:

   ii) the feature with high p-value and low VIF
   iii) the feature with high VIF and low p-value

When dropping on the basis of VIF, we do not always drop just on the basis of high VIF alone. We might also need to consider other aspects, that is, look at the EDA analysis to see how the target variable and dependent variable are related, and use domain knowldege to decide which variable to drop and which to retain. As we drop variables one at a time, the p-values and VIF of all the variables will change as we rebuild our model aafter every drop.

In the final model, all the variables have a p-value which is less than the significance level of 0.05, and a VIF lower than 5 (low multicollinearity)
We then checked and validated the various assumptions of Regression are satisfied. The model is then used to predict on the Test set data. 
The R-Squared values of the train dataset and test dataset are comparable, hence our model will be able to predict well in the case of unseen data.
The equation of the best fitted line is found, using which we can get the top variables in predicting the demand for shared bikes, along with their coefficients.

## Technologies Used
Python

Libraries: pandas, numpy, matplotlib, seaborn, sklearn, statsmodel, scipy

Jupyter Notebook

## Results

From the final model, the top variables in predicting the demand for shared bikes, along with their coefficients are found. The R-squared and Adjusted R-squared values of our final model are 0.816 and 0.812 respectively. Thus approximately 81% of the variation of the dependent variable is explained by the model.  The overall model fit is significant,  all the predictors are statistically significant and have low multicollinearity.
