# Digit Identification from Scratch (MNIST Dataset)

## Goals
In this project, I built a shallow neural network from scratch to identify handwritten digits from the MNIST dataset.  
I used libraries such as **NumPy**, **Pandas**, and **Matplotlib**, without relying on deep learning frameworks like PyTorch.

The architecture of the network:
- **Input Layer**: 784 neurons, corresponding to each pixel of the 28x28 input images.
- **Hidden Layer**: 16 neurons with **ReLU** activation.
- **Output Layer**: 10 neurons, representing the 10 digit classes (0–9).

I implemented:
- **Softmax activation** in the output layer to produce probability distributions.
- **Cross-Entropy Loss** as the loss function for multiclass classification.

Additionally, I developed various optimization algorithms from scratch:
- **Gradient Descent**
- **Stochastic Gradient Descent with Momentum**
- **AdaGrad**
- **RMSprop**
- **Adam**

All optimizers were tested using 10 epochs and a batch size of 64.

---

## Learning
The most important learning outcomes from this project were:
- A deep understanding of **forward propagation** and **backward propagation**.
- The significance of **proper weight initialization** for successful training.
- How different **optimization algorithms** affect convergence speed and model accuracy.
- Correct application of the **chain rule** in matrix-based backpropagation.

Building this from scratch gave me hands-on experience with the internals of neural networks and optimization.

---

## Struggles
Two major challenges I faced were:

1. **Backward Propagation**:  
   Applying the chain rule correctly during matrix multiplications for backpropagation was tricky. It took multiple attempts and some manual derivations to implement it properly.

2. **Weight Initialization**:  
   Initially, I initialized weights randomly using a standard normal distribution, but this led to diminishing gradients and poor training.  
   After research, I realized the need for **He Initialization** to maintain the variance of activations across layers, which solved the problem.

---

## Result / Summary
- **Adam** and **RMSprop** performed the best among the optimization algorithms, achieving:
  - **Adam**: 93% accuracy
  - **RMSprop**: 93.71% accuracy
- Tested on the MNIST test dataset.
- Training used **10 epochs** and a **batch size of 64** for all optimizers.

Overall, coding this project from scratch has given me a solid understanding of:
- Forward and backward propagation
- Weight initialization strategies
- Loss functions
- Optimization algorithms
