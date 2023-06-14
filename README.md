# Image-classification-with-convolutional-Neural-Network

# Methodology and Experiments 
 Introduction
This section explains the research design, machine learning types to be used in this study, describes the work flow of this study. 
Data collection and preparation
The data for the project is a popular dataset in data science and machine learning known as CIFAR-10 which was a tiny images collected by MIT and NYU over a period of six months(McCrary, 1992) . which contains 60,000 tiny images.



# Data pre-processing 
The images had different sizes and dimensions, so I normalized the images to have a value between 0 and 1 by dividing both the training and test data set by 255 so that all the images will have the same sizes.
Data splitting  
The dataset was divided into train and test set with training data having 50,000 images and test data having 10,000 datasets, where the test data was used to access the performance of the model after training.
Model architecture design 
In the model architecture it is widely recommended by many researchers that Convolutional Neural Network (CNN) performs better with image classification as compared to Artificial Neural Network. In this our project architecture design I will consider both ANN and CNN and determine which architecture performs better with image classification. (Anon., 2014)

# Artificial Neural Network (ANN)
With Artificial Neural Network I will consider two levels design.
1. A design with (32,32,3) input shape, a dense layer of 3000 and activation in the hidden layer as “ReLu” and an output layer with 10 variables and activation in the output layer as SOFTMAX, after I compiled the model and set optimizer as SGD, loss function as “Sparse_categotical_crossentropy” and metrics as Accuracy and then train the model on 10 epochs. 
2. A second ANN design with (32,32,3) input shape, a dense layer of 3000 and activation in the hidden layer as “ReLu” and an output layer with 10 variables and activation in the output layer as SOFTMAX, after I compiled the model and set optimizer as ADAM, loss function as “Sparse_categotical_crossentropy” and metrics as Accuracy and then train the model on 10 epochs.
   
# Convolutional Neural Network (CNN)
With Convolutional Neural networks two architectures will be considered, one with optimizer called Adaptive Moment Estimation (ADAM) and another Stochastic Gradient Descent (SGD)
1.	In the sequential model, I specify the Con2D layer and specify filters to 32, kernel size as (3,3), activation function as RELU and input shape to (32,32,3) and also specify the Maxpooling2D to (2,2)
In the second Con2D layer and specify filters to 64, kernel size as (3,3), activation function as RELU and also specify the Maxpooling2D to (2,2), in the Dense layer 64 was specified and activation to RELU, in the second Dense layer 10 was specified and activation as SOFTMAX. In the compile function, optimizer function was specified as ADAM and loss function as Sparse_Categorical_Crossentropy and metrics to Accuracy

3.	The second architecture, in the sequential model, I specify the Con2D layer and set filters to 32, kernel size as (3,3), activation function as RELU and input shape to (32,32,3) and also specify the Maxpooling2D to (2,2). In the second Con2D layer, I set the filters to 64, kernel size as (3,3), activation function as RELU and also specify the Maxpooling2D to (2,2), in the Dense layer 64 was specified and activation to RELU, in the second Dense layer 10 was specified and activation as SOFTMAX. In the compile function, optimizer function was specified as SGD and loss function as Sparse_Categorical_Crossentropy and metrics to Accuracy


Results
Table 1. Shows the architecture design for the first ANN design with optimizer SGD

Classification Report:

| variable | Precision | Recall |F1-Score | Support |
| :---     |     :---: |   ---: |     ---:|     --: |
|    0	   | 0.54       |	0.59	 |0.56	   |   1000 |
|1	|0.36	|0.87	|0.51	|1000|
|2	|0.37	|0.48|0.42	|1000|
|3	|0.40	|0.34|	0.36|	1000|
|4	|0.50	|0.34	|0.40	|1000|
|5	|0.57	|0.20	|0.30	|1000|
|6	|0.64	|0.43	|0.51	|1000|
|7	|0.49	|0.65	|0.56	|1000|
|8	|0.64	|0.59	|0.61	|1000|
|9	|0.63	|0.26	|0.36	|1000|


| Accuracy | Support |
|     :---: |     ---:|     
|       0.47  |    10000|

table 2. Shows twenty Actual Values and their predicted values
|Actual values|	Predicted values|
|     ---:|     --: |
|3	|3|
|8	|1|
|8	|8|
|0	|8|
|6	|4|
|6	|6|
|1	|1|
|3	|3|
|1	|1|
|0	|8|
|9	|1|
|5	|1|
|7	|7|
|9	|1|
|8	|8|
|5	|7|
|7	|0|
|8	|8|
|6	|7|


# TO BE CONTINUED.....


