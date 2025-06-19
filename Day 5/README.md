# ✍️ Day 5 - Handwritten Digit Recognition with MNIST

Welcome to **Day 5** of the **"30 Days, 30 Machine Learning Projects"** challenge!

In this project, we build a **digit recognizer** using the famous **MNIST dataset**, which contains thousands of labeled images of handwritten digits from 0 to 9. This project introduces you to **deep learning**, **image classification**, and how neural networks process visual data. It is a foundational step into the world of **computer vision**.

---

## 📌 Project Objective

The goal is to create and train a neural network that can accurately classify handwritten digits from the MNIST dataset using **TensorFlow** and **Keras**.

---

## 📊 Dataset: MNIST

The **MNIST (Modified National Institute of Standards and Technology)** dataset is a benchmark in the machine learning community for evaluating image classification models.

- **Total samples:** 70,000 grayscale images
  - **Training set:** 60,000 images
  - **Test set:** 10,000 images
- **Image size:** 28x28 pixels (784 pixels in total)
- **Color:** Grayscale (pixel values range from 0 to 255)
- **Labels:** Digits from 0 to 9 (10 total classes)

Each image represents a handwritten digit centered in a 28x28 square.

---

## 🧠 Concepts Covered

This project covers the following important machine learning and deep learning concepts:

- 🧹 **Data Preprocessing**: Flattening and normalizing image pixel values for input to neural networks
- 🔁 **Feedforward Neural Networks**: Using a sequential model with multiple dense (fully connected) layers
- 🔢 **Activation Functions**:
  - **ReLU**: Helps the model learn non-linear patterns
  - **Softmax**: Used in the output layer for multi-class classification
- 📉 **Loss Function**:
  - **Sparse Categorical Crossentropy** for comparing predicted class probabilities with integer labels
- 🧮 **Optimizer**:
  - **Adam** optimizer for adaptive learning rate optimization
- 📈 **Model Evaluation**: Training/validation accuracy and loss visualization
- 🧪 **Prediction Visualization**: Viewing and interpreting model predictions on test images

---

## 🛠️ Tools & Libraries Used

- 🐍 **Python 3.x**
- 🔢 **NumPy** – Numerical operations
- 📊 **Matplotlib** – For data and prediction visualization
- 🧠 **TensorFlow/Keras** – For building and training the neural network

---

## 🧪 Model Architecture

We are using a **fully connected neural network** (also called a dense network) as our baseline model:

### 📥 Input Layer
- Takes in 784 features (flattened 28x28 image)
- Normalized pixel values (0-1)

### 🧱 Hidden Layers
- `Dense(128)` neurons with **ReLU** activation
- `Dense(64)` neurons with **ReLU** activation

### 🧾 Output Layer
- `Dense(10)` neurons with **Softmax** activation
- Each neuron corresponds to one digit (0 to 9)
- Outputs a probability distribution over the 10 classes

### ⚙️ Compile Settings
- **Loss Function**: `SparseCategoricalCrossentropy`
- **Optimizer**: `Adam`
- **Metrics**: `Accuracy`

---

## 🚀 Steps Involved

1. **Load the MNIST dataset** using `tensorflow.keras.datasets`
2. **Preprocess the data**:
   - Normalize pixel values to [0, 1]
   - Flatten the 28x28 images into 1D arrays of 784 values
3. **Build the neural network** using Keras Sequential API
4. **Compile the model** with optimizer, loss, and metrics
5. **Train the model** on training data
6. **Evaluate** on test data
7. **Visualize predictions** on sample test images

---

## 📈 Sample Result (After Training)

```text
Test Accuracy: 97.8%
