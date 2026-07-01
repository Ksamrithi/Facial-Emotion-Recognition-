# Emotion Recognition System

## Overview

The Emotion Recognition System is a deep learning-based application that identifies human emotions from facial expressions in images or live webcam feeds. It detects faces, preprocesses them, and predicts the corresponding emotion using a trained Convolutional Neural Network (CNN).

The system can recognize the following emotions:

- Angry
- Disgust
- Fear
- Happy
- Neutral
- Sad
- Surprise

---

## Features

- Real-time emotion detection using webcam
- Emotion prediction from uploaded images
- Face detection using OpenCV
- Deep learning-based emotion classification
- Displays predicted emotion with confidence score
- Simple and user-friendly interface

---

## Technologies Used

- Python 3.x
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Streamlit (if applicable)

---

## Project Structure

```
Emotion-Recognition/
│
├── dataset/
│   ├── train/
│   ├── test/
│
├── models/
│   └── emotion_model.h5
│
├── images/
│
├── app.py                 # Main application
├── train.py               # Model training
├── predict.py             # Image prediction
├── webcam.py              # Live webcam detection
├── requirements.txt
├── README.md
└── utils.py
```

---

## Dataset

The model is trained using the **FER-2013 (Facial Expression Recognition 2013)** dataset.

Dataset contains grayscale facial images of size **48×48** belonging to seven emotion classes.

---

## Model Architecture

The emotion classifier is implemented using a Convolutional Neural Network (CNN) consisting of:

- Convolution Layers
- ReLU Activation
- Max Pooling
- Dropout
- Batch Normalization
- Fully Connected Layers
- Softmax Output Layer

Loss Function:
```
Categorical Crossentropy
```

Optimizer:
```
Adam
```

Evaluation Metric:
```
Accuracy
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/emotion-recognition.git
cd emotion-recognition
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Training the Model

```bash
python train.py
```

The trained model will be saved inside the `models/` directory.

---

## Running the Application

### Predict Emotion from Image

```bash
python predict.py
```

### Real-Time Webcam Detection

```bash
python webcam.py
```

### Streamlit Application

```bash
streamlit run app.py
```

---

## Workflow

1. Capture image from webcam or upload an image.
2. Detect the face using OpenCV.
3. Resize the detected face to 48×48 pixels.
4. Normalize the image.
5. Feed the image into the trained CNN model.
6. Predict the emotion.
7. Display the predicted emotion with confidence.

---

## Sample Output

```
Detected Emotion: Happy
Confidence: 97.6%
```

---

## Future Enhancements

- Multi-face emotion recognition
- Video file emotion detection
- Emotion trend analysis over time
- Speech emotion recognition integration
- Improved accuracy using Vision Transformers (ViT) or EfficientNet
- Deployment on cloud platforms

---

## Requirements

```
tensorflow
opencv-python
numpy
matplotlib
pandas
scikit-learn
streamlit
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## Results

The trained model successfully recognizes facial emotions from both static images and live webcam input. It achieves reliable performance on standard facial expression datasets and demonstrates real-time inference capability.

---

## License

This project is intended for educational and research purposes.
