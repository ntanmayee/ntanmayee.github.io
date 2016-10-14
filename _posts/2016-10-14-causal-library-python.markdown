---
title: "Causal Library in Python: Part 1"
layout: post
date: 2016-06-23 22:10
tag: causal, library
image: /assets/images/jekyll-logo-light-solid.png
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: "Our attempt to create a python library for causal inference."
jemoji: '<img class="emoji" title=":ramen:" alt=":ramen:" src="https://assets.github.com/images/icons/emoji/unicode/1f378.png" height="20" width="20" align="absmiddle">'
author: tanmayee
externalLink: false
---

In the ninth semester, we are required to work on a 12 credit project. My project is on building a python library for causal inference. I'm working on this with Chandan Yeshwanth.

Our first task was to find more about existing libraries. Here is a list of libraries that we found:
1. [pcalg](https://cran.r-project.org/web/packages/pcalg/index.html): This R package supports both structure learning and inference. For structure learning, PC, FCI, RFCI and GIES algorithms are implemented. For causal inference, the IDA algorithm, the Generalized Backdoor Criterion (GBC) and the Generalized Adjustment Criterion (GAC) have been implemented. 

2. [CausalInference](http://causalinferenceinpython.org/): This python library sopports
    * Assessment of overlap in covariate distributions
    * Estimation of propensity score
    * Improvement of covariate balance through trimming
    * Subclassification on propensity score
    * Estimation of treatment effects via matching, blocking, weighting, and least squares

3. [CausalImpact](http://google.github.io/CausalImpact/CausalImpact.html): This R package estimates the causal effect of a designed intervention on a time series.

4. [SuperLearner](https://cran.r-project.org/web/packages/SuperLearner/index.html) and [tmle](https://cran.r-project.org/web/packages/tmle/index.html): These are R packages that implement targeted maximum likelihood estimation (TMLE). 

The main challenge in conducting any survey in the area of causal inference, is that there is a wide variation in the terminology and language used, depending on the author's background. For example, my introduction was through Judea Pearl's book **Causality**, where the it was all about Markov models and DAGs and graphs. However, other books on causal inference talk about the Granger causality test, propensity scores and treatment effects. 

Ultimately, we decided to implement CausalImpact in python. We chose this because, firstly, it seemed do-able in the time that we have. Secondly, since it is basically the R implementation of [this](http://research.google.com/pubs/pub41854.html) paper, we didn't have to spend too much time in finding resources to understand the theory. 

Our next steps are to understand the paper first, and then begin its implementation.