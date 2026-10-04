VGG16 vs ResNet50 — CIFAR-10 Image Classification
-> Project Overview

This project presents a comparative study of two popular Convolutional Neural Network (CNN) architectures, VGG16 and ResNet50, for image classification using the CIFAR-10 dataset. The main objective is to understand how these architectures perform when used as pretrained feature extractors with a custom classification head.

Both models are initialized with ImageNet pretrained weights, while their original classification layers are removed. The extracted features are then passed through a custom classification head containing Global Average Pooling, Batch Normalization, Dropout, and a final Dense layer for CIFAR-10 classification.

-> Objectives
Compare VGG16 and ResNet50 on the CIFAR-10 dataset.
Explore transfer learning and feature extraction using pretrained CNN models.
Build a custom classification head for CIFAR-10.
Evaluate and compare model performance using accuracy and loss.
Understand the differences between VGG16 and ResNet50 architectures and their effectiveness for image classification.
-> Models Used
VGG16

VGG16 is a deep CNN architecture that uses a sequence of 3×3 convolutional layers followed by pooling layers. It has a simple and uniform architecture but contains a relatively large number of parameters.

ResNet50

ResNet50 is a 50-layer deep CNN that uses residual connections (skip connections) to make training deeper networks easier and reduce the vanishing-gradient problem. It generally provides strong feature extraction capabilities with a more efficient architecture than traditional deep CNNs.

-> Methodology

The CIFAR-10 images are preprocessed and resized to a suitable input size for the pretrained models. The convolutional base of each model is kept frozen and used as a feature extractor. A custom classification head is then added:

Input Image
     ↓
Pretrained VGG16 / ResNet50
     ↓
Global Average Pooling
     ↓
Batch Normalization
     ↓
Dropout
     ↓
Dense Layer (10 Classes)
     ↓
Prediction

The same dataset and classification setup are used for both architectures to make the comparison more consistent.

-> Evaluation

The models are evaluated on the CIFAR-10 test set. Their performance is compared using:

Test Accuracy
Test Loss
Training and Validation Performance
Overall classification performance

The experiment helps determine which pretrained architecture provides better feature representations for the CIFAR-10 classification task.

-> Technologies Used
Python
TensorFlow / Keras
NumPy
Matplotlib
CIFAR-10 Dataset
VGG16
ResNet50
Transfer Learning
