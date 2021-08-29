# Neural Network Charity Analysis

Using Machine Learning and Neural Networks models with the dataset provided to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Analysis Overview

The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

The following methods were used for the analysis:

- Preprocessing the data for the neural network model
- Compile, train and evaluate the model
- Optimize the model

## Results

**Data Preprocessing**

- The columns EIN and NAME are identification information and have been removed from the input data.
- The column IS_SUCCESSFUL contains binary data refering to wether or not the charity donation was used effectively. This variable is then considered as the target for the deep learning neural network.
- The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for the model.
- Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.

**Compiling, Training, and Evaluating the Model**


- The input data has 43 features and 25,724 samples.

<p align="center">
<image src="https://user-images.githubusercontent.com/82583576/131258310-e521342e-4bbb-4c34-8368-cafad16a63f6.png"
</p>

- This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
  
 <p align="center"> 
 <image src="https://user-images.githubusercontent.com/82583576/131258458-dc2a889a-85ed-4d38-b6f3-4b4f198487a8.png"
 </p>
 
  
  
- The output layer is made of a unique neuron as it is a binary classification.
- To speed up the training process, the activation function ReLU is used for the hidden layers. As the output is a binary classification, Sigmoid is used on the output layer.
- For the compilation, the optimizer is ***"adam"*** and the loss function is ***"binary_crossentropy"***.
- The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.
 
  <p align="center"> 
  <image src="https://user-images.githubusercontent.com/82583576/131259434-fe4d491e-a632-4fa0-876a-18a6be29a856.png"
  </p>
    
    
    
  <p align="center">
  <image src="https://user-images.githubusercontent.com/82583576/131259537-96cea073-17ea-4383-9b21-d56fac228601.png"
  </p>            

**Model Optimization**

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

