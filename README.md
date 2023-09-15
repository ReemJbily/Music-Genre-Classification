# Music Genre Classification project

### This repository is a team solution to the music genre classification competition on Kaggle.

### It is part of my training with SHAI for AI.

### The data set is available here and it is divided into train and test sets.

### The project went through different stages of machine learning life cycle.
# Project life cycle:
### 1-The big picture:
#### After collecting some information about the type of project we are working one, we found that it is an unbalanced multiclass classification problem related to classifying music genre #### based some important features.
### 2-Data explorination:
#### In this project we explored the train data set using numpy and panadas libraries.
#### for the train dataset, we found that:
#### Popularity column has 333 null values.
#### Key has 1609 null values.
#### Instrumentalness has 3541 null values.
#### for the test data, we found that:
#### Popularity column has 95 null values.
#### Key has 405 null values.
#### Instrumentalness has 836 null values.
### 3-Data Visualization:
#### For visualizing data, we used boxplots to detect outliers and their values, scatter plot to investigate the relation between variables and heatmap for features’ correlation.
#### Some insights we got after visualizing the train data using pandas, seaborn and matplotlib:
#### • only Popularity, Key and Instrumentalness columns have null values.
#### • There are some outliers but it did not affect the classification result.
#### • The relation between energy and loudness is expontential.
#### • The classes are unbalanced.
### 4-Preprocessing:
#### In order to make data more efficient for training the , we:
#### •	Removed all null values.
#### •	Removed all features not related to the problem.
#### •  Fixing unbalanced data by resampling both over and under.
#### •	Column transformation:
#### For numerical columns we used:
#### •	Simple Imputer(strategy=median).
#### •	CombinedAttributeAdder: to add the a new column.
#### •	StandardScaler: to scale the data for better training.
### 5-Select and train the model:
#### For this project, we selected seven models: Logistic regression Regression, K-Nearest neighbor, Random Forest, XGBoost Regressor, SGD classifier, Gradient boosting and #### stacking between random forest and gradient boosting.
### 6-Fine Tune the model:
#### For this stage we used random search on random forest and got that n_estimators =1000 is the best and on K-nearest neighbor and got k=29.
### 7-Evaluating models using:
#### 1- confusion matrix.
#### 2- accuracy score.
#### 3- precision.
#### 4- recall.
#### 5- f1 score.
### 8-Saving the results:
#### In this step predictions on the test set were performed using the chosen model, then results were saved as a csv file.
# Results:
#### the best result was given by stacking both random forest with 1000 estimators and gradient boosting with 300 estimators, max depth of 3 and learning rate equals 0.1.
