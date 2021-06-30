# DL1-T7-Projects
# Image Classification

## Dataset
For this project I have used cifar 10 from keras

tf.keras.datasets.cifar10.load_data()

This is a dataset of 50,000 32x32 color training images and 10,000 test images, labeled over 10 categories. 

airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

## Model
- Two 2D convolution layer in sequence with input shape as (32,32,3) and relu as activation function along with dropout to avoid overfitting.
- A MaxPooling2D layer to extract most prominent features.
- Two dense layer as output layer connected sequentially with relu and softmax as its activation function respectively.

## Prerequisites
numpy
tkinter
Matplotlib
keras

## How to run
Run "classification_image.ipynb" then run "gui.ipynb" and make sure to have "model1_cifar_10.h5" in your root directory.

## Result
Train accuracy 71.09%
Test accuracy 71.09000086784363%
