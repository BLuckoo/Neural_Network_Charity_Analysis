# Neural Network Charity Analysis

Using machine learning and neural networks, with the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Analysis Overview

The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

The following methods were used for the analysis:

- Preprocessing the data for the neural network model
- Compile, train and evaluate the model
- Optimize the model

## Results

**Data Preprocessing**

- The columns EIN and NAME are identification information and have been removed from the input data.
- The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
- The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
- Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.

**Compiling, Training, and Evaluating the Model**

- This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
- The input data has 43 features and 25,724 samples.
- The output layer is made of a unique neuron as it is a binary classification.
- To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
- For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
- The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.

** Model Optimization**

To increase the performance of the model:

- Bucketing was appied to the feature ASK_AMT and organized the different values by intervals.
- Increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
- A different activation function (tanh) but none of these steps helped improve the model's performance.

## Summary

The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is average, the model is not outperforming.

This is a binary classification situation. A supervised machine learning model, such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output. These results can then be compared to the Deep Learning model to evaluate which model is better for the analyis.

















***Resources***
*Data Source: charity_data.csv
Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3*

