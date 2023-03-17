# Neural_Network_Charity_Analysis
## Overview
In this analysis, we use neural networks to classify whether a charity funded by Alphabet Soup will be successful or not. We use TensorFlow to train four different neural networks to attempt to gain better accuracy at solving this problem. 

## Results
Our data, from Alphabet Soup was preprocessed in the following ways:
- Target variable: *IS_SUCCESSFUL* 
- Feature Variables: *AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT*
- Neither (Variables to be removed before analysis) - *EIN, NAME*

Many of these variables were turned into usable, numerical data using ONEHOTENCODER from SciKitLearn.

Once preprocessed, four different neural network models were used to try and achieve 75% accuracy. Their details are shown below:
- Model 1
  - 2 hidden layers
  - 5 neurons per hidden layer
  - "relu" activation function
  - Accuracy: 73.0%

In between model 1 and model 2, a random forest classifier was used to get rid of columns that were of little importance to the final classification.

- Model 2
  - 3 hidden layers
  - 10 neurons per hidden layer
  - "relu" activation function
  - Accuracy: 72.9%
- Model 3
  - 3 hidden layers
  - 30 neurons per hidden layer
  - "tanh" activation function
  - Accuracy: 73.0%
- Model 4
  - 3 hidden layers
  - 70 neurons per hidden layer
  - "relu" activation function
  - Accuracy: 73.0%

## Summary
None of these models were successful at reaching our goal of 75% accuracy. In fact, all of the optimizing techniques we used (getting rid of features that were of little importance, increasing number of hidden layers, increasing number of neurons per hidden layer, and changing activation function) all were unsuccessful at increasing our accuracy at all. One possibility is that some of these optimization techniques overfitted the training data. One potential different model might try to vary the ratio of training data to testing data. Additionally, we might look at the ratio of successful to unsuccessful charities and if they are unbalanced, try to overfit or underfit the data.
