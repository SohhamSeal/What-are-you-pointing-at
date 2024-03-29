# What are you pointing at ??

This repository contains analytics-ready data for EMG (Electromyography) signal gesture recognition. The dataset includes raw EMG data collected from 36 subjects using a MYO Thalmic bracelet while performing various hand gestures. The dataset is intended to facilitate research and experimentation in the field of gesture recognition and classification.

## About the Dataset

### Context
If you're new to gesture recognition and classification, acquiring raw data and formatting it appropriately can be challenging. This dataset aims to alleviate that challenge by providing analytics-ready data for experimentation. Contributors are encouraged to explore creative approaches and share their findings through kernels and analyses.

### Content
The dataset consists of raw EMG data recorded for 36 subjects performing static hand gestures. Each subject performed two series of gestures, each containing six to seven basic gestures. The data includes the following columns:

1. **Time**: Time in milliseconds.
2-9. **Channel**: Eight EMG channels from the MYO Thalmic bracelet.
10. **Class**: Labels for gestures, with the following mappings:
   - 0: Unmarked data
   - 1: Hand at rest
   - 2: Hand clenched in a fist
   - 3: Wrist flexion
   - 4: Wrist extension
   - 5: Radial deviations
   - 6: Ulnar deviations
   - 7: Extended palm (not performed by all subjects)
11. **Label**: Subject identifier (1 to 36), indicating the performer of the experiment.

For more detailed information, refer to the [Readme file](https://archive.ics.uci.edu/ml/datasets/EMG+data+for+gestures) of the original dataset.

### Acknowledgements
We extend our gratitude to the UCI Machine Learning Repository and the researchers who made this open data available for exploration and research.

## Sliding Window Fourier Transform and Model Implementation

To implement sliding window Fourier transform and utilize different deep learning models such as AlexNet, ResNet18, VGG16, VGG19, etc., we can follow these steps:

1. **Preprocess Data**: Prepare the dataset by applying sliding window Fourier transform to convert the raw EMG signals into a format suitable for input to deep learning models.
   
2. **Model Modification**: Modify the CNN and max-pooling layers of the chosen models to accommodate 1D input instead of 2D while keeping the rest of the architecture unchanged.

3. **Training**: Train the modified models on the preprocessed EMG data for gesture recognition tasks.

4. **Evaluation**: Evaluate the performance of the trained models using appropriate metrics and compare their effectiveness in gesture recognition.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/emg-signal-gesture-recognition.git
