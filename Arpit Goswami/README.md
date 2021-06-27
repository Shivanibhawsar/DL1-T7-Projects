# Image Classification on CIFAR-10 dataset 
The CIFAR-10 dataset is a collection of images of 10 different classes like cars, birds, dogs, horses, ships, trucks, etc. The idea of the project is to build an image classification model that will be able to identify what class the input image belongs to.

# Model
- Two 2D convolution layer in sequence with input shape as (32,32,3) and relu as activation function along with dropout to avoid overfitting.
- A MaxPooling2D layer to extract most prominent features.
- Two dense layer as output layer connected sequentially with relu and softmax as its activation function respectively.

# Libraires Required
- Keras
- Matplotlib
- Pillow
- Numpy
- tkinter

# How to run 
Run "image_classification.ipynb" then run "gui.py" and make sure to have "image_classfier_model.h5" in your root directory.

# Results

Train Accuracy : 79.76% <br>
Test Accuracy : 69.67%
