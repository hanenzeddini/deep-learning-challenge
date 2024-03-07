# Alphabet Soup Charity Funding Predictor

## Overview of the Analysis

The goal of this analysis is to aid Alphabet Soup, a nonprofit foundation, in selecting funding applicants with the highest potential for success. Utilizing a dataset containing over 34,000 organizations previously funded by Alphabet Soup, this project employs machine learning and neural networks to develop a binary classifier. This classifier aims to predict the likelihood of an applicant's success if funded, based on various features within the dataset.

### Dataset Features

- **Metadata Columns**: EIN (Employer Identification Number), NAME
- **Feature Columns**:
  - APPLICATION_TYPE: Type of funding application
  - AFFILIATION: Sector of affiliation
  - CLASSIFICATION: Government classification
  - USE_CASE: Funding use case
  - ORGANIZATION: Type of organization
  - STATUS: Active status
  - INCOME_AMT: Income classification
  - SPECIAL_CONSIDERATIONS: Special application considerations
  - ASK_AMT: Requested funding amount
- **Target Column**:
  - IS_SUCCESSFUL: Effectiveness of fund usage

## Results

### Data Preprocessing

- **Target Variable**: `IS_SUCCESSFUL` - Indicates the effectiveness of the money usage.
- **Feature Variables**: All the mentioned feature columns are used as inputs for the model.
- **Removed Variables**: `EIN` and `NAME` were excluded from the model as they serve identification purposes only and do not contribute to the outcome prediction.

### Compiling, Training, and Evaluating the Model

- **Model Structure**: The neural network model consisted of an input layer, two hidden layers, and an output layer. 
    - **Input Features**: Calculated based on the training data dimensions.
    - **Hidden Layers and Neurons**: The first hidden layer had 80 neurons, and the second hidden layer had 30 neurons. Both layers used the ReLU activation function for non-linearity.
    - **Output Layer**: Consisted of a single neuron using the sigmoid activation function, suitable for binary classification problems.
- **Performance Achievement**: The model did not achieve the desired target performance, reaching an accuracy of approximately 72.5%.
- **Performance Improvement Attempts**:
    - Utilized Keras Tuner for hyperparameter optimization, experimenting with various numbers of layers, neurons per layer, and activation functions.
    - Selected the best model configuration from Keras Tuner and conducted further training with 200 epochs.
    - Adjusted the train-test split to increase the training dataset size, changing the test size from 25% to 20%.

## Summary

The deep learning model developed for Alphabet Soup's funding prediction showed a moderate level of accuracy in predicting the success of funding applicants. Despite efforts to enhance the model's performance through hyperparameter tuning and adjustments in data partitioning, the model did not surpass the threshold of desired accuracy.

### Recommendation

For future efforts to improve classification accuracy, it is recommended to do feature engineering, data preprocessing and checking the distribution of data which could uncover more insights and improve model performance.

