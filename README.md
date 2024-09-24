# deep-learning-challenge
## Background 
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.

## Results and Analysis (Written Report)
## Overview
This analysis will deal with the neural network model which was set up to complete the challenge instructions. Two models were preprocessed, compiled and evaluated to predict whether a charity would be successful according to the data provided in the starter file. The second model attempted to optimize the features of the first by making several adjustments to do so. This analysis will assess the features of the optimized model which did achieve a higher accuracy score than the other model. 
### Data Preprocessing
* The target variable for the neural network model is "IS_SUCCESSFUL", and so our accuracy reflects how reliably it can predict this value.
* The feature variables include: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT
* The removed variables included EIN, SPECIAL_CONSIDERATIONS, and STATUS. These columns either offered little information to the model or did not show much or any variation in the dataset. For example, STATUS only had 5 '0' values in the whole file. These can therefore be deemed not helpful so that we may focus on the other information available.
### Compiling, Training, and Evaluating the Model
* The optimized model I created had three dense layers and one output layer consisting of descending numbers of neurons in each. The first hidden layer had 100 nodes, the second 30, and the last ten.
![Charity_Optimization](https://github.com/user-attachments/assets/27da005f-8f4c-4984-8cc9-8816e7b94879)
* Moreover, the attempts at optimization yielded an accuracy score of 78-79%, which exceeds the original threshold and shows that it reached target performance.
![Optimization_Results](https://github.com/user-attachments/assets/fc81de73-7456-4d4b-a206-c6d6edbf1d66)

* One important difference the optimized model makes is to bin the values according to NAME rather than CLASSIFICATION. This is because the organization name might have a stronger correlation with success if certain names show up more than once in the dataset, and so it would be reasonable that the model reflects higher accuracy as a result.
  * Two other columns were removed, SPECIAL_CONSIDERATIONS and STATUS, because of their lack of variation in the dataset. They are hardly any use in being able to better predict our target variable.
  * Furthermore, a third dense layer was added to increase the complexity of the network model.
  * The last change was to use different activation functions in the dense layers. The second, third, and output layers use sigmoid functions in defining and compiling the model.

### Summary
The tuned and optimized model yielded a higher accuracy score than the first neural network model with a score of 79% compared to ~73%. The optimization changes produced this result by eliminating columns not useful for predicting the target, increasing the complexity of the neural net, giving more parameters for the model to use, and implementing different activation functions in the dense layers. Though successful, there is room for improvement in this model and further investigation of this dataset as well as compiling other models might demonstrate a superior method to optimize it. One suggestion which occurred to me is using a random forest classifier model as a prediction method. One reason to believe the effectiveness of this process is that random forests generally train faster and require less tuning compared to neural networks, which can be more complex and time-consuming to optimize. Further, they can capture patterns in datasets which map its diversity, hinting toward possibly greater accuracy. They also do not require the sometimes extensive tuning of neural networks, which means they can train faster. They can also offer interpretability of data to understand those features that influence prediction values. Neural networks are much more opaque by comparison. For these reasons, we might discern the peculiar advantages of random forest classification to make better predictions about data.
