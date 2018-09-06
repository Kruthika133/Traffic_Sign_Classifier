## Project: Build a Traffic Sign Recognition Program
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---
In this project, I will use deep neural networks and convolutional neural networks to classify traffic signs. I will train and validate a model so it can classify traffic sign images using the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset). After the model is trained, I will then try out your model on images of German traffic signs from the web.

The project was implemented as a Jupyter notebook (with plenty of helper code already filled in). The higher-level steps prescribed to complete the project were:

0. Load the Data
1. Dataset Summary & Exploration
2. Design and Test a Model Architecture
3. Test a Model on New Images

1. Basic summary of the data set:

I used the numpy library to calculate summary statistics of the traffic signs data set:

The size of training set is 34799
The size of test set is 12630
The shape of a traffic sign image is (32, 32, 3)
The number of unique classes/labels in the data set is 43

 2. Dataset Summary & Exploration
 I performed an exploratory visualization of the data set. It is a histogram for training data (Class vs Number of Images) showing how the data is distributed across various classes
 
 3. Design and Test a Model Architecture
 I converted the images to grayscale because it would save unnecessary computation power.
 Then, I normalized the images.
 
My final model consisted of the following layers:

Layer                            Description
Input                           32x32x3 RGB image
Gray                            32x32x1 Gray Image
Normalized                 32x32x1 Normalized Image
Convolution         1x1 stride, valid padding, outputs 28x28x6
RELU     
Max pooling               2x2 stride, outputs 14x14x6
Convolution          1x1 stride, valid padding, outputs 10x10x16
RELU     
Max pooling             2x2 stride, outputs 5x5x6
Flatten                         outputs 400
Fully Connected              	outputs 120
RELU     
Fully Connected              	outputs 84
RELU     
Fully Connected              	outputs 43
Softmax     

4. Hyperparameters:
To train the model, I used an EPOCHS of 25, BATCH SIZE of 128, learning rate of 0.001

The accuracy on my final model were:

validation set accuracy of 0.931
test set accuracy of 0.912





