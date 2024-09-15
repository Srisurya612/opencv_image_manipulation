
# Fashion MNIST Classification with ANN: Ablation Study

This repository contains code and results for classifying images from the Fashion MNIST dataset using an Artificial Neural Network (ANN). An ablation study is performed to analyze how the model's accuracy changes when varying:

The number of hidden layers in the network.
The number of neurons per layer.




## Table of Contents

1. Introduction
2. Dataset Description
3. Model Architecture
4. Experiments

   4a. Varying the Number of Hidden Layers

   4b. Varying the Number of Neurons per Layer

5. Results

   5a. Effect of Hidden Layers on Accuracy

   5b. Effect of Neurons per Layer on Accuracy

6. Conclusion
7. Requirements
8. Usage
9. References
## Introduction

The goal of this project is to build an ANN to classify images from the Fashion MNIST dataset and to perform an ablation study to understand how the model's architecture affects its performance. By systematically varying the number of hidden layers and neurons per layer, we aim to identify trends and draw conclusions about model complexity and accuracy.
## Dataset Description

The Fashion MNIST dataset is a collection of 70,000 grayscale images of fashion products from 10 categories, with 7,000 images per category. The images are of size 28x28 pixels.

Training Set: 60,000 images

Test Set: 10,000 images

  Classes: 

    0. T-shirt/top
    1. Trouser
    2. Pullover
    3. Dress
    4. Coat
    5. Sandal
    6. Shirt
    7. Sneaker
    8. Bag
    9. Ankle boot
## Model Architecture

An Artificial Neural Network (ANN) is implemented using TensorFlow and Keras. The initial model architecture is as follows:

Input Layer: Flattened input of size 784 (28x28 pixels).

Hidden Layers: 4 hidden layers with 128 neurons each and ReLU activation.

Output Layer: 10 neurons with Sigmoid activation for classification into 10 categories.

## Experiments

## Varying the Number of Hidden Layers
In this experiment, we varied the number of hidden layers while keeping the number of neurons per layer constant at 128.

 Hidden Layers Tested: [1, 2, 3, 4, 5, 6]

 Neurons per Layer: 128

 Epochs: 5

 Batch Size: 128



## Varying the Number of Neurons per Layer
In this experiment, we varied the number of neurons per layer while keeping the number of hidden layers constant at 4.

 Neurons per Layer Tested: [32, 64, 128, 256, 512]

 Hidden Layers: 4
 
 Epochs: 5
 
 Batch Size: 128

## Results

### Effect of Hidden Layers on Accuracy

![Effect of Hidden Layers on Accuracy](reports/figures/layers_accuracy.png)

*Figure 1: Test accuracy vs. Number of hidden layers*

| Number of Hidden Layers | Test Accuracy |
|-------------------------|---------------|
| 1                       | 0.8439        |
| 2                       | 0.8390        |
| 3                       | 0.8521        |
| 4                       | 0.8352        |
| 5                       | 0.8356        |
| 6                       | 0.8457        |

#### Observations

- **Increasing hidden layers** from 1 to 3 resulted in a gradual improvement in test accuracy.
- The **highest accuracy** was achieved with **3 hidden layers**.
- Adding a **4th hidden layer** did not significantly improve accuracy, indicating a point of diminishing returns.

### Effect of Neurons per Layer on Accuracy

![Effect of Neurons per Layer on Accuracy](reports/figures/neurons_accuracy.png)

*Figure 2: Test accuracy vs. Number of neurons per layer*

| Neurons per Layer | Test Accuracy |
|-------------------|---------------|
| 32                | 0.8288        |
| 64                | 0.8428        |
| 128               | 0.8349        |
| 256               | 0.8562        |
| 512               | 0.8181        |

#### Observations

- Increasing the **number of neurons per layer** from 32 to 256 led to improved test accuracy.
- The **best accuracy** was observed with **256 neurons per layer**.
- Increasing to **512 neurons** did not yield significant improvements, suggesting over-parameterization without substantial gains.

### Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Install dependencies

```bash
  pip3 install -r requirements.txt
```

Go to the project directory

```bash
  cd notebooks
```

Run the cells in fashion_mnsit.ipynb notebook



