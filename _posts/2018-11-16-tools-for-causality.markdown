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

Here is a list of libraries, packages and tools for causal discovery and inference.<!--more--> Please let me know if I've missed out on something!

## Python

### Inference

1. **DoWhy**: DoWhy is based on a unified language for causal inference, combining causal graphical models and potential outcomes frameworks. [[GitHub](https://github.com/Microsoft/dowhy)]
2. **CausalInference**: Causalinference is a software package that implements various statistical and econometric methods used in the field variously known as Causal Inference, Program Evaluation, or Treatment Effect Analysis. [[GitHub](https://github.com/laurencium/causalinference)] [[PyPi](https://pypi.org/project/CausalInference/)]
3. **CausalImpact**: This is the Python version of Google's [Causal Impact model](https://github.com/google/CausalImpact). The main goal of the algorithm is to infer the expected effect a given intervention (or any action) had on some response variable by analyzing differences between expected and observed time series data. [[GitHub](https://github.com/dafiti/causalimpact)]

### Discovery

1. **CausalDiscoveryToolbox**: This is a package for causal discovery, and includes algorithms from the popular R packages such as `bnlean` and `pcalg`. [[GitHub](https://github.com/FenTechSolutions/CausalDiscoveryToolbox)]
2. **CGNN**: This is not exactly a package, but its code to reproduce the results from the [paper](https://arxiv.org/abs/1709.05321) "Learning Functional Causal Models with Generative Neural Networks" [[GitHub](https://github.com/GoudetOlivier/CGNN)]
3. **BETS**: This is a package to use Granger causality to learn causal networks with time series data. Although this package is targeted towards gene expression datasets, the method itself is fairly generic, and should work in cases where the number of samples is much lesser than the number of random variables. [[GitHub](https://github.com/lujonathanh/BETS/)]
4. **TiMINO**: This is not a package, but the code to replicate the results from the [paper](https://papers.nips.cc/paper/5063-causal-inference-on-time-series-using-restricted-structural-equation-models.pdf). This is applicable for learning causal graphs from time series data. [[Website](http://people.tuebingen.mpg.de/jpeters/onlineCodeTimino.zip)]
5. **LiNGAM**: This is a package to learn non-Gaussian linear causal models. It includes functionality for different variations of the LiNGAM algorithm, such as ICA based LiNGAM, Direct LiNGAM, VARMA-LiNGAM and LiNGAM for multiple groups. [[GitHub](https://github.com/cdt15/lingam)]

## R

### Inference

1. **CausalImpact**: This R package implements an approach to estimating the causal effect of a designed intervention on a time series. [[GitHub](https://github.com/google/CausalImpact)]
2. **tmle**: This package implements targeted maximum likelihood estimation of point treatment effects. [[CRAN](https://cran.r-project.org/web/packages/tmle/index.html)]
3. **InvariantCausalPrediction**: This R package implements an approach for estimating confidence intervals for causal effects, using data collected in different experimental or environmental conditions. [[CRAN](https://cran.r-project.org/web/packages/InvariantCausalPrediction/index.html)]
4. **pcalg**: This package provides functions for causal structure learning and causal inference using graphical models. Algorithms implemented are - the IDA algorithm, the Generalized Backdoor Criterion (GBC), the Generalized Adjustment Criterion (GAC) and some related functions. [[CRAN](https://cran.r-project.org/web/packages/pcalg/index.html)]

### Discovery

1. **pcalg**: This package provides functions for causal structure learning and causal inference using graphical models. Algorithms implemented are PC, FCI, RFCI, GIES. [[CRAN](https://cran.r-project.org/web/packages/pcalg/index.html)]
2. **CAM**: This package fits a Causal Additive Model [(CAM)](https://arxiv.org/abs/1310.1533) for estimating the causal structure of the underlying process. [[CRAN](https://cran.r-project.org/web/packages/CAM/index.html)]
5. **VAR-LiNGAM**: This is the R code for Vector Autoregressive Linear Non-Gaussian Acyclic Model. [[Website](https://sites.google.com/site/dorisentner/publications/VARLiNGAM)]
6. **Bayes-LiNGAM**: This is a software package for learning directed acyclic graph structures from non-experimental ('uncontrolled') data. [[Website](https://www.cs.helsinki.fi/group/neuroinf/lingam/bayeslingam/)]

More code for causal discovery and inference is listed [here](http://web.math.ku.dk/~peters/code.html) and [here](http://webdav.tuebingen.mpg.de/causality/).

## Tools

1. **Tetrad**: Tetrad is a program which creates, simulates data from, estimates, tests, predicts with, and searches for causal and statistical models. [[Website](http://www.phil.cmu.edu/tetrad/about.html)]

## Other Useful Links
1. Website for LiNGAM [[Website](https://sites.google.com/site/sshimizu06/lingam)]
1. Website with code from papers on causality [[Website](http://web.math.ku.dk/~peters/code.html)]
1. Elias Barenboim's group is beta-testing a tool for doing causal inference from first principles. You can apply to beta test the tool [here](https://bit.ly/36qUz4y). [[Twitter](https://twitter.com/eliasbareinboim/status/1191609450462883841)]

(Updated 20th April, 2020)
