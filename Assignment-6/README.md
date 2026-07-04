# Assignment 6 - Autoencoder for Image Denoising using MNIST

## Overview

This assignment demonstrates the implementation of a Deep Learning Autoencoder to remove Gaussian noise from handwritten digit images using the MNIST dataset. The model learns a compressed representation of the input images and reconstructs clean images from noisy inputs.

## Objectives

- Load and preprocess the MNIST dataset.
- Normalize and flatten the images.
- Add Gaussian noise to the images.
- Build an Autoencoder using TensorFlow/Keras.
- Train the model on noisy images.
- Reconstruct denoised images.
- Compare original, noisy, and reconstructed images.

## Dataset

- Dataset: MNIST Handwritten Digits
- Training Images: 60,000
- Testing Images: 10,000
- Image Size: 28 × 28 pixels

## Model Architecture

### Encoder
- Dense (128, ReLU)
- Dense (64, ReLU)
- Dense (32, ReLU)

### Decoder
- Dense (64, ReLU)
- Dense (128, ReLU)
- Dense (784, Sigmoid)

## Training Configuration

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Epochs: 20
- Batch Size: 256

## Workflow

1. Import Libraries
2. Load the MNIST Dataset
3. Normalize the Images
4. Flatten the Images
5. Add Gaussian Noise
6. Visualize Original and Noisy Images
7. Build the Autoencoder Model
8. Compile the Model
9. Train the Model
10. Plot Training and Validation Loss
11. Reconstruct (Denoise) Images
12. Compare Original, Noisy, and Denoised Images

## Results

The autoencoder successfully reduced Gaussian noise from handwritten digit images while preserving their important features. The training and validation losses decreased consistently, indicating effective learning and good generalization.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

## Author

**Shravya Banoth**
