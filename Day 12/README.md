# Day 12 – Sentiment Analysis on Tweets using LSTM + GloVe

---

## Project Overview

In this project, we build a deep learning model to classify the sentiment of tweets as **positive** or **negative**.  
We use an LSTM (Long Short-Term Memory) network along with pretrained GloVe word embeddings to capture the context and semantics of tweets.

---

## Key Concepts Covered

- Text cleaning and preprocessing (removing mentions, hashtags, URLs, and other noise)  
- Tokenization and padding of text sequences  
- Using pretrained GloVe embeddings to represent words as dense vectors  
- Building an LSTM model for sequence modeling of tweet text  
- Training and evaluating the model for binary sentiment classification  
- Visualizing training history and performance metrics  

---

## Dataset

- We use a dataset of tweets labeled with sentiment (0 = negative, 1 = positive).  
- The dataset is loaded directly from a public GitHub URL.

---

## How the Model Works

1. **Text Cleaning:**  
   Remove Twitter-specific noise like user mentions (`@user`), hashtags (`#hashtag`), retweet tags (`RT`), URLs, and non-alphanumeric characters. Convert text to lowercase.

2. **Tokenization & Padding:**  
   Convert cleaned tweets into sequences of word indices using Keras `Tokenizer`. Pad sequences to fixed length (e.g., 150 tokens) so the model input is uniform.

3. **GloVe Embeddings:**  
   Load pretrained 100-dimensional GloVe embeddings to convert words into meaningful vectors. We create an embedding matrix mapping our tokenizer’s vocabulary to GloVe vectors.

4. **LSTM Model Architecture:**  
   - Embedding layer initialized with GloVe weights (frozen during training).  
   - LSTM layer with 128 units to learn sequential context.  
   - Dropout layers (0.5 and 0.3) to reduce overfitting.  
   - Dense layer with ReLU activation for nonlinear learning.  
   - Final Dense layer with sigmoid activation for binary classification output.

5. **Compilation:**  
   The model is compiled using `binary_crossentropy` loss (for binary classification), Adam optimizer, and accuracy metric.

6. **Training:**  
   The model is trained for 5 epochs with batch size 64. 20% of training data is reserved for validation to monitor performance and avoid overfitting.

7. **Evaluation:**  
   Evaluate model performance on unseen test data to get test loss and accuracy.

8. **Metrics:**  
   Generate classification report showing precision, recall, F1-score, and support for each class.

9. **Visualization:**  
   Plot training and validation accuracy and loss curves to visualize learning progress.

---

## How to Run

1. Clone or download the notebook and dataset.  
2. Download the GloVe embeddings (e.g., `glove.6B.100d.txt`) and place it in your working directory.  
3. Run all cells step-by-step to preprocess data, build, train, and evaluate the model.  
4. Visualize results using the plotted graphs and classification report.

---

## Notes

- The vocabulary size is limited to 10,000 most frequent words.  
- Sequences are padded/truncated to a fixed length of 150 tokens to standardize input size.  
- GloVe embeddings are loaded and used as fixed weights (not trainable) for better generalization.  
- The model is a binary classifier and can be extended to multi-class with modifications.  
- Overfitting is controlled using dropout layers and validation split during training.

---

## Potential Improvements

- Fine-tune GloVe embeddings by setting `trainable=True` in the embedding layer.  
- Experiment with more LSTM units or stacking multiple LSTM layers.  
- Try GRU or bidirectional LSTM layers.  
- Use more advanced pretrained language models like BERT or RoBERTa via Hugging Face Transformers.  
- Implement multi-class sentiment classification (positive, neutral, negative).  
- Add real-time tweet sentiment inference and visualization.

---

## References

- [GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/projects/glove/)  
- [Keras Embedding Layer Documentation](https://keras.io/api/layers/core_layers/embedding/)  
- [TensorFlow LSTM Tutorial](https://www.tensorflow.org/tutorials/text/text_classification_rnn)  
- [Scikit-learn Classification Report](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)

---

## Contact

If you have questions or want to collaborate, feel free to reach out!

---

*Happy coding and keep exploring NLP!* 🚀
