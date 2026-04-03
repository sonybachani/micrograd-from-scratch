# 🧠 Building Micrograd from Scratch

### Autograd Engine + Backpropagation Explained Step-by-Step

---

## 📌 Overview

This project implements a **mini deep learning framework from scratch**, inspired by how PyTorch works internally.

Instead of relying on high-level libraries, this notebook builds everything from first principles:

* Automatic differentiation (autograd)
* Backpropagation using the chain rule
* A fully connected neural network (MLP)
* Training using gradient descent

---

## 🎯 Why This Project

Modern frameworks abstract away the complexity of training neural networks.

This project focuses on understanding what happens under the hood:

* How computational graphs are built
* How gradients flow backward
* How parameters are updated during training

👉 The goal is to move from *using models* to *understanding them deeply*.

---

## ⚙️ Features

* Custom **Value class** for scalar autograd
* Reverse-mode automatic differentiation
* Support for operations: `+`, `*`, `-`, `/`, `tanh`, `exp`, `pow`
* Backpropagation via topological sorting
* Fully connected neural network (MLP)
* Training loop with gradient descent
* PyTorch comparison for verification

---

## 🏗️ Architecture

The system is built step-by-step:

1. **Value** → stores data, gradient, and graph connections
2. **Neuron** → weighted sum + activation
3. **Layer** → group of neurons
4. **MLP** → stack of layers
5. **Training loop** → forward → backward → update

---

## 📊 Example

The model is trained on a small dataset:

```python
xs = [
    [2.0,  3.0, -1.0],
    [3.0, -1.0,  0.5],
    [0.5,  1.0,  1.0],
    [1.0,  1.0, -1.0],
]

ys = [1.0, -1.0, -1.0, 1.0]
```

The goal is to learn a mapping from inputs → targets using gradient descent.

---

## 📉 Training

Training follows:

1. Forward pass
2. Compute loss (MSE)
3. Backward pass (autograd)
4. Update parameters

---

## 🔬 Key Concepts Covered

* Computational graphs
* Chain rule
* Reverse-mode autodiff
* Gradient descent
* Neural network fundamentals

---

## 🔗 Notebook

👉 Kaggle version:
https://www.kaggle.com/code/sonybachani/building-micrograd-from-scratch

---

## 🛠 Tech Stack

* Python
* NumPy
* Matplotlib
* Graphviz
* PyTorch (for verification only)

---

## 🚀 How to Run

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/micrograd-from-scratch.git
cd micrograd-from-scratch
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

## 📈 Future Improvements

* Add ReLU activation
* Train on real datasets (MNIST)
* Add optimizers (Adam, SGD variants)
* Vectorized version (beyond scalars)

---

## 🌟 Inspiration

Inspired by Andrej Karpathy’s micrograd project.

---

## 🤝 Connect

If you found this useful, feel free to connect or give a ⭐ to the repo!
