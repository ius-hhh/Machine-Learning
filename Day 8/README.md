# 🧠 Day 8 – CNN Image Classification (CIFAR-10)

Welcome to Day 8 of the **"30 Days, 30 Machine Learning Projects"** challenge.  
Today, we build a **Convolutional Neural Network (CNN)** using TensorFlow/Keras to classify images from the **CIFAR-10 dataset**, a benchmark dataset containing small images from 10 object categories.

---

## 📊 Dataset

The **CIFAR-10** dataset contains:
- 60,000 color images (32x32 pixels) in 10 classes
- 50,000 training images and 10,000 test images
- Categories:  
  `airplane`, `automobile`, `bird`, `cat`, `deer`, `dog`, `frog`, `horse`, `ship`, `truck`

---

## 🧠 Concepts Covered

- Convolutional Neural Networks (Conv2D, MaxPooling)
- Flattening and Dense layers for classification
- Dropout & Batch Normalization to prevent overfitting
- Softmax activation for multi-class outputs
- Training-validation splitting
- Model evaluation on test set
- Visualization of accuracy and predictions

---

## 🛠️ Tools & Libraries Used

- Python
- TensorFlow / Keras
- Matplotlib & Seaborn
- NumPy

---

## 📌 Objective

Build a CNN model that learns to classify images from the CIFAR-10 dataset with high accuracy.

---

## 📈 Model Summary

The model consists of:
- 3 Convolutional blocks with BatchNormalization and MaxPooling
- 1 Dense hidden layer with Dropout
- 1 Output layer with 10-class Softmax

Trained over 15 epochs with 64-image batch size and 20% validation split.

---

## ✅ Evaluation

- Model is evaluated on the CIFAR-10 test set (10,000 images).
- Final test accuracy: **~66%** (can be improved with augmentation or transfer learning)
- Visual check of predictions via sample test images

---

## 📊 Sample Output Visualization

```python
# Shows 10 test images with true and predicted class names
