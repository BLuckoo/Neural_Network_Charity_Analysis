# Neural Network Charity Analysis

This analysis uses Machine Learning and Neural Networks models utilizing the dataset provided to create binary classifier that can predict if applicants will be successful if funded by Alphabet Soup.

## Analysis Overview

The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

The following methods were used for the analysis:

- Preprocessing the data for the neural network model
- Compile, train and evaluate the model
- Optimize the model

## Results

**Data Preprocessing**

- Columns EIN and NAME are identification information and have been removed from the input data.
- Column IS_SUCCESSFUL contains binary data that refers to whether the charitable donation was used effectively. This variable is then considered as the target for the deep learning neural network.
- The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are features used for the model.
- Encoding of the categorical variables, splitting into training and testing datasets and standardization have been applied to the features.

**Compiling, Training, and Evaluating the Model**


- The input data has 43 features and 25,724 samples.

<p align="center">
<image src="https://user-images.githubusercontent.com/82583576/131258310-e521342e-4bbb-4c34-8368-cafad16a63f6.png"
</p>

- This deep-learning neural network model is comprised of two hidden layers with 80 and 30 neurons respectively.
  
 <p align="center"> 
 <image src="https://user-images.githubusercontent.com/82583576/131258458-dc2a889a-85ed-4d38-b6f3-4b4f198487a8.png"
 </p>
 
  
  
- The output layer is made of a unique neuron as it is a binary classification.
- To speed up the training process, the activation function ReLU is used for the hidden layers. As the output is a binary classification, Sigmoid is applied on the output layer.
- For the compilation, the optimizer is ***"adam"*** and the loss function is ***"binary_crossentropy"***.
- The model accuracy target is at least 75%. 
  However, the model's highest accuracy reached is at 70.44% with a loss of 1.30.
   
  This is not a satisfactory performance in predicting the outcome of the charitable donations.
 
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
<br>
    
## Model Optimization

To increase the performance of the model:

- Bucketing was applied to the feature ASK_AMT and as well as organized the different values by intervals.
    
Three different techniques were employed to optimize the model and to achieve improved accuracy.

1.  Increased the number of hidden layers from two to four.
    This attempt brought down the accuracy to 69.48% and the loss increased to 12.21
    
    <p align="center">
    <image src="https://user-images.githubusercontent.com/82583576/131260720-1bd39988-38ed-4fb7-afb6-48a33ae2f7d2.png">
    </p>
      
    <p align="center">  
    <image src="https://user-images.githubusercontent.com/82583576/131260788-aab79746-76b0-4503-b789-4fe084fbd770.png">
    </p>
      
    <p align="center">  
    <image src="https://user-images.githubusercontent.com/82583576/131260835-c76ffc01-b6cf-4348-b766-00f8064fb618.png">
    </p>
     
    
2.  Retained the original number of hidden layers to two, but changed activation function used for the hidden input layers to the "sigmoid" function.
    This model resulted in a loss of 0.637 and an accuracy of 69.78%.
      
    <p align="center">
    <image src="https://user-images.githubusercontent.com/82583576/131261078-b64bc3f9-7c56-49fc-9e2a-0e6b0d6e9500.png"
    </p>
    
    <p align="center">  
    <image src="https://user-images.githubusercontent.com/82583576/131261122-5239d422-383b-4099-8964-dd566323165c.png"
    </p>
      
    <p align="center">
    <image src="https://user-images.githubusercontent.com/82583576/131261196-9114d89f-6009-41b0-ac1f-af070eb59cf7.png"
    </p>  
    
3.  Kept the original number of hidden layers to two, but increased the number of neurons from 80 to 100 in the 1st layer and from 30 to 40 in the 2nd layer. The activation function used for the hidden input layers was switched back to the "relu" function.  
      For this model the loss came to 10.98 and the accuracy to 59.98%.
    
      <p align="center">
      <image src="https://user-images.githubusercontent.com/82583576/131261335-03af4473-e2fa-418a-9b10-fd182471b8ef.png"
      </p>
      
      <p align="center">  
      <image src="https://user-images.githubusercontent.com/82583576/131261359-46508d8f-dc23-4516-a7d1-335d0c298854.png"
      </p>
             
      <p align="center">       
      <image src="https://user-images.githubusercontent.com/82583576/131261384-961bc799-9d10-4a61-b11c-5a9564598b67.png"
      </p>
      
 4. In an attempt to get better results, this model uses 3 hidden layers and the "relu" activation function for the input layers.
    Unfortuntaely the results were not satisfactory: the loss was at 10.97 and the accuracy at 59.98%.
        
        
      <p align="center">  
      <image src="https://user-images.githubusercontent.com/82583576/131281069-eff41955-1e2f-4485-ba57-66b12b076253.png"
      </p>
        
        ![image](https://user-images.githubusercontent.com/82583576/131281239-a2cfba77-f798-4a2c-9c69-38508699ef91.png)

        
        
        

## Summary

The deep learning neural network model did not reach the target of 75% accuracy. The performance of this model therefore does not meet the requirements as laid out.

This is a binary classification situation. It is recommended that a supervised machine learning model, such as the Random Forest Classifier be used to combine a multitude of decision trees. This will allow the generation of classified ouput. The result can then be compared to the Deep Learning model to evaluate its performance and whether it meets the client's requirements.
        
       
       
