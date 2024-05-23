# Crop-Health-Classification-CNN

## Table of Contents

1\. [Project Overview](#project-overview)

2\. [Introduction](#introduction)

3\. [Dataset](#dataset)

4\. [Features](#features)

5\. [Methodology](#methodology)

6\. [Results](#results)

7\. [Usage](#usage)

8\. [Contributing](#contributing)

9\. [License](#license)

## Project Overview

This project focuses on classifying the health status of crops using Convolutional Neural Networks (CNNs). The goal is to identify whether crops are healthy or affected by diseases such as viruses or bacteria based on images, aiding farmers in effective crop management.

## Introduction

    Monitoring crop health is a critical aspect of modern agriculture, as it directly impacts yield, profitability, and food security. However, traditional methods of monitoring, such as manual inspection, are often labor-intensive, time-consuming, and prone to human error. This project addresses the challenge by leveraging Convolutional Neural Networks (CNNs), a powerful deep learning technique, to automate the classification of crop health from images.The problem at hand is the need for an efficient and reliable method to monitor crop health. Early detection of diseases, nutrient deficiencies, or pest infestations is vital for timely intervention and effective farm management. By accurately identifying and classifying crop health issues, farmers can take proactive measures to mitigate risks, optimize resource allocation, and maximize yield.
    This project offers a scalable solution to the problem by utilizing CNNs, a type of artificial neural network particularly effective for image classification tasks. CNNs can automatically learn and extract relevant features from images, enabling them to discern subtle differences indicative of crop health conditions. TensorFlow and Keras, popular deep learning libraries, are employed to build and train the CNN model. TensorFlow provides a robust framework for constructing neural networks, while Keras offers a user-friendly interface for prototyping and deploying deep learning models.
    By harnessing the capabilities of CNNs and leveraging TensorFlow and Keras, this project provides a reliable and scalable solution for agricultural monitoring and precision farming. Farmers can utilize the trained model to analyze images of crops captured in the field, swiftly identifying any signs of distress or abnormalities. This proactive approach enables timely intervention, optimizing resource allocation, minimizing crop losses, and ultimately contributing to sustainable and efficient agricultural practices.

## Dataset

The dataset contains images of crops categorized into two classes:

- **Healthy**: Crops with no signs of disease.

- **Diseased**: Crops affected by various diseases.

### Example Images

![image](https://github.com/Sahilwarudkar27/Crop-Health-Classification-CNN/assets/99885674/7bfdec11-6b9b-4d05-8d9e-a32b00d96d4f)

## Features

- **Image Data**: High-quality images labeled as healthy or diseased.

- **CNN Architecture**: Multiple convolutional layers for feature extraction.

- **Data Augmentation**: Techniques like random flipping and rotation to enhance model robustness.

- **Evaluation Metrics**: Accuracy, precision, recall, and F1-score.

## Methodology

1\. **Data Loading and Preprocessing**:

    - Loaded images from the dataset directory.

    - Resized and normalized images.

    - Applied data augmentation.

2\. **Model Architecture**:

    - Convolutional layers for feature extraction.

    - Max pooling layers to reduce dimensionality.

    - Fully connected layers for classification.

    - Softmax activation for output layer.

3\. **Training**:

    - Split the dataset into training, validation, and test sets.

    - Trained the model using the Adam optimizer and sparse categorical cross-entropy loss.

    - Evaluated performance on validation and test sets.

### Model Summary

Model: "sequential_5"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 sequential_3 (Sequential)   (28, 256, 256, 3)         0         
                                                                 
 conv2d_6 (Conv2D)           (28, 254, 254, 32)        896       
                                                                 
 max_pooling2d_6 (MaxPoolin  (28, 127, 127, 32)        0         
 g2D)                                                            
                                                                 
 conv2d_7 (Conv2D)           (28, 125, 125, 64)        18496     
                                                                 
 max_pooling2d_7 (MaxPoolin  (28, 62, 62, 64)          0         
 g2D)                                                            
                                                                 
 conv2d_8 (Conv2D)           (28, 60, 60, 64)          36928     
                                                                 
 max_pooling2d_8 (MaxPoolin  (28, 30, 30, 64)          0         
 g2D)                                                            
                                                                 
 conv2d_9 (Conv2D)           (28, 28, 28, 64)          36928     
                                                                 
 max_pooling2d_9 (MaxPoolin  (28, 14, 14, 64)          0         
 g2D)                                                            
                                                                 
 conv2d_10 (Conv2D)          (28, 12, 12, 64)          36928     
                                                                 
 max_pooling2d_10 (MaxPooli  (28, 6, 6, 64)            0         
 ng2D)                                                           
                                                                 
 conv2d_11 (Conv2D)          (28, 4, 4, 64)            36928     
                                                                 
 max_pooling2d_11 (MaxPooli  (28, 2, 2, 64)            0         
 ng2D)                                                           
                                                                 
 flatten_1 (Flatten)         (28, 256)                 0         
                                                                 
 dense_2 (Dense)             (28, 64)                  16448     
                                                                 
 dense_3 (Dense)             (28, 3)                   195       
                                                                 
=================================================================
Total params: 183747 (717.76 KB)
Trainable params: 183747 (717.76 KB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________

## Results

The model achieved high accuracy and effectively distinguished between healthy and diseased crops. Below are the key performance metrics:

- **Accuracy**: 86.61%

### Training and Validation Accuracy

![image](https://github.com/Sahilwarudkar27/Crop-Health-Classification-CNN/assets/99885674/07b0b94c-9b08-4583-9aaa-4441ed3fb6b8)


### Example Predictions

The following images show the model's predictions on the test dataset, with the actual and predicted labels along with confidence scores.

![image](https://github.com/Sahilwarudkar27/Crop-Health-Classification-CNN/assets/99885674/8ec9be1e-1302-4acd-881f-d32896c013cd)


## Usage

To use this project, follow these steps:
1\. Access the colab notebook:

   - Open the colab by clicking on the following link: Link to colab (https://colab.research.google.com/drive/1MRvDIDazo9HFg2vIwexWULqF3y9AMKEz#scrollTo=RuYXM4Y66_QS)

2\. Run the notebook:

   - Once the notebook is open, you can run each cell sequentially to see the analysis and model implementation.

## Contributing

Contributions are welcome! Please follow these steps:

1\. Fork the repository.

2\. Create a new branch (`git checkout -b feature-branch`).

3\. Commit your changes (`git commit -m 'Add new feature'`).

4\. Push to the branch (`git push origin feature-branch`).

5\. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
