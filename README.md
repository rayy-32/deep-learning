# deep-learning
Assignment 21

## Overview
The goal of this deep learning analysis was to create a binary classifier that could predict if an applicant would be approved for funding.
The model would be a multi-layered neural network that would accurately predict results at least 75% of the time.
---
## Results
#### Data Preprocessing
 * Target variables was the column 'IS_SUCCESSFUL' in the source csv, which details whether an applicant was successful in using the money granted.

 * Feature variables were an applicant's:
    - 'APPLICATION_TYPE'—Alphabet Soup application type
    - 'AFFILIATION'—Affiliated sector of industry
    - 'CLASSIFICATION'—Government organization classification
    - 'USE_CASE'—Use case for funding
    - 'ORGANIZATION'—Organization type
    - 'STATUS'—Active status
    - 'INCOME_AMT'—Income classification
    - 'SPECIAL_CONSIDERATIONS'—Special consideration for application
    - 'ASK_AMT'—Funding amount requested

 * Data removed were the 'EIN' and 'NAME' columns.

#### Compiling, Training, Evaluating the Model
 * The neural network consisted of an input layer (with 43 inputs, 64 neurons and the ReLU activation function),
 a hidden layer (with 64 neurons and the ReLU activation function), and an output layer (with 1 neuron and the sigmoid activation function).
 For the initial model, 1 more hidden layer felt sufficient, as the dataset wasn't too large.

 * The initial machine learning model performed decently, with an accuracy of around 72-73%.

 * To increase optimization, the dataset was transformed further by removing inactive applicants and binning more values together.
 The new neural network has two hidden layers (both with 100 neurons and the ReLU activation function) for further complexity.
 After running the new model, the hyperparameters were tuned with Keras Tuner to find the best performing activation functions, and amounts of neurons and layers.
---
## Summary
With the steps taken to increase optimization, the final neural network was able to achieve an accuracy of 74%, very close to the goal set at the beginning of the assignment.
To increase accuracy further, it may be necessary to further transform the data, or to obtain more data.

Potential different models that could be used to predict applicant success are Logistic Regression, which is simple to set up and flexible to use,
and Support Vector Classifier, which could further define successful and unsuccessul outcomes and help inform what applicant qualities are most influential in a given outcome.