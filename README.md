 VGG16 vs ResNet50: CIFAR-10 Image Classification

## Project Overview

This project presents a comparative study of two widely used Convolutional Neural Network (CNN) architectures, VGG16 and ResNet50, for image classification using the CIFAR-10 dataset. The primary objective is to evaluate the effectiveness of both pretrained architectures when used for feature extraction and classification.

Both models use pretrained ImageNet weights, with their original classification layers removed. The extracted features are passed through a custom classification head consisting of Global Average Pooling, Batch Normalization, Dropout, and a final Dense layer for classifying the ten CIFAR-10 categories.

## Objectives

The main objectives of this project are:

* To compare the performance of VGG16 and ResNet50 on the CIFAR-10 dataset.
* To understand the application of transfer learning and feature extraction using pretrained CNN architectures.
* To develop a custom classification head for CIFAR-10 image classification.
* To evaluate both models using test accuracy and test loss.
* To analyze the differences between VGG16 and ResNet50 in terms of architecture and classification performance.

## Models Used

### VGG16

VGG16 is a deep convolutional neural network developed by the Visual Geometry Group. It uses multiple 3×3 convolutional layers followed by pooling layers. Its simple and consistent architecture makes it a widely used model for image classification and feature extraction. However, VGG16 contains a relatively large number of parameters.

### ResNet50

ResNet50 is a 50-layer deep convolutional neural network that introduces residual connections, also known as skip connections. These connections allow information and gradients to flow more effectively through deep networks, helping to address the vanishing-gradient problem. ResNet50 provides powerful feature representations while being more parameter-efficient than traditional architectures such as VGG16.

## Methodology

The CIFAR-10 dataset is used for training and evaluating both models. Since the pretrained models were originally trained on ImageNet, the input images are resized and preprocessed according to the requirements of the respective architectures.

The convolutional bases of VGG16 and ResNet50 are initially kept frozen and used as pretrained feature extractors. A custom classification head is then added to classify the extracted features into the ten CIFAR-10 classes.

The overall architecture is:

```text
Input Image
     |
     v
Pretrained VGG16 / ResNet50
     |
     v
Global Average Pooling
     |
     v
Batch Normalization
     |
     v
Dropout
     |
     v
Dense Layer (10 Classes)
     |
     v
Class Prediction
```

The same dataset, preprocessing strategy, and classification head are used for both models to provide a fair comparison.

## Evaluation

The performance of VGG16 and ResNet50 is evaluated on the CIFAR-10 test dataset. The comparison is based on:

* Test Accuracy
* Test Loss
* Training and Validation Performance
* Feature Extraction Capability
* Overall Classification Performance

The results are analyzed to determine which architecture provides better performance for the given classification task.

## Technologies and Tools

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* CIFAR-10 Dataset
* VGG16
* ResNet50
* Transfer Learning

## Project Structure

```text
VGG-vs-ResNet50/
│
├── VGG16_CIFAR10.ipynb
├── ResNet50_CIFAR10.ipynb
├── README.md
└── requirements.txt
```

## Conclusion

This project provides a practical comparison between VGG16 and ResNet50 for CIFAR-10 image classification using transfer learning. By applying the same dataset, preprocessing pipeline, and custom classification head to both pretrained architectures, the project evaluates their relative classification performance and demonstrates the practical differences between traditional CNN architectures and residual networks.
