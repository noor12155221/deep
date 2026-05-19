# Deep Learning CNN Project - MNIST Classification

This project is a Deep Learning image classification task using Convolutional Neural Networks (CNNs) with PyTorch.

The project compares the performance of two different CNN architectures on the MNIST handwritten digits dataset:

- Simple CNN
- Enhanced CNN

---

## Project Overview

The goal of this project is to classify handwritten digits (0–9) from the MNIST dataset and compare a basic CNN model with an improved CNN architecture.

Dataset used:
- MNIST Dataset
- 60,000 training images
- 10,000 testing images
- Image size: 28x28 grayscale

---

## Technologies Used

- Python
- PyTorch
- Torchvision
- Matplotlib

Libraries:

```python
torch
torchvision
matplotlib
```

---

## Project Structure

```bash
DeepLearning-CNN-Project/
│
├── data/                  # MNIST dataset
├── results/               # Saved training curves
│   └── cnn_curves.png
├── main.py                # Main training code
└── README.md
```

---

## Data Preprocessing

Applied preprocessing steps:

1. Convert images to tensors
2. Normalize images using MNIST mean and standard deviation

```python
transforms.ToTensor()
transforms.Normalize((0.1307,), (0.3081,))
```

---

## Models

### 1. Simple CNN

Architecture:

- Conv2D (1 → 16)
- ReLU
- MaxPooling
- Conv2D (16 → 32)
- ReLU
- MaxPooling
- Fully Connected Layer
- Output Layer (10 classes)

---

### 2. Enhanced CNN

Architecture improvements:

- More filters
- Batch Normalization
- Dropout Regularization
- Larger Fully Connected Layer

Layers:

- Conv2D (1 → 32)
- BatchNorm2D
- ReLU
- MaxPooling

- Conv2D (32 → 64)
- BatchNorm2D
- ReLU
- MaxPooling

- Dropout (0.25)

- Fully Connected (256)

- Dropout (0.5)

- Output Layer (10 classes)

---

## Hyperparameters

```python
batch_size = 32
epochs = 5
learning_rate = 0.001
optimizer = Adam
loss_function = CrossEntropyLoss
```

---

## Training Results

### Final Test Accuracy

| Model | Accuracy |
|------|----------|
| Simple CNN | 98.90% |
| Enhanced CNN | 99.13% |

Result:

The Enhanced CNN achieved better accuracy than the Simple CNN because of:
- Batch Normalization
- Dropout
- Increased model capacity

---

## Training Curves

Generated plots include:

- Train Accuracy
- Validation Accuracy
- Train Loss
- Validation Loss

Saved figure:

```bash
results/cnn_curves.png
```

---

## How to Run

Clone repository:

```bash
git clone <your-repo-link>
cd DeepLearning-CNN-Project
```

Install dependencies:

```bash
pip install torch torchvision matplotlib
```

Run project:

```bash
python main.py
```

---

## Output Example

```bash
Simple CNN Accuracy   : 98.90%
Enhanced CNN Accuracy : 99.13%
```

---

## Conclusion

This project demonstrates how architectural improvements in CNNs can improve image classification performance.

Key findings:
- Basic CNN performs very well on MNIST
- Enhanced CNN slightly improves performance
- Regularization and normalization improve generalization

---

## Author

Nour Ahmed
