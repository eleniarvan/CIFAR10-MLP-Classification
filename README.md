# Image Classification on CIFAR-10 using a Multi-Layer Perceptron (MLP)

Design, training, and evaluation of a fully connected neural network on the 
CIFAR-10 image classification dataset, with hyperparameter tuning and 
comparison against classical baseline classifiers.

## Project Overview

The CIFAR-10 dataset consists of 60,000 color images (32×32 pixels) across 
10 classes. A custom MLP was built from scratch to classify these images, 
with a focus on regularization and generalization.

## Architecture
```
Input (3072) → Linear(3072→512) → ReLU → Dropout(0.5)
             → Linear(512→256)  → ReLU → Dropout(0.5)
             → Linear(256→10)
```

- **Loss:** Cross-Entropy
- **Optimizer:** Adam (lr=1e-4, weight_decay=1e-4)
- **Epochs:** 40 | **Batch size:** 32

## Data Augmentation

To improve generalization, the following augmentations were applied to 
the training set:
- RandomHorizontalFlip
- RandomCrop(32, padding=4)

## Results

| Model                  | Test Accuracy |
|------------------------|---------------|
| MLP (this project)     | ~56–57%       |
| k-Nearest Neighbors    |  38.5%        |
| Nearest Class Centroid |  27.7%        |

The MLP significantly outperformed both classical baselines.

## Error Analysis

Most misclassifications occurred between visually similar classes 
(e.g. cats vs dogs, ships vs trucks) — expected behavior for a fully 
connected network that does not explicitly model spatial structure 
unlike CNNs. Training vs test accuracy curves confirmed a small 
generalization gap, indicating that Dropout and Weight Decay 
successfully controlled overfitting.

## Technologies

- Python, PyTorch, NumPy, Matplotlib, Scikit-learn
- Jupyter Notebook
- Dataset: [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)

## How to Run
```bash
git clone https://github.com/eleniarvan/CIFAR10-MLP-Classification.git
cd CIFAR10-MLP-Classification
jupyter notebook MLP.ipynb
```

Dependencies: `torch`, `torchvision`, `numpy`, `matplotlib`, `scikit-learn`

## Context

Developed as part of the Neural Networks course at the Aristotle University 
of Thessaloniki (AUTH), November 2025.
