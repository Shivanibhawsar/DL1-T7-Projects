# Sentiment Analysis on YELP reviews

Trained a bidirectional LSTM with self trained word embeddings. The model was used to classify YELP reviews as either positive or negative.

Things I learnt in the process are Regular Expressions, F strings and cleaning text data for neural networks. This is the first time I used the Sequential model in Keras instead of its functional API.

# Model

1. An embedding layers converting word tokens into 50-dim embeddings.
2. Bidirectional LSTM layer with dropout to minimize overfitting.
3. A single unit dense layer acting as the output layer with activation set to 'Sigmoid'

# Result

After 3 epochs: <br>
Train Acc = 96.5% <br>
Test Acc = 90.1% <br>

# Future_Ideas

The model over fitted a little. Thinking of using pre-trained word embeddings and using TensorBoard for optimization.
