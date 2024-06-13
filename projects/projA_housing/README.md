## Housing 

### Introduction

This project explores what can be learned from an extensive housing dataset that is embedded in a dense social context in Cook County, Illinois.

In Project A.1, I perform some basic Exploratory Data Analysis (EDA) to understand the structure of the data. Next, I add a few new features to the dataset, while cleaning the data as well in the process.

In project A.2, I specify and fit a linear model to a few features of the housing data to predict house prices. Next, I analyze the error of the model and brainstorm ways to improve the model's performance. Finally, I delve deeper into the implications of predictive modeling within the Cook County Assessor's Office (CCAO) case study, especially because statistical modeling is how the CCAO valuates properties. Given the history of racial discrimination in housing policy and property taxation in Cook County, I consider the impacts of your modeling results as you work through this project - and think about what fairness might mean to property owners in Cook County.

### Project A.1

I have a provided dataset that consists of over 500,000 records from Cook County, Illinois, the county where Chicago is located. The dataset has 61 features in total; the 62nd is sales price, which you will predict with linear regression in the next part of this project.

The data are split into training and test sets with 204,792 and 68,264 observations, respectively, but we will only be working on the training set for this part of the project.

**Part 1**

I note observations of the dataset to understand the background before diving into a full-scale analysis.

**Part 2**

I build a linear regression model that predicts sales prices using training data but it's important to first understand how the structure of the data informs such a model. I make a series of exploratory visualizations and feature engineering in preparation for that prediction task.

**Part 3**

In this section, I implement a few feature engineering techniques.

### Project A.2

The dataset comes from the Cook County Assessor’s Office (CCAO) in Illinois, a government institution that determines property taxes across most of Chicago’s metropolitan area and its nearby suburbs. In the United States, all property owners are required to pay property taxes, which are then used to fund public services including education, road maintenance, and sanitation. These property tax assessments are based on property values estimated using statistical models that consider multiple factors, such as real estate value and construction cost.

In this section split the dataset into a training set and validation set. I use the training set to fit our model's parameters, and I use the validation set to evaluate how well our model will perform on unseen data drawn from the same distribution.








