# Traffic Signs Classification

## Overview
This project focuses on building a deep learning model to classify traffic signs into one of 43 different categories. The dataset used is the German Traffic Sign Recognition Benchmark (GTSRB), and the LeNet neural network architecture is implemented for the classification task.

![Traffic Sign Example](https://upload.wikimedia.org/wikipedia/commons/b/b6/UK_traffic_sign_543.svg)

### Problem Statement
The aim is to develop a machine learning model capable of identifying and classifying various traffic signs from images. Such a model can assist autonomous driving systems in recognizing and responding to traffic signs in real-time.

### Dataset
The dataset contains 43 classes, including but not limited to:
- Speed limit signs (e.g., 20km/h, 30km/h, 50km/h)
- Warning signs (e.g., Dangerous curves, Slippery road)
- Mandatory signs (e.g., Keep right, Roundabout mandatory)
- Prohibitory signs (e.g., No passing, No entry)

A complete list of classes is provided within the project notebook.

## Project Features
- **Deep Learning Architecture**: Implementation of LeNet, a convolutional neural network originally developed by Yann LeCun for handwritten digit recognition.
- **Preprocessing**: Image resizing, normalization, image augumentation,coverted the image from rgb to gray as LeNet generally work on gray images
- **Training & Evaluation**: Model training on a labeled dataset with performance evaluation metrics like accuracy.

## Inference
- Trained both the normal data and augumented data  using the LeNet CNN model and we could only achieve 85% accuracy in both cases.
- Generally augumented data ,yields better accuracy but the traffic signals are typically simple and have well-defined shapes and colors. Aggressive augmentations like excessive rotations, shearing, or zooming might distort their core features did not help here




