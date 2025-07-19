# 🧠 Next-Word Predictor using LSTM

---

### 🎯 **Objective**
To build an intelligent Next Word Prediction system using **Long Short-Term Memory (LSTM)** networks. By learning from sequential patterns in a large text corpus, the model aims to accurately predict the next word in a sentence, enhancing user experience in applications like smart typing, autocomplete, and conversational AI.

---

### 📚 **Data Collection & Preprocessing**
* **Dataset**: The novel *The Mysterious Island* by Jules Verne was downloaded from [gutenberg.org](https://www.gutenberg.org/).
* **Text Cleaning**:
    * Removed punctuation, special characters, and extra spaces.
    * Converted all text to lowercase for uniformity.
* **Sequence Creation**: Tokenized the text into individual words and created input sequences using a sliding window approach.

---

### 🎟️ **Text Tokenization**
* **Tokenizer**: Utilized the `Keras Tokenizer` to convert words into integer sequences.
* **N-gram Sequences**: Defined a fixed sequence length to form input sequences (n-grams).
* **Target Encoding**: One-hot encoded the target words (the next word in the sequence) for the model's output layer.

---

### 🏗️ **Model Architecture**
A Sequential LSTM model was constructed with the following layers:
* **Embedding Layer**: Maps integer-encoded words to dense word vectors of a fixed size.
* **Two LSTM Layers**: Two stacked LSTM layers to effectively learn long-range dependencies and temporal patterns in the text sequences.
* **Dense Layer (Softmax)**: A fully connected output layer with a **softmax** activation function to predict the probability distribution of the next word over the entire vocabulary.

---

### 💪 **Training**
* **Loss Function**: `categorical_crossentropy` was used, which is ideal for multi-class classification tasks.
* **Optimizer**: The **Adam** optimizer was employed for its efficiency and adaptive learning rate capabilities.
* **Training Process**: The model was trained for up to 150 epochs with **Early Stopping** to prevent overfitting and save the best model weights.

---

### 🔍 **Evaluation & Prediction**
* **Evaluation**: The model's performance was evaluated based on its training accuracy and loss.
* **Prediction**: Generated sample text by providing seed sentences to qualitatively assess the logical flow and coherence of the predicted words.

---

### 📊 **Results**
* **Dataset**: *The Mysterious Island* by Jules Verne
* **Model Architecture**: Stacked LSTM (2 layers)
* **Sequence Length**: 15 words
* **Vocabulary Size**: 10,067 unique words
* **Test Accuracy**: **91.67%**
* **Loss**: 0.3847
