# Drowsiness Detection System
 This is a project implementing Computer Vision and Deep Learning concepts to detect drowsiness of a driver and sound an alarm if drowsy
### Description
 In this deep learning model which first detect the face and eyes and based on the status of the eyes if the eyes are closed more than usual time then it can generate an alarm. This can be used by riders who tend to drive for a longer period of time that may lead to accidents.
### Technologies used
Python, OpenCV, Tensorflow, Keras
### Code Requirements
- Python 3.7.6
- OpenCv 4.5.2
### Libraries 
```
import cv2
import os
import random
import pickle
import numpy as np
import matplotlib.pyplot as plt
import tensorflow as tf
from tensorflow import keras
from tensorflow.keras import layers
```
### Model
1. Reading all the images from the dataset and converting them into an array for Data & Labels.
2. Random shuffle is used to minimize overfitting
3. Using TensorFlow, import a Keras image classification model, optionally loaded with weights pre-trained on ImageNet. 
  ``` model = tf.keras.applications.mobilenet.MobileNet() ```
3. Use Tranfer Learning to create new model from above pretrained model
4. A single unit dense layer is acting as output for binary classification with activation set to **Sigmoid**
5. Optimizer is set to Adam.
6. For realtime time eyetracking in videos, use Haar Cascades frontal face algo.
### Execution
- Run "Drowsiness detection system.ipynb" and make sure to have "my_driver.h5" in your root directory
### Result
- After epochs = 3
  - Accuracy on Training set = 97.60%
  - Accuracy on Validation set = 76.25%
### Team Quad
- Varun Rathore
- Vishal Singh Chawada
- Rajveer Singh Chouhan
- Sumer Singh Parmar
  
