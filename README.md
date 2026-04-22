# Deep Learning Bonus Project: CNN Classification and Neural Network Optimization

## Overview
This project explores two deep learning applications using Python and neural networks:

1. **Image Classification using Convolutional Neural Networks (CNNs)** on the MNIST handwritten digit dataset.
2. **Sentiment Classification using Feedforward Neural Networks** on the IMDB movie reviews dataset.

The project investigates model architecture design, parameter tuning, and regularization techniques such as dropout to evaluate their impact on performance.

---

## Project Objectives
- Build and train a CNN for handwritten digit recognition.
- Analyze model performance, parameter counts, and validation accuracy.
- Study how hidden layer size affects neural network performance.
- Evaluate whether dropout improves sentiment classification accuracy.
- Compare test accuracy and loss across multiple model configurations.

---

## Dataset
### MNIST Dataset
- 70,000 grayscale images of handwritten digits (0–9)
- Image size: 28 x 28 pixels
- Used for multiclass classification

### IMDB Dataset
- Movie review sentiment dataset
- Binary classification:
  - Positive Review
  - Negative Review

---

## Methods

## Part 1: CNN for MNIST Classification

### Model Architecture
The convolutional neural network consists of:

- Conv2D: 32 filters (3x3), ReLU  
- MaxPooling: 2x2  
- Conv2D: 64 filters (3x3), ReLU  
- MaxPooling: 2x2  
- Conv2D: 64 filters (3x3), ReLU  
- Flatten Layer  
- Dense Layer (64 units, ReLU)  
- Output Layer (10 units, Softmax)

### Model Summary
- Total Parameters: 93,322
- Optimizer: RMSprop (Learning Rate = 0.01)
- Loss Function: Categorical Crossentropy
- Epochs: 5
- Batch Size: 64

### Result
- Test Accuracy: **97.64%**

---

## Part 2: IMDB Sentiment Classification

A two-hidden-layer feedforward neural network was used to study:

- Hidden Units:
  - 16
  - 32
  - 64

- Dropout Rates:
  - 0.0
  - 0.3

### Training Setup
- Optimizer: RMSprop
- Learning Rate: 0.01
- Batch Size: 512
- Epochs: 30

## Results

| Hidden Units | Dropout | Test Accuracy | Test Loss |
|------------|---------|---------------|-----------|
| 16 | 0.0 | 0.8593 | 1.7610 |
| 32 | 0.0 | 0.8531 | 0.5276 |
| 64 | 0.0 | 0.8558 | 1.7286 |
| 16 | 0.3 | 0.8660 | 1.0663 |
| 32 | 0.3 | 0.8694 | 1.0839 |
| 64 | 0.3 | 0.8677 | 0.9234 |

### Findings
- Increasing hidden units alone did not consistently improve accuracy.
- 32 hidden units with 30% dropout produced the highest accuracy.
- 32 hidden units without dropout produced the lowest test loss.
- Dropout improved generalization performance.

---

## Technologies Used
- Python
- TensorFlow / Keras
- PyTorch
- PyTorch Lightning
- ISLP
- NumPy
- Jupyter Notebook

---

## Repository Structure
```bash
├── Bonus_Project.ipynb          # Main notebook
├── Bonus-project_report.pdf     # Project Report
├── Deep_Learning_presentation   # Project Presentation                
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name
```

Install dependencies:

```bash
pip install tensorflow torch torchvision pytorch-lightning ISLP numpy
```

Run the notebook:

```bash
jupyter notebook Bonus-Project.ipynb
```

---

## Future Improvements
- Explore additional hyperparameter tuning, including learning rates and batch sizes.
- Compare the current CNN with deeper architectures or alternative optimizers.
- Test additional regularization methods beyond dropout.
- Extend the IMDB analysis using alternative models such as LSTM or Transformer-based approaches.
- Investigate performance on additional datasets for broader model comparison.

---

## Author
Priyasri Sankaran

Master’s in Data Science and Statistics  
The University of Texas at Dallas
