

# DeepFER: Facial Emotion Recognition Using Deep Learning

## Project Overview

DeepFER is a deep learning project that uses Convolutional Neural Networks (CNNs) and transfer learning to classify facial expressions into seven emotion categories: angry, disgust, fear, happy, neutral, sad, and surprise.

The project explores a CNN built from scratch and an improved approach using the pretrained MobileNetV2 architecture. The trained model can predict the expression category from an individual facial image.

## Problem Statement

Facial expression recognition is a computer vision task that involves identifying visual patterns associated with different facial expressions. Building an accurate model can be challenging because facial expressions may vary across individuals, lighting conditions, image quality, and backgrounds.

The objective of this project is to develop a deep learning model capable of classifying facial images into seven emotion categories and evaluate its performance using training and validation data.

## Objectives

- Load and preprocess facial images.
- Explore the distribution of the seven emotion classes.
- Develop a CNN model from scratch.
- Apply transfer learning using MobileNetV2.
- Train and evaluate the models.
- Compare the performance of the CNN and transfer-learning approaches.
- Predict facial expression categories for individual images.

## Dataset

The project uses the Facial Expression Recognition dataset available on Kaggle.

**Dataset:** [Facial Expression Recognition – Kaggle](https://www.kaggle.com/datasets/someshwar2410/facial-expression-recognition)

The dataset contains facial images organized into seven emotion classes:

- Angry
- Disgust
- Fear
- Happy
- Neutral
- Sad
- Surprise

The dataset provides separate training and validation folders.

## Methodology

### 1. Dataset Loading and Preprocessing

The dataset was loaded using TensorFlow's `image_dataset_from_directory()` utility.

Images were resized to 224 × 224 pixels and processed in batches. Pixel values were normalized as required by the model's preprocessing pipeline.

### 2. CNN from Scratch

A custom CNN architecture was developed using convolutional layers, max-pooling layers, dense layers, and dropout.

The model was trained to learn facial-expression features directly from the dataset.

### 3. Transfer Learning with MobileNetV2

MobileNetV2 was used as a pretrained feature-extraction architecture.

Transfer learning allows the model to reuse visual features learned from a larger image dataset and adapt them to facial-expression classification.

### 4. Model Evaluation

The model was evaluated using validation accuracy and validation loss. Individual image predictions were also performed to observe the model's output.

## Results

The MobileNetV2 model achieved a validation accuracy of approximately **51.85%** in the current experiment.

This result represents the performance of the current model configuration. Further improvements may be possible through class balancing, data augmentation, hyperparameter tuning, and fine-tuning the pretrained model.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab
- Kaggle

## Future Improvements

- Address class imbalance in the dataset.
- Improve model performance through data augmentation.
- Fine-tune MobileNetV2.
- Evaluate the model using a confusion matrix and classification report.
- Develop a real-time facial-expression recognition application.
- Explore deployment using Streamlit or another application framework.

## Disclaimer

The model predicts facial-expression categories based on visual patterns. Its predictions do not establish a person's actual internal emotional state. The model may also be affected by image quality, lighting, pose, and dataset limitations.

