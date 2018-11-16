---
title: "Tools and Libraries for Causality"
layout: post
date: 2018-11-16 12:35
headerImage: false
tag:
- causality
- ai
- machine Learning
- Tools
- Libraries
- python
- R
blog: true
author: tanmayee
description: List of tools and libraries available for causal discovery and inference.
---

Here is a list of libraries, packages and tools for causal discovery and inference. Please let me know if I've missed out on something!

## Python

### Inference

1. **DoWhy**: DoWhy is based on a unified language for causal inference, combining causal graphical models and potential outcomes frameworks. [[GitHub](https://github.com/Microsoft/dowhy)]
2. **CausalInference**: Causalinference is a software package that implements various statistical and econometric methods used in the field variously known as Causal Inference, Program Evaluation, or Treatment Effect Analysis. [[GitHub](https://github.com/laurencium/causalinference)] [[PyPi](https://pypi.org/project/CausalInference/)]
3. **CausalImpact**: This is the Python version of Google's [Causal Impact model](https://github.com/google/CausalImpact). The main goal of the algorithm is to infer the expected effect a given intervention (or any action) had on some response variable by analyzing differences between expected and observed time series data. [[GitHub](https://github.com/dafiti/causalimpact)]

### Discovery

1. **CGNN**: This is not exactly a package, but its code to reproduce the results from the [paper](https://arxiv.org/abs/1709.05321) "Learning Functional Causal Models with Generative Neural Networks" [[GitHub](https://github.com/GoudetOlivier/CGNN)]

## R

### Inference

1. **CausalImpact**: This R package implements an approach to estimating the causal effect of a designed intervention on a time series. [[GitHub](https://github.com/google/CausalImpact)]
2. **tmle**: This package implements targeted maximum likelihood estimation of point treatment effects. [[CRAN](https://cran.r-project.org/web/packages/tmle/index.html)]
3. **InvariantCausalPrediction**: This R package implements an approach for estimating confidence intervals for causal effects, using data collected in different experimental or environmental conditions. [[CRAN](https://cran.r-project.org/web/packages/InvariantCausalPrediction/index.html)]
4. **pcalg**: This package provides functions for causal structure learning and causal inference using graphical models. Algorithms implemented are - the IDA algorithm, the Generalized Backdoor Criterion (GBC), the Generalized Adjustment Criterion (GAC) and some related functions. [[CRAN](https://cran.r-project.org/web/packages/pcalg/index.html)]

### Discovery

1. **pcalg**: This package provides functions for causal structure learning and causal inference using graphical models. Algorithms implemented are PC, FCI, RFCI, GIES. [[CRAN](https://cran.r-project.org/web/packages/pcalg/index.html)]
2. **CAM**: This package fits a Causal Additive Model [(CAM)](https://arxiv.org/abs/1310.1533) for estimating the causal structure of the underlying process. [[CRAN](https://cran.r-project.org/web/packages/CAM/index.html)]

More code for causal discovery and inference is listed [here](http://web.math.ku.dk/~peters/code.html) and [here](http://webdav.tuebingen.mpg.de/causality/).

## Tools

1. **Tetrad**: Tetrad is a program which creates, simulates data from, estimates, tests, predicts with, and searches for causal and statistical models. [[Website](http://www.phil.cmu.edu/tetrad/about.html)]

(Updated 16th November, 2018)
