---
layout: default
title: CIFAR-10 Image Classification
github_url: https://github.com/will51mps0n/Image_CNN/tree/main
---

[← Back to Home](../index.html)

# CIFAR-10 Image Classification: Fully-Connected and Convolutional Neural Networks  
[View Code on GitHub](https://github.com/will51mps0n/Image_CNN/tree/main)

---

## Overview

This project involves training and evaluating two types of neural networks—**Fully-Connected Networks (FCNs)** and **Convolutional Neural Networks (CNNs)**—to classify images from the **CIFAR-10 dataset**, which consists of 60,000 32x32 color images across 10 classes.

Key components include:

1. **FCNet Model:**
   - A simple feedforward neural network utilizing adjustable activation functions.
2. **ConvNet Model:**
   - A deeper convolutional network designed to capture spatial hierarchies in image data.
3. **Hyperparameter Grid Search:**
   - Performed over different learning rates and activation functions to optimize model performance.

---

## Features

### Fully-Connected Network (FCNet):
- Implements multi-layer perceptron architecture.
- Configurable activation functions (`ReLU`, `Sigmoid`).
- Trained using **Adam optimizer** and **CrossEntropyLoss**.
- Evaluates test accuracy on CIFAR-10 dataset.

### Convolutional Neural Network (ConvNet):
- Uses convolutional and pooling layers followed by dense layers.
- Supports flexible activation functions.
- Achieves higher accuracy compared to FCNet by leveraging spatial features.

### Hyperparameter Tuning:
- Conducted grid search across:
  - Learning rates: `1e-7`, `1e-3`, `1`.
  - Activation functions: `ReLU`, `Sigmoid`.
- Best configuration determined by highest test accuracy.

### Visualization:
- Generates plots showing model predictions vs actual labels for sample CIFAR-10 images.

---

## Technologies
- Python
- PyTorch
- Matplotlib
- Grid Search & Hyperparameter Optimization
- Adam Optimizer 
- Cross Entropy Loss


---

[← Back to Home](../index.html)
