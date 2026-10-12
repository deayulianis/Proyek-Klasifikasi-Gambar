# 🖼️ Intel Image Classification CNN

An end-to-end computer vision project leveraging a custom Convolutional Neural Network (CNN) architecture to classify natural scenery images into six distinct categories: **buildings, forest, glacier, mountain, sea, and street**.

---

## 🚀 Project Overview
This project processes image datasets from Kaggle (`intel-image-classification`), performs automated data merging, splits data into training, validation, and test sets, trains a custom multi-layer CNN model, evaluates its performance using confusion matrices and classification reports, and exports the trained model into production-ready formats (**TF-Lite** and **TensorFlow.js**).

---

## 📊 Model Performance Metrics
* **Training Accuracy:** 94.87% (Loss: 0.1539 | 11,920 Images)
* **Validation Accuracy:** ~84.37% (Loss: 0.5487 | 2,552 Images)
* **Test Accuracy:** 85.01% (Loss: 0.4134 | 2,562 Images)

### Classification Report Summary (Test Set):
* **Forest:** F1-Score 0.95 (Precision: 0.93, Recall: 0.97)
* **Sea:** F1-Score 0.87 (Precision: 0.90, Recall: 0.85)
* **Buildings:** F1-Score 0.83 (Precision: 0.76, Recall: 0.91)
* **Street:** F1-Score 0.84 (Precision: 0.90, Recall: 0.79)
* **Mountain:** F1-Score 0.81 (Precision: 0.84, Recall: 0.79)
* **Glacier:** F1-Score 0.80 (Precision: 0.80, Recall: 0.80)

---

## ⚙️ Development Workflow
1. **Data Loading & Merge:** Using Kaggle API to download and merge test/train directories.
2. **Preprocessing & Split:** Resizing images, normalizing pixel values (`rescale=1./255`), and splitting into **70% Train, 15% Validation, 15% Test**.
3. **CNN Architecture:** Built using sequential layers of `Conv2D`, `MaxPooling2D`, `Flatten`, `Dropout (0.4)`, and `Dense (Softmax)`.
4. **Model Training:** Trained over 15 epochs using the Adam optimizer and categorical cross-entropy loss.
5. **Evaluation & Export:** Evaluated with classification metrics and converted into SavedModel, `.tflite`, and TensorFlow.js formats.

---

## 🛠️ Tech Stack & Libraries
* **Deep Learning:** TensorFlow, Keras, CNN
* **Data Processing & Vision:** OpenCV, Scikit-Image, NumPy, Pandas, ImageDataGenerator
* **Evaluation:** Scikit-Learn (Confusion Matrix, Classification Report)
* **Environment:** Google Colab

---

## 📦 Submission Package Structure
```text
submission/
│
├── saved_model/          # TensorFlow SavedModel format
├── tflite/               # TF-Lite model & label.txt
├── tfjs_model/           # TensorFlow.js format
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
