# Music Generation with Deep Learning

###### Team Name:- GodFather

###### Team Members:-
                    Anmol Sharma    Rollno:- 19EJDML005
                    Anupam Mishra   Rollno:- 19EJDML006
                    Bhawesh Gehlot  Rollno:- 19EJDML011
                    Pawan Choudhary Rollno:- 19EJDML021
                    
##### Real World Problem
This case-study focuses on generating music automatically using Recurrent Neural Network(RNN).
We do not necessarily have to be a music expert in order to generate music. Even a non expert can generate a decent quality music using RNN.
We all like to listen interesting music and if there is some way to generate music automatically, particularly decent quality music then it's a big leap in the world of music industry.


###### Task:
Our task here is to take some existing music data then train a model using this existing data. The model has to learn the patterns in music that we humans enjoy. Once it learns this, the model should be able to generate new music for us. It cannot simply copy-paste from the training data. It has to understand the patterns of music to generate new music. We here are not expecting our model to generate new music which is of professional quality, but we want it to generate a decent quality music which should be melodious and good to hear.

Now, what is music? In short music is nothing but a sequence of musical notes. Our input to the model is a sequence of musical events/notes. Our output will be new sequence of musical events/notes. In this case-study we have limited our self to single instrument music as this is our first cut model. In future, we will extend this to multiple instrument music.

##### Data Source:
1. http://abc.sourceforge.net/NMD/

From first data-source, we have downloaded first files
Jigs (340 tunes)

the format is incredibly compact. Each line begins with a single letter field (except for notes). ABC notation for music (link: http://abcnotation.com/)

X denotes a reference number
M denotes Meter
K denotes the Key
L denotes the beats
T denotes the Title
Z denotes the transcription The rest are notes that denote the melody for the song.

To create an RNN, specify the model_type as one 'lstm', 'rnn', or 'gru'. In general, the LSTM type networks have shown to be more effective (per Karpathy)

Specify these params:

  batch_size: sequences in a mini batch
  sequence_length: number of characters in a sequence
  n_cells: number of cells in the (hidden) RNN layers
  n_layers: number of layers in the RNN
  ckpt_name: unique name for the model; used to save the model or restore from it
  learning_rate: how fast or slow the network should learn (typically, 0.001, but can be set to 0.0001)
  
##### File Structure:
data -> is the data folder for Music Generation using ABC Sheet Music🎹.ipynb, here I used the ABC sheet music data which is actually in .txt format.
logs -> this is the folder which is consist of output log, that got generated while training the model.
model -> contains weights


##### Prerequisites
You need to have installed following softwares and libraries in your machine before running this project.

Python 3
Anaconda: It will install ipython notebook and most of the libraries which are needed like sklearn, pandas, seaborn, matplotlib, numpy, scipy.
keras

##### Built With
ipython-notebook - Python Text Editor
numpy, scipy- number python library
pandas - data handling library
Keras - Deep Learning Library

##### Model 

Here we are using char-RNN structure(Many-Many RNN) where one output corresponds to each input(input Ci -.> output C(i+1)) at each time step(cell). It can have multiple hidden layers(multiple LSTM layers).
 we’ll customize it to our use case by adding a few tweaks. We’ll use a ‘character RNN’. In character RNNs, the input, output, and transition output are in the form of characters.
 
 ##### How to Run the Model
In order to run the model you can run the file " Music_Generation.ipynb"  There are total 9 weight files over there. Each weight file represents the epoch number. For instance " Weights_50.h5" are the weights saved at epoch 50. We ran our model for total of 90 epochs. You can add more layers into your model and fine tune the existing layers in the model. Any epoch weight can be loaded for fine tuning or "Transfer Learning".

#### Result 
Total params: 1,904,983
Trainable params: 1,904,983
Non-trainable params: 0
loss = 0.23245219886302948, acc = 0.9130859375
