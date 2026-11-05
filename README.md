# Offline Sign Language Recognition Using CNN with Raspberry Pi 5 and ESP32-CAM

## 📌 Project Overview

This project presents an offline sign language hand gesture recognition system using Deep Learning and Computer Vision. It captures hand gestures through an ESP32-CAM and uses a Convolutional Neural Network (CNN) running on a Raspberry Pi 5 to classify gestures and convert them into readable text.

The system captures images using the ESP32-CAM (OV2640), transfers them to the Raspberry Pi 5 for image processing and CNN-based classification, and displays the recognized character on an LCD.

The primary objective is to develop an affordable and accessible communication solution that helps reduce the communication gap between sign language users and non-sign language users.

## 🎯 Objectives

- Develop an offline hand gesture recognition system.
- Capture hand gesture images using ESP32-CAM.
- Implement a CNN model for gesture classification.
- Recognize 35 predefined alphabet and digit gestures.
- Convert recognized gestures into readable text.
- Display the classification output on an LCD.
- Perform gesture recognition using Raspberry Pi 5.

## 🏗️ System Architecture

The system follows the workflow below:

1. **Image Acquisition:** ESP32-CAM with OV2640 captures hand gesture images at 240 × 240 resolution.
2. **Image Transfer:** Captured images are made available to the Raspberry Pi through the HTTP capture endpoint (`/capture`).
3. **Image Preprocessing:** The captured image is processed and resized to the CNN input dimensions of 128 × 128 × 3.
4. **Gesture Recognition:** The trained CNN model performs inference and predicts one of the 35 gesture classes.
5. **Text Conversion:** The predicted class is mapped to its corresponding alphabet or digit.
6. **Output Display:** The recognized character is displayed through an LCD connected to the processing system.

## 🛠️ Technologies Used

### Hardware

- Raspberry Pi 5
- ESP32-CAM (OV2640)
- LCD Display

### Software and Frameworks

- Python
- TensorFlow
- Keras
- TensorFlow Lite
- OpenCV
- Convolutional Neural Network (CNN)

## 🧠 Deep Learning Model

A Convolutional Neural Network (CNN) is used to classify static hand gesture images.

The project contains two trained model formats:

| Model | Description |
|---|---|
| `final_sign_language_model.keras` | Original trained Keras model |
| `sign_language_int8.tflite` | INT8 quantized TensorFlow Lite model |

### Model Specifications

| Parameter | Value |
|---|---|
| Model architecture | CNN |
| Input dimensions | 128 × 128 × 3 |
| Output classes | 35 |
| Input format | INT8 for the quantized TFLite model |
| Captured image resolution | 240 × 240 |
| Inference platform | Raspberry Pi 5 |

The quantized TensorFlow Lite model is intended for efficient edge inference.

## 📊 Supported Gestures

The trained CNN model recognizes 35 predefined gesture classes.

### Digits (9 Classes)

1, 2, 3, 4, 5, 6, 7, 8, 9

### Alphabets (26 Classes)

A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

**Total: 35 Classes**

## ✨ Key Features

- Offline hand gesture recognition.
- CNN-based image classification.
- ESP32-CAM-based image acquisition.
- Raspberry Pi 5 edge processing.
- INT8 quantized TensorFlow Lite model.
- Recognition of 26 alphabets and 9 digits.
- LCD-based text output.

## 📁 Repository Structure

```text
Offline-Sign-Language-Recognition/
│
├── CameraWebServer/
│   ├── CameraWebServer.ino
│   ├── app_httpd.cpp
│   ├── board_config.h
│   ├── camera_index.h
│   └── camera_pins.h
│
├── models/
│   ├── README.md
│   ├── final_sign_language_model.keras
│   └── sign_language_int8.tflite
│
└── README.md
```

## 🚀 Future Enhancements

- Expand the supported gesture vocabulary.
- Improve recognition speed and classification accuracy.
- Integrate speech output for recognized gestures.
- Develop continuous gesture recognition.
- Implement sentence formation from recognized gestures.
- Improve the accessibility and usability of the system.

## 👩‍💻 Project Team

**Final Year Academic Project**

## 📄 Usage Note

This project is intended for educational and research purposes. Please contact the project authors before redistributing or using the implementation commercially.
