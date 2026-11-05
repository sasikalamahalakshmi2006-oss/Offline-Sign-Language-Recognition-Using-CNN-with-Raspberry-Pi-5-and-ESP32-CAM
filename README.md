# Offline Sign Language Recognition Using CNN with Raspberry Pi 5 and ESP32-CAM

## 📌 Project Overview

This project presents an offline sign language recognition system that uses Deep Learning and Computer Vision to recognize hand gestures and convert them into readable text.

The system uses an ESP32-CAM to capture hand gesture images and a Raspberry Pi 5 for processing and CNN-based gesture recognition. The recognized output is displayed through an LCD.

The main objective is to develop an affordable and accessible communication system that helps bridge the communication gap between sign language users and non-sign language users.

## 🎯 Objectives

- Develop an offline sign language recognition system.
- Capture hand gestures using ESP32-CAM.
- Train and implement a Convolutional Neural Network (CNN).
- Recognize predefined hand gestures accurately.
- Convert recognized gestures into text.
- Display the recognized output on an LCD.

## 🛠️ Technologies Used

### Hardware
- Raspberry Pi 5
- ESP32-CAM (OV2640)
- LCD Display

### Software
- Python
- TensorFlow / Keras
- OpenCV
- CNN (Convolutional Neural Network)
- TensorFlow Lite

## ⚙️ System Architecture

1. Image Acquisition: ESP32-CAM captures hand gesture images.
2. Image Processing: Captured images are prepared for recognition.
3. Gesture Recognition: The trained CNN model predicts the corresponding gesture.
4. Text Conversion: The predicted gesture is converted into readable text.
5. Output Display: The recognized text is displayed on the LCD.

## 🧠 Deep Learning Model

A Convolutional Neural Network (CNN) is used to classify hand gesture images.

The project includes trained model formats:

- `final_sign_language_model.keras`
- `sign_language_int8.tflite`

## ✨ Key Features

- Offline gesture recognition.
- CNN-based hand gesture classification.
- ESP32-CAM image acquisition.
- Raspberry Pi 5 processing.
- Real-time text output.
- LCD-based output display.

## 📊 Supported Gestures

The trained CNN model recognizes 35 classes, including:

### Digits
1, 2, 3, 4, 5, 6, 7, 8, 9

### Alphabets
A, B, C, D, E, F, G, H, I, J, K, L, M,
N, O, P, Q, R, S, T, U, V, W, X, Y, Z

**Total Classes: 35**

## 🚀 Future Enhancements

- Expand the number of supported sign language gestures.
- Improve recognition speed and accuracy.
- Integrate speech output.
- Develop a more comprehensive sign language vocabulary.
- Improve accessibility and usability.

## 👩‍💻 Project Team

**Project developed as part of the Final Year Academic Project.**

## 📄 License

This project is currently available for educational and research purposes.
