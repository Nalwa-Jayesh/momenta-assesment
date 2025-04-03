# 🎙️ Audio Deepfake Detection

## 📝 Overview
This project implements a deep learning model to detect deepfake audio using Mel Spectrogram features. The model is trained on a dataset containing real and fake audio samples.

## 🚀 Implementation Details

### 🤖 Model Selection
A **ResNet-based architecture** was chosen due to its effectiveness in learning feature representations from spectrograms.

### 🎛️ Data Preprocessing
- 📊 **Mel Spectrograms** are extracted from audio files using `torchaudio.transforms.MelSpectrogram`.
- 🔧 **Fixed Size Processing**: Spectrograms are padded or truncated to ensure a uniform input size.
- 🚫 **Skipping Corrupt Files**: Any unreadable or silent files are automatically skipped to maintain dataset integrity.

### 🏋️‍♂️ Training and Evaluation
- 📌 The dataset is split into **training (80%)**, **validation (10%)**, and **test (10%)** sets.
- ⚡ A standard training loop with **batch normalization and gradient scaling** is used for efficient training.
- 📈 Performance is evaluated using **Accuracy** and **F1-score**.

## 📊 Performance Results
After training the model for **10 epochs**, the evaluation results were:
- ✅ **Test Accuracy**: **92.64%**
- 🎯 **F1-Score**: **92.29%**

## 🔍 Strengths and Weaknesses
### ✅ Strengths:
- The **ResNet model generalizes well** to the dataset.
- Effective use of **spectrogram-based feature extraction**.
- Handles **silent and corrupt files gracefully**.

### ❌ Weaknesses:
- Might struggle with **real-world noisy audio conditions**.
- Requires **computational resources** for training.

## 🔮 Future Improvements
- 🧪 **Experiment with different architectures** like CNN+LSTM.
- 🎵 **Apply data augmentation** techniques for better generalization.
- 🎙️ **Investigate alternative preprocessing techniques** like MFCCs.

## ⚙️ Setup Instructions
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Ensure the dataset is available and formatted correctly.
3. Run `main.ipynb` to **train and evaluate** the model.

## 📦 Dependencies
- 🏗 **PyTorch**
- 🎧 **Torchaudio**
- 🔢 **NumPy**
- 📊 **Pandas**
- 📈 **Matplotlib**

## 🔄 Reproducibility
To reproduce the results:
1. Follow the **setup instructions**.
2. The instructions for data set is in the first few cells of the notebook.
3. Run the **training script** in `momenta_task.ipynb`.
