# Music-Generation-Using-Deep-Learning

Created By Ankush Patel 

Roll No:-19EJDAI003

email_id: ankush.19jdai044@jietjodhpur.ac.in

Demo Link : https://drive.google.com/file/d/1215WpdEbwvG9LdUb-xhuCHl2Ae-bC7B7/view?usp=sharing

This project allows you to train a neural network to generate midi music files that make use of a single instrument

## Requirements

* Python 3.x
* Installing the following packages using pip:
	* Music21
	* Keras
	* Tensorflow
	* h5py
	
## Data

You Can use your own midi file just add them in midi_songs folder

## Training

To train the network you run **lstm.py**.

E.g.

```
python lstm.py
```

The network will use every midi file in ./midi_songs to train the network. The midi files should only contain a single instrument to get the most out of the training.

**NOTE**: You can stop the process at any point in time and the weights from the latest completed epoch will be available for text generation purposes.

## Generating music

Once you have trained the network you can generate text using **predict.py**

E.g.

```
python predict.py
```

You can run the prediction file right away using the **weights.hdf5** file

## Theory

Neural networks are being used to improve all aspects of our lives. They provide us with recommendations for items we want to purchase, generate text based on the style of an author and can even be used to change the art style of an image.

Recurrent Neural Networks (RNN)
A recurrent neural network is a class of artificial neural networks that make use of sequential information. They are called recurrent because they perform the same function for every single element of a sequence, with the result being dependent on previous computations. Whereas outputs are independent of previous computations in traditional neural networks.

Music21
Music21 is a Python toolkit used for computer-aided musicology. It allows us to teach the fundamentals of music theory, generate music examples and study music. The toolkit provides a simple interface to acquire the musical notation of MIDI files. Additionally, it allows us to create Note and Chord objects so that we can make our own MIDI files easily.

Keras
Keras is a high-level neural networks API that simplifies interactions with Tensorflow. It was developed with a focus on enabling fast experimentation.

## In our model we use four different types of layers:

LSTM layers is a Recurrent Neural Net layer that takes a sequence as an input and can return either sequences (return_sequences=True) or a matrix.

Dropout layers are a regularisation technique that consists of setting a fraction of input units to 0 at each update during the training to prevent overfitting. The fraction is determined by the parameter used with the layer.

Dense layers or fully connected layers is a fully connected neural network layer where each input node is connected to each output node.

The Activation layer determines what activation function our neural network will use to calculate the output of a node.

## Information about the different layers we will be using it is time to add them to the network model.

For each LSTM, Dense, and Activation layer the first parameter is how many nodes the layer should have. For the Dropout layer the first parameter is the fraction of input units that should be dropped during training.

For the first layer we have to provide a unique parameter called input_shape. The purpose of the parameter is to inform the network of the shape of the data it will be training.

The last layer should always contain the same amount of nodes as the number different outputs our system has. This assures that the output of the network will map directly to our classes.

To calculate the loss for each iteration of the training we will be using categorical cross entropy since each of our outputs only belongs to a single class and we have more than two classes to work with. And to optimise our network we will use a RMSprop optimizer as it is usually a very good choice for recurrent neural networks.

Once we have determined the architecture of our network the time has come to start the training. The model.fit() function in Keras is used to train the network. The first parameter is the list of input sequences that we prepared earlier and the second is a list of their respective outputs. In our tutorial we are going to train the network for 200 epochs (iterations), with each batch that is propagated through the network containing 64 samples.

To make sure that we can stop the training at any point in time without losing all of our hard work, we will use model checkpoints. Model checkpoints provide us with a way to save the weights of the network nodes to a file after every epoch. This allows us to stop running the neural network once we are satisfied with the loss value without having to worry about losing the weights. Otherwise we would have to wait until the network has finished going through all 200 epochs before we could get the chance to save the weights to a file.
