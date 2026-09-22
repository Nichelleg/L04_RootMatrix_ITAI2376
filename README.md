# Lab 04: CNN for MNIST Handwritten Digit Classification
### Deep Learning in AI - ITAI 2376 
### Team Root Matrix: Cesar Noriega, Mary Ann Mastri, Luiz Paludo, Nichelle Graf
---
This project explores the fundamentals of Convolutional Neural Networks (CNNs) using the MNIST handwritten digit dataset. The lab walks through the full deep learning workflow, including data preprocessing, CNN model construction, model compilation, training, experimentation, evaluation, and reflection.

## Project Objectives

The goals of this lab were to:

- Understand the basic architecture of a CNN
- Work with the MNIST handwritten digit dataset
- Preprocess image data for deep learning
- Build and train a CNN using TensorFlow/Keras
- Explore the role of convolution, pooling, dropout, and dense layers
- Experiment with model architecture and training parameters
- Evaluate model performance on unseen test data
- Reflect on the learning process and results

## Dataset

The project uses the **MNIST dataset**, which contains grayscale images of handwritten digits from 0 through 9.

Each image is:

- 28 × 28 pixels
- Grayscale
- Assigned to one of 10 digit classes

The dataset is loaded directly through TensorFlow/Keras.

## Data Preprocessing

The preprocessing steps included:

- Loading the MNIST training and test sets
- Normalizing pixel values from 0–255 to 0–1
- Reshaping images to include a grayscale channel dimension
- One-hot encoding the digit labels for multi-class classification

## CNN Architecture

The CNN used in the completed notebook includes:

1. Input layer: 28 × 28 × 1
2. Conv2D layer with 32 filters and a 3 × 3 kernel
3. MaxPooling2D layer with a 2 × 2 pool
4. Conv2D layer with 128 filters and a 3 × 3 kernel
5. MaxPooling2D layer with a 2 × 2 pool
6. Flatten layer
7. Dropout layer with a rate of 0.5
8. Dense output layer with 10 units and Softmax activation

The second convolutional layer was changed from 64 filters to 128 filters as an architecture modification.

## Model Compilation

The model was compiled using:

- **Loss Function:** Categorical Cross-Entropy
- **Optimizer:** Adam
- **Evaluation Metric:** Accuracy

Categorical cross-entropy was selected because the task involves 10 one-hot encoded output classes. Adam was used because it efficiently updates model weights while adapting the learning rate during training.

## Training Experiment

The initial training configuration used:

- Batch size: 128
- Epochs: 15
- Validation split: 10%

A second training experiment was conducted using:

- Batch size: 64
- Epochs: 10
- Validation split: 10%

The CNN architecture remained unchanged during the training-parameter experiment so that the effects of batch size and number of epochs could be compared more directly.

## Results

### Initial Training Run

- Final training accuracy: 99.25%
- Final validation accuracy: 99.12%
- Highest validation accuracy: approximately 99.22%

### Training Parameter Experiment

- Final training accuracy: approximately 99.10%
- Final validation accuracy: approximately 99.13%
- Highest validation accuracy: approximately 99.30%

### Test Evaluation

The experimental model achieved:

- **Test Accuracy:** 99.19%
- **Test Loss:** 0.0253

The test accuracy was close to both the training and validation accuracy, suggesting that the model generalized well to unseen data without significant overfitting.

## Key Observations

- Conv2D layers learn visual features such as edges, curves, and shapes.
- Increasing the number of filters allows the network to learn a larger variety of features but increases computational requirements.
- MaxPooling reduces the size of feature maps while preserving important information.
- Dropout helps reduce overfitting.
- Reducing the training from 15 epochs to 10 epochs did not significantly reduce validation performance.
- A smaller batch size resulted in more frequent weight updates.
- More epochs did not automatically produce better validation performance.

## Repository Contents

This repository contains the materials associated with the group lab, including:

- Completed CNN notebooks
- PDF version of notebooks 
- Team Reflective Journal
- Team Contributions Journal

## Team Contributions

Each team member contributed to the project through individual technical work, research and notebook reflections. 

Individual contributions are documented separately in the team contribution journal.

## Tools and Technologies

- Python
- Google Colab
- TensorFlow
- Keras
- MNIST Dataset
- GitHub

## Conclusion

This lab provided hands-on experience with building and evaluating a Convolutional Neural Network. In addition to achieving high classification accuracy, the project demonstrated how changes to network architecture and training parameters can affect model behavior, efficiency, and generalization.
