# Telugu Speech Emotion Recognition using 1D CNN

## Overview

This project implements a **Speech Emotion Recognition (SER)** system for the Telugu language using a **1D Convolutional Neural Network (CNN)**. The model analyzes speech audio recordings and classifies them into different emotional categories based on extracted acoustic features.

The system uses a combination of **MFCC**, **Chroma**, and **Mel Spectrogram** features to capture emotional characteristics from speech signals and employs a deep CNN architecture for classification.

---

## Features

* Telugu speech emotion classification
* Audio feature extraction using Librosa
* MFCC, Chroma, and Mel Spectrogram feature fusion
* Audio data augmentation techniques
* Deep 1D CNN architecture
* PyTorch implementation
* Emotion prediction on unseen audio samples

---

## Emotion Classes

The model is trained to recognize the following emotions:

* Happy
* Sad
* Angry
* Fear
* Disgust
* Neutral

---

## Project Workflow

### 1. Dataset Preparation

Audio samples are organized into emotion-specific folders:

```text
emotions_dataset/
│
├── happy/
├── sad/
├── angry_modified/
├── fear/
├── disgust/
└── neutral/
```

### 2. Feature Extraction

For every audio file, the following features are extracted:

#### MFCC (Mel Frequency Cepstral Coefficients)

Captures speech characteristics that closely resemble human auditory perception.

#### Chroma Features

Represent pitch and harmonic information present in speech.

#### Mel Spectrogram

Captures frequency-energy distribution useful for emotion recognition.

### 3. Feature Fusion

The extracted features are combined into a single feature vector:

```text
MFCC + Chroma + Mel Spectrogram
```

Resulting Feature Size:

```text
180 Features
```

### 4. Data Augmentation

To improve model generalization:

* Noise Injection
* Time Shifting

### 5. Model Training

The extracted features are used to train a 1D CNN model using PyTorch.

### 6. Emotion Prediction

For a new speech sample:

```text
Audio Input
      ↓
Feature Extraction
      ↓
CNN Model
      ↓
Emotion Prediction
```

---

## CNN Architecture

```text
Input Layer (180 Features)
        ↓
Conv1D (1 → 16)
        ↓
Conv1D (16 → 32)
        ↓
Max Pooling
        ↓
Conv1D (32 → 64)
        ↓
Conv1D (64 → 128)
        ↓
Max Pooling
        ↓
Conv1D (128 → 128)
        ↓
Conv1D (128 → 128)
        ↓
Max Pooling
        ↓
Conv1D (128 → 128)
        ↓
Conv1D (128 → 128)
        ↓
Max Pooling
        ↓
Dropout (0.5)
        ↓
Flatten
        ↓
Fully Connected Layer
        ↓
Softmax Output
```

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Pandas
* Librosa
* Scikit-Learn
* Matplotlib
* Google Colab

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/telugu-speech-emotion-recognition.git
cd telugu-speech-emotion-recognition
```

Install required packages:

```bash
pip install torch librosa numpy pandas matplotlib scikit-learn
```

---

## Running the Project

Open the notebook:

```bash
jupyter notebook _cnn4setstelugu.ipynb
```

or

```bash
Google Colab
```

Run all cells sequentially.

---

## Training Configuration

| Parameter     | Value            |
| ------------- | ---------------- |
| Optimizer     | Adam             |
| Loss Function | CrossEntropyLoss |
| Learning Rate | 0.001            |
| Epochs        | 100              |
| Batch Size    | 64               |

---

## Advantages

* Supports Telugu language emotion analysis
* Lightweight compared to large transformer models
* Robust through audio augmentation
* Effective feature extraction strategy
* Suitable for real-time emotion recognition applications

---

## Applications

* Human-Computer Interaction
* Virtual Assistants
* Mental Health Monitoring
* Customer Service Analytics
* Educational Systems
* Smart Call Centers
* Voice-Based Recommendation Systems

---

## Future Enhancements

* Add more Telugu emotion datasets
* Support real-time microphone input
* Deploy as a web application
* Improve accuracy using CNN-LSTM hybrid models
* Add multilingual emotion recognition

---

## Results

The model successfully classifies Telugu speech into multiple emotional categories using deep learning and audio signal processing techniques.

---

## Author

**Udata Lekhana Surya Bhanu**

B.Tech Project – Speech Emotion Recognition using Deep Learning

---

## License

This project is intended for academic and educational purposes.
