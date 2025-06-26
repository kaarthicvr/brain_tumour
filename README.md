# Brain Tumor Classification Using Deep Learning

This project uses a Convolutional Neural Network (CNN) to classify MRI brain scan images into two categories: "Yes Tumor" or "No Tumor". A web application built with Streamlit allows users to upload MRI scans and receive real-time predictions.

---

## Features

- Upload MRI brain scan images for classification
- Predicts presence or absence of brain tumors
- Clean and responsive web interface using Streamlit
- Trained using Keras with TensorFlow backend

---

## Dataset

The dataset is organized into two directories:
- `yes/` — MRI images that contain tumors
- `no/` — MRI images without tumors

All images are resized to 64x64 pixels during preprocessing to match the input shape expected by the model.

---

## Model Architecture

The Convolutional Neural Network (CNN) model consists of the following:

- Input shape: (64, 64, 3)
- 3 convolutional layers with ReLU activation and max pooling
- Fully connected dense layer with dropout
- Output layer with 2 classes using softmax activation

Compilation parameters:
```python
loss = 'categorical_crossentropy'
optimizer = 'adam'
metrics = ['accuracy']
