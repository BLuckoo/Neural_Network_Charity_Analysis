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
- The model accuracy target is at least 75%. 
  However, the model's highest accuracy reached is at 70.44% with a loss of 1.30.
   
  This is not a satisfying performance to help predict the outcome of the charity donations.
 
  <p align="center"> 
  <image src="https://user-images.githubusercontent.com/82583576/131259434-fe4d491e-a632-4fa0-876a-18a6be29a856.png"
  </p>
    
    
  However, as illustrated below, the best balance of loss and accuracy is achieved at Epoch 37, loss of 0.63 and accuracy of 65.3%  
  <p align="center">
  <image src="https://user-images.githubusercontent.com/82583576/131259537-96cea073-17ea-4383-9b21-d56fac228601.png"
  </p>            

  <p align="center">  
  <image src="https://user-images.githubusercontent.com/82583576/131259618-b0198b60-2a6e-4680-b0d4-569133c58ce6.png"
  </p>
    
**Model Optimization**

To increase the performance of the model:

- Bucketing was appied to the feature ASK_AMT and organized the different values by intervals.
    
Three different techniques were used to optimize the model and get better accuracy.

1.  Increased the number of hidden layers from two to four.
    
    
    <p align="center">
    <image src="https://user-images.githubusercontent.com/82583576/131260720-1bd39988-38ed-4fb7-afb6-48a33ae2f7d2.png">

    <image src="https://user-images.githubusercontent.com/82583576/131260788-aab79746-76b0-4503-b789-4fe084fbd770.png">

    <image src="https://user-images.githubusercontent.com/82583576/131260835-c76ffc01-b6cf-4348-b766-00f8064fb618.png"
    </p>
     
    
2.  Kept the original number of hidden layers to two, but changed activation function used for the hidden input layers to the "sigmoid" function.
    
3.  Kept the original number of hidden layers to two, but increased the number of neurons from 80 to 100 in the 1st layer and from 30 to 40 in the 2nd layer. The activation function used for the hidden input layers was switched back to the "relu" function.  
    
4.

## Summary

The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is average, the model is not outperforming.

This is a binary classification situation. A supervised machine learning model, such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output. These results can then be compared to the Deep Learning model to evaluate which model is better for the analyis.

















***Resources***
*Data Source: charity_data.csv
Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3*

