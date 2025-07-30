# sign-language-detection
# 🤟 Sign Language Recognition using LSTM

This repository contains a deep learning model for recognizing sign language gestures from video using LSTM-based neural networks and the MediaPipe framework.

## 📌 Overview

This project focuses on recognizing American Sign Language (ASL) gestures from video clips and classifying them into one of 10 predefined words. It aids communication for individuals with hearing impairments.

## 📂 Dataset

- **Name**: [WLASL Dataset](https://dxli94.github.io/WLASL/)
- **Description**: A large-scale dataset for Word-Level ASL recognition.
- **Subset Used**: 10 classes — `['book', 'drink', 'computer', 'before', 'chair', 'go', 'clothes', 'who', 'candy', 'cousin']`.

## 🛠️ Technologies

- Python
- TensorFlow / Keras
- MediaPipe
- NumPy, Pandas
- OpenCV

## 📈 Input Format

- Each video is divided into 30 frames.
- Each frame includes 258 landmarks (from hands, pose, and face).
- Input to the model is a `30 × 258` feature matrix.

## 🧠 Model Architecture

A Sequential LSTM model is used:
- Optimizer: Adam  
- Loss Function: Categorical Crossentropy  
- Accuracy: ~53.5%

## 🚀 How It Works

1. Load video and break it into frames.
2. Use MediaPipe to extract hand/pose/face landmarks from each frame.
3. Feed sequence of extracted features into LSTM model.
4. Output predicted action word.
