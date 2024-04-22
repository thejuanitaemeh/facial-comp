# Facial Completion Model Training and Testing
## Introduction 
In this task, you'll be training and testing a model to predict the 512 pixels of the right face from the 512 pixels of the left face by formulating a regression task.

## Instructions
1. Use Copilot Chat to create a new notebook in your project. Use command /newnotebook and name it as "Facial Completion Model".
2. Look through the supporting file lab3lib,the functions you will be using in this project and understand the format that they need to be used in.
3. Use Copilot and Copilot Chat to develop the exercise and support your learning.

## DATA PREPARATION
1. Import load_data, show_single_face, show_faces, partition_data, split_left_right, join_left_right, show_split_faces
2. import numpy
3. Display a single face
4. There are 400 images. Pick a random number from one to 400 and display that image.
5. Display the first 16 faces
6. Display the first 16faces with four faces in a row
7. Normalise the pixel values
8. Get the training and testing indices using the partition_data function. Specify 3 images per class for training.
9. Get training and testing data from the indices with corresponding labels


## TRAINING MODEL
Below are the specifications for training the model
1. Create a function to train the model
2. Minimise the L2 regularised sum of squares loss
3. Zero the loss gradient
4. It should support both single-output and multi-output cases
5. Function should take a set of training samples and a user-specified regularisation parameter lambda as the input
6. Function should return predicted weights.
7. When lambda is zero, use a pseudo-inverse to implement the solution

## PREDICTION
Create a function that takes the trained weights and your query data as the input and return corresponding prediction

## FACIAL COMPLETION
1. Split data into left and right
2. Display the first 16 left and right faces using the show_faces function

## IMPLEMENT THE MODEL
1. Get the training and testing indices by partitioning labels using the partion_data function with 5 per class for training.
2. Get the left training data using the training indices and the left data
3. Get the right training data using the training indices and the right data
4. Get the left testing data using the testing indices and the left data
5. Get the right testing data using the testing indices and the right data
6. Train a regularized least squares model on the left training data using the training functon with right data as labels and lamba = 0
7. Get the predicted labels for the left testing data using the prediction function
8. Calculate the mean absolute percentage error between the predicted and actual training labels using sklearn mean absolute percentage error function.

## TESTING 

Choose a random index, join all the left training data with the right training data usng the join_left_right function, then use the show_single_face function to print the joint face at that index.
Join all the left training data with their predicted labels using the join_left_right function and then use the show_single_face function to show the predicted face for that index.

What does the Mean Absolute Percentage Error represent here?




   
