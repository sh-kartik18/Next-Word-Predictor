# Next-Word-Predictor using LSTM
The objective of this project is to build an intelligent Next Word Prediction system using Long Short-Term Memory (LSTM) networks. By learning from sequential patterns in a large text corpus, the model aims to accurately predict the next word in a sentence, enhancing user experience in applications like smart typing, autocomplete, and conversational AI systems.
# Data Collection & Preprocessing
Downloaded the novel The Mysterious Island by Jules Verne from gutenberg.org.

Cleaned the text: removed punctuation, special characters, extra spaces; converted to lowercase.

Tokenized the text into individual words and created input sequences using a sliding window approach.
# Text Tokenization
Used Keras Tokenizer to convert words to integer sequences.

Defined a fixed sequence length to form n-gram sequences.

One-hot encoded the target words for training.
# Model Architecture
Built a Sequential LSTM model:

Embedding Layer – to map integers to dense word vectors.

Two LSTM Layers – to learn temporal patterns in sequences.

Dense Layer with Softmax – to predict the next word.
# Training
Used categorical_crossentropy as the loss function and Adam Optimizer.

Applied early stopping and trained for up to 150 epochs.
# Evaluation & Prediction
Evaluated the model based on training accuracy.

Generated text samples to check the logical flow of predicted words/
# Results
Dataset: The Mysterious Island by Jules Verne (from Gutenberg.org)

Model Architecture: LSTM (2 stacked layers)

Sequence Length: 15 words

Vocabulary Size: 10,067

Test Accuracy: 91.67%

Loss: 0.3847

