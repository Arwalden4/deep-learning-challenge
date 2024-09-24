# deep-learning-challenge
## Background 
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

## Results and Analysis
## Overview
This analysis will deal with the neural network model which was set up to complete the challenge instructions. Two models were preprocessed, compiled and evaluated to predict whether a charity would be successful according to the data provided in the starter file. The second model attempted to optimize the features of the first by making several adjustments to do so. This analysis will assess the features of the optimized model which did achieve a higher accuracy score than the other model. 
### Data Preprocessing
* The target variable for the neural network model is "IS_SUCCESSFUL", and so our accuracy reflects how reliably it can predict this value.
* The feature variables include: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT
* The removed variables included EIN, SPECIAL_CONSIDERATIONS, and STATUS. These columns either offered little information to the model or did not show much or any variation in the dataset. For example, STATUS only had 5 '0' values in the whole file. These can therefore be deemed not helpful so that we may focus on the other information available.
### Compiling, Training, and Evaluating the Model
* The optimized model I created had three dense layers and one output layer consisting of descending numbers of neurons in each. The first hidden layer had 100 nodes, the second 30, and the last ten.
![Charity_Optimization](https://github.com/user-attachments/assets/27da005f-8f4c-4984-8cc9-8816e7b94879)
