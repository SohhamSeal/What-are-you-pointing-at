# What are you pointing at ??

## EMG Signal Gesture Recognition

This repository contains code and resources for conducting gesture recognition using EMG (Electromyography) signal data. The dataset used in this project can be found on Kaggle [here](https://www.kaggle.com/datasets/sojanprajapati/emg-signal-for-gesture-recognition).

## About the Dataset

The dataset consists of raw EMG data recorded from individuals wearing a MYO Thalmic bracelet on their forearm while performing various hand gestures. Each gesture is labeled with a specific category, and the dataset includes information such as time stamps and channel readings from the sensors on the bracelet.

## Work Conducted

In this project, we conducted the following steps to preprocess the data and classify the gestures:

1. **Data Preprocessing**:
   - Cleaned the dataset to handle any missing or erroneous data points.
   - Applied sliding window Fourier transform to segment the EMG signals into smaller windows, which helps capture temporal patterns in the data.
   - Extracted features from the Fourier transformed signals to reduce dimensionality and focus on relevant information for classification.

2. **Model Selection**:
   - Experimented with various deep learning models suitable for time-series data classification, including:
     - AlexNet
     - ResNet18
     - Resnet34
     - VGGNET16
     - ZFNET
     - RCCGNET
   - Chose models with architectures capable of handling 1D input data while maintaining the convolutional and pooling layers for feature extraction.

3. **Model Training and Evaluation**:
   - Split the preprocessed data into training and testing sets uisng k-fold Cross Validation.
   - Trained each selected model on the training data using appropriate loss functions and optimization techniques.
   - Evaluated the trained models on the test data to assess their performance in classifying different gesture categories.
   - Utilized metrics such as accuracy, precision, recall and F1-score to measure the classification performance of each model.
