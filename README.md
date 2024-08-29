# CNN Image Classification Project

This project involves building, training, and deploying Convolutional Neural Network (CNN) models for image classification. The code is organized into three main parts: image preprocessing, model building, training, and ensemble learning.

## Table of Contents

- [Introduction](#introduction)
- [Preprocessing](#preprocessing)
- [Model Building](#model-building)
- [Training](#training)
- [Ensemble Learning](#ensemble-learning)
- [Usage](#usage)
- [License](#license)

## Introduction

This project aims to classify images using CNN models. It includes three key stages: preprocessing images, building CNN models, and applying ensemble learning techniques to improve classification accuracy. Additionally, the ensemble model detects and labels outlier images that do not belong to the training set.

## Preprocessing

The first part of the code involves preprocessing the images by standardizing them. Standardization helps the model process images more efficiently by ensuring consistent input data.

## Model Building

Three CNN models were built based on training results and existing research:

1. **First CNN Model:** Filters used are 32, 64, 128, and 256.
2. **Second CNN Model:** Filters used are 64, 128, 128, 256, 256, 512, and 512.
3. **Third CNN Model:** Two additional convolutional 2D layers, with 64 and 128 filters, respectively, were added to the second model.

## Training

During training, the images were divided into training and validation sets with an 85:15 ratio. A checkpoint mechanism was implemented to monitor the learning rate. If the validation loss does not decrease within 10 epochs, the learning rate is reduced to 70% of its initial value.

## Ensemble Learning

Ensemble learning combines the classification results from multiple CNN models to achieve higher accuracy. Two methods are used:

- **Majority Voting:** Combines predictions from multiple models to determine the final classification.
- **Average:** Averages the probabilities from different models to make the final decision.

Additionally, the ensemble model is designed to identify and label outlier images (images not seen during training) with a label of `-1`. A probability threshold of 0.5 is set; if the classification probability is lower than this threshold, the image is labeled `-1`.

## Usage

To use this project, follow these steps:

1. **Preprocess the Images:** Run the preprocessing script to standardize the images.
2. **Build and Train the Models:** Train the three CNN models using the provided code.
3. **Apply Ensemble Learning:** Combine the trained models using majority voting or averaging techniques to classify new images and detect outliers.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
