# AQI Detection Using CNN

## About This Project

This project aims to detect Air Quality Index (AQI) levels using a Convolutional Neural Network (CNN) model. It leverages deep learning techniques to predict AQI from given image data or environmental features. The main goal is to develop an effective solution for assessing air quality, which is crucial for public health and environmental monitoring.

The model is trained using historical air quality data, coupled with relevant visual or sensor data, to accurately predict the AQI levels. The CNN architecture has been optimized for regression tasks, allowing for continuous value prediction, which is suitable for determining AQI levels in real time.

## Key Features
- **Deep Learning Model**: Utilizes a CNN architecture optimized for regression to predict AQI.
- **Data-Driven Approach**: Trained on real environmental datasets for reliable predictions.
- **Real-Time Capability**: Designed to potentially integrate with IoT systems for real-time air quality monitoring.
- **Comprehensive Evaluation**: Includes model evaluation metrics and visualization tools for performance analysis.

### Dataset Preparation
- **Prepare the dataset** by placing it in the specified folder (`data/`). The dataset should contain relevant features like particulate matter (PM), temperature, humidity, etc.
- **Update the configuration file** (`config.json`) with dataset paths and preprocessing parameters if needed.

### Model Training
1. **Train the model** using the following command:
   ```sh
   python train.py
   ```
   - The training script will use the dataset to train the CNN model, and the training logs will be saved for visualization.

2. **Monitor the training progress** with TensorBoard:
   ```sh
   tensorboard --logdir logs/
   ```

### Model Evaluation
- **Evaluate the model's performance** on the test dataset:
  ```sh
  python evaluate.py
  ```
  - This will output metrics like **Mean Squared Error (MSE)**, **Mean Absolute Error (MAE)**, and **R-squared (R²)** to gauge the model's accuracy.

### AQI Prediction
- **Use the trained model to predict AQI** for new input data:
  ```sh
  python predict.py --input your_input_data
  ```
  - The `predict.py` script takes input features and outputs the predicted AQI level.

