# Fashion-MNIST

Fashion-MNIST is a dataset of images consisting of a training set of 60,000 examples and a 
test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label
from 10 classes.

The objective is to identify (predict) different fashion products from the given images 
using a CNN model.

## Libraries Required
- Tensorflow
- Keras
- Matplotlib
- Pandas
- Numpy

## Model

- Used Sequential model API to create a simple CNN model repeating 2 layers of 2D 
convolution layer followed by a MaxPooling2D layer then a dropout layer.
- Compiled the model using model.compile() to configure the learning process before training
 the model. Here we used categorical_crossentropy loss function and adam optimizer.
- Finally, trained the model with a batch_size of 64 and 10 epochs. 

## Result

Train Accuracy = 99.14% <br>
Test Accuracy = 91.25% <br>

## Team Members:
Yogita Keswani - 19EJDDS025<br>
Janvi Vijay    - 19EJDML014<br> 
Ajay Kathat    - 19EJDDS002
