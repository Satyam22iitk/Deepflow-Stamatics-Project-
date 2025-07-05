# 🐶 Dog Breed Identification – Major Assignment 2

This project is part of the Deep Learning Specialization (Week 6 – CNNs) and involves building a deep learning model to identify the **breed of a dog** from an image using **Convolutional Neural Networks (CNNs)** and **Transfer Learning** with **MobileNetV2**.

---

## 📁 Files Included

- `cnn_model_full.h5` – Trained model using full training set
- `submission.csv` – Kaggle-compatible test predictions
- `DogBreed_CNN.ipynb` – Jupyter Notebook with complete pipeline
- `README.md` – Project overview and instructions

---

## 🧠 Model Architecture

- **Base Model**: MobileNetV2 (pre-trained on ImageNet)
- **Custom Layers**:
  - `GlobalAveragePooling2D`
  - `Dense(128, activation='relu')`
  - `Dense(num_classes, activation='softmax')`
- **Transfer Learning Strategy**:
  - Feature extraction using MobileNetV2 (frozen base)
  - Trained only the top classification layers

---

## 🔁 Dataset

- Source: [Dog Breed Identification | Kaggle](https://www.kaggle.com/c/dog-breed-identification/)
- Total Classes: 120 dog breeds
- Training Images: ~10,000
- Test Images: ~10,000 (no labels)
- Format: `.jpg` images with ID-based filenames

---

## 📊 Performance

| Metric                 | Value        |
|------------------------|--------------|
| **Final Validation Accuracy** | **77.65%**    |
| Epochs Trained         | 10           |
| Batch Size             | 32           |
| Input Image Size       | 224 × 224    |

---

