# Autonomous-car-similator

Basically here I tried to simulate a self driving car using udacity self driving simulator

# Requirements

1. Udacity Simulator
```bash
https://github.com/udacity/self-driving-car-sim
```
2. You can create your own dataset or you can download from 
```bash
!git clone https://github.com/rslim087a/track`
```
or
```bash
https://www.kaggle.com/datasets/zaynena/selfdriving-car-simulator`
```
3. Python 3.7 preferred because I tried it in Python 3.10 and I was getting
```bash
TypeError: Could not locate function 'mse'. Make sure custom classes are decorated with `@keras.saving.register_keras_serializable()`. Full object config: {'module': 'keras.metrics', 'class_name': 'function', 'config': 'mse', 'registered_name': 'mse'}
```

# Architecture 
1. NVIDIA model used
```bash
Image normalization to avoid saturation and make gradients work better.
Convolution: 5x5, filter: 24, strides: 2x2, activation: ELU
Convolution: 5x5, filter: 36, strides: 2x2, activation: ELU
Convolution: 5x5, filter: 48, strides: 2x2, activation: ELU
Convolution: 3x3, filter: 64, strides: 1x1, activation: ELU
Convolution: 3x3, filter: 64, strides: 1x1, activation: ELU
Drop out (0.5)
Fully connected: neurons: 100, activation: ELU
Fully connected: neurons: 50, activation: ELU
Fully connected: neurons: 10, activation: ELU
Fully connected: neurons: 1 (output)`
```

# Demo Video



# Paper Link
https://arxiv.org/pdf/1604.07316v1.pdf
