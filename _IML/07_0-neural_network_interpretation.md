---
title:  "Chapter 7. Neural Network Interpretation"
permalink: /IML/neural_network_interpretation/
---


# Neural Network Interpretation {#neural-networks}

`r if(is.html){only.in.html}`

<!-- General Intro -->
The following chapters focus on interpretation methods for neural networks.
The methods visualize features and concepts learned by a neural network, explain individual predictions and simplify neural networks.

Deep learning has been very successful, especially in tasks that involve images and texts such as image classification and language translation. 
The success story of deep neural networks began in 2012, when the ImageNet image classification challenge [^imagenet] was won by a deep learning approach.
Since then, we have witnessed a Cambrian explosion of deep neural network architectures, with a trend towards deeper networks with more and more weight parameters.

<!-- Why not interpretable -->
To make predictions with a neural network, the data input is passed through many layers of multiplication with the learned weights and through non-linear transformations.
A single prediction can involve millions of mathematical operations depending on the architecture of the neural network.
There is no chance that we humans can follow the exact mapping from data input to prediction.
We would have to consider millions of weights that interact in a complex way to understand a prediction by a neural network.
To interpret the behavior and predictions of neural networks, we need specific interpretation methods.
The chapters assume that you are  familiar with deep learning, including convolutional neural networks.

<!-- Why specific interpretation -->
We can certainly use [model-agnostic methods](#agnostic), such as [local models](#lime) or [partial dependence plots](#pdp), but there are two reasons why it makes sense to consider interpretation methods developed specifically for neural networks:
First, neural networks learn features and concepts in their hidden layers and we need special tools to uncover them.
Second, the gradient can be utilized to implement interpretation methods that are more computationally efficient than model-agnostic methods that look at the model "from the outside".
Also most other methods in this book are intended for the interpretation of models for tabular data.
Image and text data require different methods.

The next chapters cover the following topics:

- [Feature Visualization](#feature-visualization): What features has the neural network learned?
  [Adversarial Examples](#adversarial) from the [Example-Based Explanations chapter](#example-based) are closely related to feature visualization : How can we manipulate the inputs to get a wrong classification?
- [Concepts](#neural-concepts) (IN PROGRESS): Which more abstract concepts has the neural network learned?
- [Feature Attribution](#feature-attribution) (IN PROGRESS): How did each input contribute to a particular prediction?
- [Modell Distillation](#neural-distillation) (IN PROGRESS): How can we explain a neural network with a simpler model?
