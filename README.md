# Deep Learning Challenge

## Project Overview

The objective of this project was to explore the feasibility of constructing a predictive model using neural networks (NN) to evaluate the eligibility of applicants seeking funding from the nonprofit organization Alphabet Soup.

We leveraged a comprehensive dataset provided by Alphabet Soup's business team, comprising information from over 34,000 previously funded organizations. This dataset included crucial metadata for each organization, such as application type, industry affiliation, government classification, funding purpose, organization type, status, income, requested amount, and specific considerations for each application. The primary focus was on a binary success metric indicating the effective utilization of funds, as documented in the dataset.

## Methodology

Following established protocols, the dataset was split into training and testing sets using the `train_test_split` function. To enhance model performance, categorical features were encoded using `pd.get_dummies()`, ensuring an accurate representation of the data. Additionally, feature scaling was applied to account for variations in the raw weights of individual features.

### Variables

**Target Variable:**
- IS_SUCCESSFUL

**Feature Variables:**
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT

**Excluded Variables:**
- EIN
- NAME

### Model Architecture

Our initial model architecture was designed as follows:

- **First Hidden Layer:** 80 neurons with relu activation function
- **Second Hidden Layer:** 20 neurons with relu activation function
- **Output Layer:** 1 neuron with sigmoid activation function

The model underwent training over 100 epochs to optimize its performance.

### Initial Model

- **First Hidden Layer:** 50 neurons, relu activation
- **Second Hidden Layer:** 20 neurons, relu activation
- **Output Layer:** 1 neuron, sigmoid activation
- **Training Epochs:** 100

### Optimized Model

- **First Hidden Layer:** 100 neurons, relu activation
- **Second Hidden Layer:** 50 neurons, relu activation
- **Third Hidden Layer:** 20 neurons, sigmoid activation
- **Fourth Hidden Layer:** 10 neurons, sigmoid activation
- **Output Layer:** 1 neuron, sigmoid activation
- **Training Epochs:** 100

## Summary

In both the original and optimized models, achieving an accuracy rate exceeding 73% in predicting applicant success proved challenging. Rigorous attempts were made, involving adjustments in binning thresholds for categorical variables, modifications to the number of neurons in hidden layers, layer counts, exploration of various activation functions, and extension of training epochs. Despite these systematic adjustments, accuracy stubbornly plateaued between 72% and 73%.

For a more sophisticated analysis, deeper model refinement is imperative. Integration of KerasTuner, a tool designed for identifying optimal combinations of layers, neurons, epochs, and activation functions, holds promise in maximizing accuracy. Notably, KerasTuner was not utilized in the current model, emphasizing its potential significance in subsequent optimization initiatives.

Alternatively, exploring supervised models presents an intriguing avenue. Considering the unique features and the target variable, initiating trials with a random forest model emerges as a compelling starting point for investigating alternative modeling strategies. These models, once implemented, will undergo meticulous evaluation, facilitating a thorough comparison of metrics to select the most effective model for future endeavors.
