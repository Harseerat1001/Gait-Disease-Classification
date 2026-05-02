# 🧠 Gait Disease Classification using CNN-BiLSTM

This project focuses on classifying human gait patterns into **Healthy**, **Parkinson’s**, and **Huntington’s** using deep learning techniques on time-series foot pressure data.

---

## 📌 Overview

Gait (walking pattern) carries important information about neurological health. This project uses a **hybrid CNN-BiLSTM model** to learn both spatial and temporal features from gait signals and classify them into different categories.

---

## 📊 Dataset

- Source: PhysioNet Gait Dataset  
- Type: Time-series foot pressure signals  
- Classes:
  - Healthy  
  - Parkinson’s  
  - Huntington’s  

Each sample consists of:
- **Left foot pressure**
- **Right foot pressure**
- Recorded over time

---

## ⚙️ Methodology

1. Load gait recordings  
2. Segment signals into fixed-length windows (900 time steps)  
3. Feed data into CNN-BiLSTM model  
4. Train model for classification  
5. Evaluate performance using standard metrics  

---

## 🧠 Model Architecture

- Conv1D (128 filters, kernel=5)  
- Batch Normalization  
- MaxPooling  
- Conv1D (64 filters, kernel=3)  
- Batch Normalization  
- MaxPooling  
- Bidirectional LSTM (64 units)  
- Dropout (0.4)  
- Dense (32)  
- Output Layer (Softmax - 3 classes)

---

## 📈 Results

- Accuracy: **92%**
- Balanced Precision, Recall, and F1-score across all classes

---

## 🔍 Explainability

Grad-CAM is used to visualize important regions of the gait signal that influence model predictions.

---

## 🛠️ Tech Stack

- Python  
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib  

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/yourusername/your-repo

# Navigate to project folder
cd your-repo

# Install dependencies
pip install -r requirements.txt

# Run the notebook or script
