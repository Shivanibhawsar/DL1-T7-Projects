# Traffic-signs-recognition

## Table of contents
* [Dataset](#dataset)
* [Prerequisites](#prerequisites)
* [Model](#model)
* [Steps](#steps)
* [Result](#result)


## Dataset
For this project I have used public dataset from kaggle

https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

The dataset contains more than 50,000 images of different traffic signs. It is further classified into 43 different classes. The dataset is quite varying, some of the classes have many images while some classes have few images. The size of the dataset is around 300 MB. The dataset has a train folder which contains images inside each class and a test folder which we will use for testing our model.

## Prerequisites
Tensorflow 
Keras
Scikit-learn
Matplotlib
Pandas
Numpy
Pillow
Tkinter

## Model
To classify the images into their respective categories, I have build a CNN model(Convolutional Neural Network) because CNN is best for image classification purposes.
To compile the model with Adam optimizer which performs well and loss is “categorical_crossentropy” because we have multiple classes to categorise.

## Steps
* Run "traffic_signs_recognition.ipynb" on google colab
* and then download "traffic_sign_classifier.h5"
* now you have to run "gui.ipynb"(not on google colab because it cannot open window) and make sure "traffic_sign_classifer.h5" is in root directory.

## Result
* Training accuracy - 98.38%
* Test accuracy - 94.86%
