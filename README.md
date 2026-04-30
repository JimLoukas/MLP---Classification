# MLP Neural Network (Java)

## Overview

This project implements a **Multi-Layer Perceptron (MLP)** in Java for a classification task.
The network is trained using **backpropagation** and **mini-batch gradient descent**.

---

## Features

* MLP implemented from scratch
* Up to 3 hidden layers
* Activation functions: Tanh, Logistic, ReLU
* Mini-batch training
* Evaluation on test dataset

---

## Files

* `Main.java` – runs the program
* `MLP_SDT.java` – neural network implementation
* `Activation.java` – activation functions
* `train.txt`, `test.txt` – datasets

---

## Results

* Best basic model: **32-16-8**, accuracy ≈ **89%**
* Best overall model: **128-96-32**, accuracy ≈ **95.7%**
* Smaller batch sizes improved performance
* Tanh performed best in most cases

---

## Run

```bash
javac Main.java
java Main
```
