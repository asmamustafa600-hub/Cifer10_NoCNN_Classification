# CIFAR-10 Image Classification (No CNN, with Early Stopping)

A deep learning project that classifies CIFAR-10 images into 10 categories using a plain Dense (fully-connected) Neural Network — **no Convolutional layers used** — with a custom Early Stopping rule.

## Project Overview

- **Dataset:** CIFAR-10 (60,000 32x32 color images across 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
- **Model:** Dense Neural Network (Flatten + Dense layers only, no CNN)
- **Special Feature:** Custom Early Stopping callback — training automatically stops once training accuracy reaches 90%
- **Task:** Multi-class image classification (10 classes)

## How It Works

1. Load the CIFAR-10 dataset directly from `tf.keras.datasets`.
2. Normalize pixel values from the 0-255 range down to 0-1, which helps the network train faster and more reliably.
3. Build a simple network: a `Flatten` layer (turns each image into a single long list of numbers) followed by two `Dense` (fully-connected) layers, and a final output layer with 10 neurons (one per class).
4. Train using a custom callback that stops training early once training accuracy hits 90%, so the model doesn't keep training unnecessarily.
5. Evaluate the final model on the unseen test set.

## Tech Stack

- Python
- NumPy, Matplotlib
- TensorFlow / Keras (model building, training, custom callbacks)

## Files

- `cifar10_no_cnn_early_stopping.ipynb` — full notebook (data loading, model building, custom early stopping, training, evaluation)

## Notes

This project intentionally avoids Convolutional Neural Network (CNN) layers, to explore how a plain Dense network performs on image data compared to CNN-based approaches.

## Author

Asma — NAVTTC Data Science & Machine Learning Program
