## Overview

This project implements a **Multi-Layer Perceptron (MLP)** neural network in **Java** for solving a classification problem.
The model is trained using **backpropagation** and **mini-batch gradient descent**, and its performance is evaluated on a separate test dataset.

The main goal of this project is to study how different parameters affect the **generalization ability** of the network.

---

## ⚙️ Features

* Fully implemented MLP from scratch (no external ML libraries)
* Support for **multiple hidden layers (up to 3)**
* Training with **mini-batch gradient descent**
* Multiple **activation functions**:

  * Logistic (Sigmoid)
  * Tanh
  * ReLU
* Performance evaluation on test data
* Experimentation with:

  * Network architecture
  * Activation functions
  * Batch sizes

---

## Project Structure

```
├── Main.java                # Entry point of the program
├── MLP_SDT.java            # Core MLP implementation
├── Activation.java         # Activation functions and derivatives
├── train.txt               # Training dataset
├── test.txt                # Test dataset
```

---

## How It Works

### 1. Forward Pass

Computes the output of the network for a given input sample.

### 2. Backpropagation

Gradients are computed using the **chain rule**, starting from the output layer and moving backward.

### 3. Weight Update

Weights and biases are updated using:

* Mini-batch gradient descent
* Learning rate scaling
* Gradient averaging per batch

---

## Training Process

* Training runs for multiple **epochs**
* Minimum epochs: **800**
* Stops when:

  * Convergence is reached OR
  * Maximum epochs limit is exceeded

Each epoch:

* Shuffles the dataset
* Splits data into mini-batches
* Performs forward + backward pass
* Updates weights

---

## Experiments

We tested:

###  Network Architectures

* 8 – 8 – 8
* 16 – 8 – 4
* 32 – 16 – 8

###  Activation Functions (3rd Hidden Layer)

* Tanh
* Logistic
* ReLU

###  Batch Sizes

* N/10
* N/20
* N/100
* N/200

Total experiments: **36 combinations**

---

## Key Results

* Smaller batch sizes significantly improve performance
* Larger networks generally achieve better accuracy
* **Tanh activation** performs best in most cases
* Logistic function performs worst overall

### Best Result (Initial Experiments)

* Architecture: **32 – 16 – 8**
* Activation: **Tanh**
* Batch size: **N/200**
* Accuracy: **89.20%**

---

## Further Optimization

Additional experiments were performed to maximize performance.

### Best Accuracy Achieved

* Architecture: **128 – 96 – 32**
* Accuracy: **95.70%**

### Best Trade-off Model

* Architecture: **32 – 32 – 16**
* Accuracy: **94.95%**
* Faster and more efficient

---

## Error Analysis

* Misclassifications occur mainly near **class boundaries**
* The model performs well on clearly separable data
* Increasing network complexity improves boundary learning

---

## Visualization

The project includes functionality to export classification results:

* `+` → Correct classification
* `-` → Incorrect classification

These can be plotted to analyze error distribution.

---

## How to Run

### Compile

```bash
javac Main.java
```

### Run

```bash
java Main
```

---

## Notes

* A fixed random seed is used for reproducibility
* The export function is optional (commented in code)
* Additional Python script (not included) was used for plotting

---

## Authors

* Georgios Kefalas
* Dimitrios Loukas

---

## Course

Computational Intelligence (ΜΥΕ035)
