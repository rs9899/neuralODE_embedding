# Word Embedding using NeuralODE 
> Done as a part of project in course EE763

Paper followed : [neuralODE](https://arxiv.org/abs/1806.07366)

## Summary of the paper

* One of the key insight on the paper was giving a new continuous layer approach instead of Residual Network.
* The comparison what done with Residual networks like ResNet and how each layer just work as a small change to the original input.
* ODE Network changes this step wise approach to continuous domain.

![](https://pbs.twimg.com/media/DgJIjd7VQAAEENZ.jpg)

* This Differential Equation based approach removes the bottle-neck we have in normal Neural Network approach to store the activations of the layer in forward pass.
* In section 5 of the paper, we see the use of ODE in time series. The benifit of this ODE network is that given the initial activation, we can run out network to obtain the output at any timestep.
* We can use this time-series based output in both direction as they showed in the experiments with Bi-directional spiral dataset. This gave me the idea that I continue in the later parts.

## [BERT](https://arxiv.org/pdf/1810.04805.pdf)
> **B**idirectional **E**ncoder **R**epresentations from **T**ransformers : Pre-training of Deep Bidirectional Transformers for Language Understanding

* BERT is a pre-trained langauge model word representation.
* As the name suggests and in one of the training part of BERT is bidirectional Language modelling where they mask a few words and expect the network to predict them.

## The IDEA
* One of the few feature of training time series using ODE Network is that, given the activations at some of the given timesteps, we can expect the output at any other timestep, either forward of backward in time.
* This can be used to train a embedding network like the mask Langage modelling of BERT. We can mask few of the input and infer the activations at those places given rest of the activations. 

## Benifits of this approach
* While training, we can use all the benifits that were proposed by the neuralODE paper like *memory efficiency*, *Adaptive computation* & *Scalability* 
* One of the shortcoming of BERT was is large size and inability to train such network specific to the usecase from scratch and making a model that is efficient with the memory use will be benifit in many ways.

## Experiments
* Basic installation and usage in colab : [here](neuralODE_basic.ipynb)