# ✍️ Day 11 – Image Classification with Transfer Learning (Cats vs Dogs)

Welcome to **Day 11** of the **"30 Days, 30 Machine Learning Projects"** challenge!

In this project, we build an image classifier to distinguish between **cats** and **dogs** using **transfer learning** with the pretrained **VGG16** convolutional neural network. Transfer learning helps us leverage a powerful pretrained model and adapt it to a new task with limited data, saving training time and improving accuracy.

---

## 📌 Project Objective

The goal is to create and train a model that classifies images of cats and dogs by:

- Using a pretrained VGG16 model as a fixed feature extractor
- Adding custom classification layers on top
- Training the new layers with the base model frozen
- Fine-tuning some of the top convolutional layers for better performance
- Loading and preprocessing images from directories using `ImageDataGenerator`

---

## 📊 Dataset: Cats vs Dogs Filtered

The dataset contains images organized in the following folder structure:

cats_and_dogs_filtered/
├── train/
│ ├── cats/
│ └── dogs/
├── validation/
│ ├── cats/
│ └── dogs/


- Images resized to 160x160 pixels
- Batches of 32 images loaded for training and validation
- Folder names (`cats`, `dogs`) are used as class labels by Keras

---

## 🧠 Concepts Covered

- 🧹 **Data Preprocessing**: Rescaling pixel values, loading images by folder structure  
- 🔁 **Transfer Learning**: Using VGG16 pretrained on ImageNet without its top layers  
- 🧱 **Model Building**: Adding Flatten, Dense, and Dropout layers  
- ⚙️ **Freezing & Fine-tuning**: First freeze base model, then unfreeze some layers for fine-tuning  
- 📈 **Model Evaluation**: Plotting training/validation accuracy and loss  
- 🧪 **Prediction**: Binary classification using sigmoid activation and binary crossentropy loss  

---

## 🛠️ Tools & Libraries Used

- 🐍 Python 3.x  
- 🧠 TensorFlow/Keras  
- 📊 Matplotlib for visualization  

---

## 🧪 Model Architecture

### Input Layer
- Input shape: (160, 160, 3) RGB images  

### Base Model
- Pretrained VGG16 convolutional base (ImageNet weights)  
- Top layers removed (`include_top=False`)  
- Base layers frozen during initial training  

### Custom Top Layers
- Flatten layer  
- Dense layer with 256 neurons and ReLU activation  
- Dropout layer (rate 0.5)  
- Dense output layer with 1 neuron and sigmoid activation (binary classification)  

### Compile Settings
- Loss function: Binary crossentropy  
- Optimizer: Adam (with learning rates 0.0001 for initial training, 0.00001 for fine-tuning)  
- Metrics: Accuracy  

---

## 🚀 Steps Involved

1. Load and preprocess images using `ImageDataGenerator` with rescaling  
2. Create data generators from folders for training and validation sets  
3. Load VGG16 pretrained model without top layers and freeze it  
4. Add custom classification layers on top  
5. Compile and train the model for 5 epochs  
6. Plot training and validation accuracy and loss  
7. Unfreeze last 4 convolutional layers and fine-tune with lower learning rate for 3 epochs  
8. Evaluate model performance on validation data  

---

## 📈 Sample Result (After Training)

```text
Epoch 5/5
Train Accuracy: ~95%
Validation Accuracy: ~88%

Epoch 3/3 (Fine-tuning)
Train Accuracy: ~89%
Validation Accuracy: ~92%

Final Validation Accuracy: 0.9108
