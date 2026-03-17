# Image Classification on CIFAR-10 using a Multi-Layer Perceptron (MLP)

This project investigates the performance of a fully connected neural network (Multi-Layer Perceptron - MLP) on the CIFAR-10 image classification dataset. The goal is to design, train, and optimize an MLP architecture and evaluate its performance compared to traditional machine learning algorithms.

## Project Overview

The CIFAR-10 dataset consists of 60,000 color images (32×32 pixels) distributed across 10 classes. In this project, a custom MLP model was developed to classify these images.

To improve generalization and reduce overfitting, several architectural and training strategies were explored, including:
* **Architecture:** Fully connected neural network with ReLU activation functions
* **Optimization:** Adam optimizer with Cross-Entropy loss
* **Regularization:** Dropout layers and weight decay
* **Data Augmentation:** Techniques applied to expand the training dataset and improve model robustness

## Results & Evaluation

Extensive experimentation was performed by tuning several hyperparameters such as learning rate, batch size, number of hidden units, and number of training epochs.

**Final Performance**
* **Test Accuracy:** ~56–57%

The optimized MLP model significantly outperformed simpler baseline classifiers such as:
* k-Nearest Neighbors (kNN)
* Nearest Class Centroid

## Error Analysis

As expected for fully connected networks, which do not explicitly preserve spatial structure like Convolutional Neural Networks (CNNs), most misclassifications occurred between visually similar classes. Examples include:
* Ships vs. Trucks
* Cats vs. Dogs

Analysis of the training and testing curves showed a small generalization gap, suggesting that the regularization techniques successfully mitigated overfitting.

## Technologies Used

* **Language:** Python
* **Environment:** Jupyter Notebook
* **Core Libraries:** PyTorch, NumPy, Matplotlib, Scikit-learn
* **Key Concepts:** Deep Learning, Feedforward Neural Networks, Backpropagation, Hyperparameter Tuning, Image Classification

## How to View the Project

Open the `.ipynb` notebook directly on GitHub or download it and run it locally to explore:
* The model implementation
* The training pipeline
* Hyperparameter experiments
* Visualization of training and testing performance

## Notes

This project focuses on understanding how fully connected neural networks perform on image classification tasks and highlights the limitations of MLP architectures when compared to convolutional approaches.
