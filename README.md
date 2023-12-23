# Cats vs Dogs Image Classification

This repository contains code for a simple image classification model that distinguishes between cats and dogs using a combination of a pre-trained ResNet50 model and a YOLOv5 model. The code is written in Python and utilizes popular deep learning libraries such as TensorFlow and Keras.

## Getting Started

To run this code, follow these steps:

1. Install the required dependencies:

    ```bash
    !pip install yolov5
    ```

2. Set up the Kaggle API for downloading the dataset:

    - Create a Kaggle account if you don't have one.
    - Obtain the Kaggle API key (kaggle.json) from your Kaggle account settings.
    - Upload the API key to Colab:

        ```bash
        !mkdir -p ~/.kaggle
        !cp kaggle.json ~/.kaggle/
        ```

3. Download and extract the dataset:

    ```bash
    !kaggle datasets download -d salader/dogs-vs-cats
    ```

4. Import the necessary libraries and preprocess the dataset.

## Dataset

The dataset used in this project is the ["Dogs vs. Cats" dataset](https://www.kaggle.com/datasets/salader/dogs-vs-cats) available on Kaggle. It contains labeled images of cats and dogs for training and testing the classification model.

## Models Used

- **ResNet50**: A pre-trained convolutional neural network for feature extraction.
- **YOLOv5**: A state-of-the-art object detection model.

## Model Training

The code includes the following steps for model training:

1. Loading and preprocessing the dataset using TensorFlow's ImageDataGenerator.
2. Creating a ResNet50 model with transfer learning.
3. Creating a YOLOv5 model using PyTorch.
4. Combining the features extracted by ResNet50 with a fully connected neural network.
5. Compiling and training the combined model on the dataset for 10 epochs.

## Evaluation and Visualization

The model's performance is visualized using Matplotlib, plotting training and validation accuracy, as well as training and validation loss over epochs.

## Prediction

The code includes an example of making predictions on a test image (`cat.jpg`) using the trained model. The image is loaded, resized, and fed into the model for prediction, with a threshold of 0.5 for classifying as either a cat or a dog.

Feel free to explore ways to improve the model's performance, such as adding more data, applying data augmentation, using regularization techniques, or experimenting with different architectures.

**Note**: Make sure to adjust the paths and filenames according to your dataset and file locations.
