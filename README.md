# README: Human Activity Recognition Using IMU Sensor

## Overview

This project focuses on **Human Activity Recognition (HAR)** using data collected from a **triaxial accelerometer IMU sensor**. The dataset contains activity data from 30 different subjects with ages ranging from 10 to 45 years (11 females and 19 males). Subjects performed 5 different activities (normal walk, walk on the toe, jogging, sit-ups, and walking downstairs), and the IMU sensor was placed at the umbilical region to capture the acceleration data. The data was then pre-processed using filtering techniques and fed into deep learning models (CNN and CNN-LSTM) to classify these activities.

## Dataset Description

The dataset consists of the following features:

1. **UID**: User ID (unique identifier for each subject)
2. **Timestamp**: Time of data recording
3. **Operation**: Type of activity performed
4. **X, Y, Z accelerations**: Accelerometer readings in three axes
5. **Activity Label**: Labels for the different activities (e.g., normal walk, walk on the toe, etc.)

The sensor data was recorded for each subject performing the 5 activities for 20 seconds each.

## Key Activities

The following five activities were recorded:

1. **Normal Walk**
2. **Walk on the Toe**
3. **Jogging**
4. **Sit-ups**
5. **Walking Downstairs**

These activities were chosen due to their close resemblance to one another, which makes classification more challenging.

## Data Preprocessing

The collected raw sensor data was pre-processed using various filtering techniques to remove noise and normalize the acceleration data. The data was then vectorized into one-hot encoded format to prepare it for deep learning models.

## Models Used

### CNN (Convolutional Neural Network)

- **Purpose**: CNN is used to extract spatial features from the time-series accelerometer data.
- **Working**: The data is split into frames, and convolutional filters are applied to identify the most relevant features for classification.

### CNN-LSTM (Convolutional Neural Network with Long Short-Term Memory)

- **Purpose**: CNN is used for feature extraction, and LSTM is employed to capture the temporal dependencies in the data.
- **Working**: CNN extracts features from the input data, which are then passed to LSTM layers for learning the time-based patterns and making the final classification.

### Performance Metrics

The performance of both models was evaluated using the following metrics:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**

The CNN model achieved an accuracy of 87%, while the CNN-LSTM model improved performance to 90%.

## Results

- The **CNN model** achieved an accuracy of **87%**.
- The **CNN-LSTM model** boosted the accuracy to **90%**.
- The **Confusion Matrix** and **Classification Report** showed that both models performed well in distinguishing between similar activities, although some errors were made between **normal walk** and **walk on the toe**.
- **CNN-LSTM** outperformed **CNN** in terms of classification accuracy, precision, and recall.

## Future Work

- **Data Collection**: More diverse data can be collected from a larger group of subjects to improve the models.
- **Computer Vision-based HAR**: Future research could explore computer vision-based HAR using **Microsoft Kinect** for a multi-view environment and gait analysis.
- **Multi-sensor Systems**: Combining multiple sensors could improve accuracy, though the current work focuses on a single sensor mimicking smartphone-based data collection.

## Conclusion

This work demonstrates the potential of deep learning models, particularly **CNN** and **CNN-LSTM**, in classifying human activities based on sensor data. By using a single **IMU sensor**, the proposed solution successfully distinguishes between five closely related activities, achieving high classification accuracy and robustness. The results indicate the models' ability to generalize to diverse subjects with different health conditions.

