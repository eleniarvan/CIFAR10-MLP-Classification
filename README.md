# Image Classification on CIFAR-10 using Multi-Layer Perceptron (MLP)

This project explores the performance of a fully connected neural network (Multi-Layer Perceptron) on the **CIFAR-10** image classification dataset. The goal is to design, train, and optimize an MLP architecture and compare its performance against traditional Machine Learning algorithms.

## Project Overview

The CIFAR-10 dataset consists of 60,000 color images (32x32 pixels) across 10 classes. In this project, a custom MLP was developed to classify these images. 

To prevent overfitting and achieve good generalization, various techniques and hyperparameters were evaluated, including:
- **Architecture:** Fully connected layers with ReLU activations.
- **Optimization:** Adam Optimizer with Cross-Entropy Loss.
- **Regularization:** Dropout and Weight Decay.
- **Data Augmentation:** Applied to artificially expand the training dataset and improve model robustness.

## Results & Evaluation

Extensive experiments were conducted by tuning learning rates, batch sizes, and the number of epochs. 

* **Accuracy:** The best-performing MLP model achieved an accuracy of **~56-57%** on the test set.
* **Comparative Analysis:** The MLP model significantly outperformed simpler baseline methods such as **k-Nearest Neighbors (kNN)** and **Nearest Class Centroid**.
* **Error Analysis:** As expected for MLPs (which do not preserve spatial structure like CNNs), misclassifications mostly occurred between visually similar classes (e.g., ships vs. trucks, cats vs. dogs). The learning curves (train vs. test accuracy) demonstrated a small generalization gap, indicating successful mitigation of overfitting.

## Technologies Used

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Core Libraries:** PyTorch / TensorFlow, NumPy, Matplotlib, Scikit-learn
- **Concepts:** Deep Learning, Neural Networks, Hyperparameter Tuning, Image Classification

## How to View

Open the `.ipynb` notebook directly in GitHub (or download it to run locally) to view the code, the experimental setup, and the plotted learning curves.
