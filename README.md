# Neural Network Charity Analysis

## Overview of the Analysis

The following analysis was completed for a hypothetical client, Alphabet Soup. This client, a philanthropic foundation dedicated to helping other organizations, was seeking to develop a model that predicts whether a receiving organization will use the funds donated to them effectively. 

This analysis used historical data from 34,000 organizations that have been the recipients of donations from Alphabet Soup. Using machine learning and neural networks, this dataset was used to create a binary classifier that is capable of predicting whether applicants will be successful if funded. 

## Results

### Data Preprocessing

_What variable(s) are considered the target(s) for your model?_

  - The target variable for this analysis is the IS_SUCCESSFUL variable, which is a binary classified for whether the money was used effectively.
  
_What variable(s) are considered to be the features for your model?_

  - APPLICATION_TYPE
  - AFFILIATION	CLASSIFICATION	
  - USE_CASE	ORGANIZATION	
  - STATUS	
  - INCOME_AMT	
  - SPECIAL_CONSIDERATIONS	
  - ASK_AMT
 
_What variable(s) are neither targets nor features, and should be removed from the input data?_

  - At the very beginning of data pre-processing for this analysis, the identification columns, EIN & NAME, were removed from the input data. 

### Compiling, Training, and Evaluating the Model

_How many neurons, layers, and activation functions did you select for your neural network model, and why?_

  - In an attempt to optimize the model, I selected 3 layers:
      1. 90 neurons
      2. 35 neurons
      3. 10 neurons
  - Any additional layers and neurons beyond what I selected did not yield any significant performance in model performance and were therefore omitted. 
  - The activation function selected for all 3 hidden layers was "ReLu" and "Tanh" was selected for the output layer. These activation functions yielded the highest accuracy scores. 

_Were you able to achieve the target model performance?_
  - No.
  
_What steps did you take to try and increase model performance?_
  - Removed an additional variable, ASK_AMT, that was neither a target or a feature.
  - Bucked the noisy variables from the input features.
  - Added additional neurons to the hidden layers.
  - Added additional hidden layers. 
  - Changed the output layer's activation function for optimization.
  - The model's weights are saved every 5 epochs.
  - The results are saved to an HDF5 file.

### Summary

Overall, the Neural Network yielded a 72% accuracy in predicting whether Alphabet Soup's donation will be used successfully by the fund recipient. This accuracy maintains consistency in predicting both failure and success. Because of this, I do think that it is a relatively successful model that could be used for future predictions of this nature. 

As a recommendation for future optimization of this model, I would advise leveraging a method that creates a new Sequential model with hyperparameter options. This would allow Kerastune to select which activation function is optimal to use at each hidden layer in the neural network in addition to the number of hidden layers and neurons that are optimal to run an accurate model. 

