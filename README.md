# brain_tumour
# 🧠 Brain Tumor Classification Using Deep Learning

This project uses a Convolutional Neural Network (CNN) to classify MRI brain scan images into two categories: **"Yes Tumor"** or **"No Tumor"**. A user-friendly web app interface is built with **Streamlit** for interactive image upload and classification.

---

## 🔍 Features

- Upload MRI brain scan images
- Predicts presence of a brain tumor
- Clean, intuitive UI with gradient background
- Built using TensorFlow, Keras, OpenCV, and Streamlit

---

## 🖼️ Dataset

- The dataset is divided into two folders:  
  - `yes/` — Contains MRI images with tumors  
  - `no/` — Contains MRI images without tumors  
- All images are resized to **64x64 pixels** for model input.

---

## 🏗️ Model Architecture

- **Input Layer**: (64x64x3)
- **3 Convolutional Blocks**:
  - Conv2D → ReLU → MaxPooling2D
- **Fully Connected Layers**:
  - Flatten → Dense(64) → Dropout → Dense(2) with Softmax

Compiled with:
```python
loss = 'categorical_crossentropy'
optimizer = 'adam'
metrics = ['accuracy']
