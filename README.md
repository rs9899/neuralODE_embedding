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
