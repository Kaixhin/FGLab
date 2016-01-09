# DNGO Bayesian Optimisation (FGLab)

## Introduction

Bayesian optimisation is a global optimisation technique, which treats the function it must optimise as a random function. It places a prior on the function, and evaluates the function to collect data points. Each evaluation is used to update the posterior distribution over the function, which in turn is used to select the next point to evaluate. This allows Bayesian optimisation to be data-efficient, and hence it is a suitable technique for optimising hyperparameters of another system. Although this is usually performed with Gaussian processes, an alternative technique is to use Deep Networks for Global Optimization (DNGO) [1]. This example will utilise the bot7 library in order to optimise the 6-dimensional Hartmann function.

This example has been adapted from the [DNGO demo](https://github.com/j-wilson/bot7/blob/master/examples/dngo_demo.lua). **TO CHANGE:** `branin_noisy.py` has been set up to take command line arguments and save its results in a JSON file, whilst `fglab.py` acts as an intermediary between Spearmint and the function to optimise by using FGLab's API.

## Requirements

- [Torch7](http://torch.ch/)
- [gpTorch7](https://github.com/j-wilson/gpTorch7)
- [bot7](https://github.com/j-wilson/bot7)

## Instructions

1. Create a new project from [dngo-bayesian-optimisation.json](dngo-bayesian-optimisation.json).
1. Set up [FGMachine](https://github.com/Kaixhin/FGMachine/blob/master/examples/DNGO-Bayesian-Optimisation) and run bot7.

## Citations

[1] Snoek, J., Rippel, O., Swersky, K., Kiros, R., Satish, N., Sundaram, N., Patwary, M., Ali, M. & Adams, R. P. (2015). Scalable Bayesian Optimization Using Deep Neural Networks. *arXiv preprint* arXiv:1502.05700.
