---
layout: default
title: PyTorch
parent: Deployment
---


## PyTorch on embedded hardware

We wish to run our RL algorithms on devicem which means that we need to get our RL framework working on our hardware. We wish to deploy to an arm CPU.

Additionaly we want to use our model from within Java ideally as the NMF App framework is designed for Java.


We will use the PyTorch Java bindings, and we need to cross compile for the correct architechure.

[Bindings](https://github.com/pytorch/java-demo)