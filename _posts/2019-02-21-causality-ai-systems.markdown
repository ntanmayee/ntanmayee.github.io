---
title: "Using Causality to Understand AI Systems Better"
layout: post
date: 2019-02-21 11:08
headerImage: false
tag:
- causality
- ai
- machine Learning
- systems
- causal inference
- interpretability
blog: true
author: tanmayee
description: Can ideas from causality help us in understanding AI systems?
---
*This article originally appeared on [LinkedIn pulse](https://www.linkedin.com/pulse/using-causality-understand-ai-systems-better-tanmayee-narendra/).* <!--more-->

Co-Authors: [Utkarsh Desai](https://www.linkedin.com/in/utkarsh-desai-b927336/), [Senthil Mani](https://www.linkedin.com/in/kmsenthil/) and [Anush Sankaran](https://www.linkedin.com/in/goodboyanush/)

## Motivating Example
Suppose you had a long day at work, and now you have a terrible headache. Hoping to feel better, you take an aspirin tablet and go to sleep. The next day, you wake up refreshed with no headache to bother you. Now, did the headache go away because of the aspirin? Would you still have the headache if you hadn't taken the aspirin last night? There is no way to go back in time, recreate the same situation, and check whether you would still have a headache if you hadn't taken the aspirin. How might we answer such questions?

Let us consider another example. Those who design complex processes or systems constantly introspect whether any proposed change will lead to certain improvement in performance. A definitive way to test the benefit of the change is to implement the change, and conduct a randomized experiment and observe changes in performance. In most cases, this is expensive and time consuming, and this inherently limits the number of changes that can be tested practically.

## Causality Theory
The theory of causality provides a principled method to codify assumptions, and use existing data to answer hypothetical "what-if" kinds of questions. In causality theory, questions/queries are organized into a three level hierarchy;

* The easiest level involves questions about prediction (How many shoppers buy pencils and pens?)
* The next level involves questions about interventions (How many shoppers would buy a pen if I doubled the price of a pencil?)
* The hardest questions are counterfactuals (How much profit would I have made yesterday on pencils, if I had doubled the price of pens?)

The expressive power of causal models is strictly greater than those of statistical models, as the latter is equipped to answer only prediction type of questions. [1]

Typically, there are two steps to using a causal model.

1. Causal Discovery, the process of discovering causal relationships between variables. This step can also be thought of as a method of codifying assumptions about the system. Causal discovery is a hard problem on many levels - First, from a statistics standpoint, empirically discovering causal relationships between variables is an ill-posed problem. Second, the choice of variables depends on the granularity of analysis required, and is related to the nature of queries that are required to be answered by the causal model.
2. Causal Inference, where queries (predictions, interventions and counterfactuals) are answered using the causal model.
A typical causal inference engine [2] consists of the following –

The following would be required as inputs:

1. Query, which is the question that needs to be answered
2. Assumptions, which are usually codified by a directed graph
3. Data, for empirical estimation

The engine would produce the following outputs:

1. Estimand, which is a recipe or formula to answer the query based on assumptions
2. Estimate, which is the answer to the query. This is computed from the estimand and the data
3. Fit indices, which give a measure of compatibility between the data and the assumptions

There are several statistical techniques to compute the estimand, estimate and fit indices. [3]

Suppose a designer wanted to quantify a system’s change in performance for a particular change. Causal models provide a principled methodology where assumptions can be codified, and performance changes can be estimated with data.

## Applications of Causality
Historically, causal inference has been used in econometrics to estimate effects of policies, and in epidemiology[3], to estimate the effectiveness of drugs and other medical treatments. However, in the past few years, there have been several intriguing applications of causality to other non-traditional domains such as computational advertisement[4], exoplanet search[5], recommendation engines[6], fairness and bias[7], and in image understanding[8]. Mechanisms of causation are present in (arguably) every discipline, and causality as a theory has reached that level of maturity where it can be potentially applied to different domains. There is a lot of value in answering questions about interventions, and about hypothetical what-if questions, without conducting expensive experiments.

## Causality and AI Research
In our research, we are exploring several problems where we think causality will provide an alternate (and hopefully useful) method of investigation. One particular avenue is trying to better understand deep learning models by using techniques from causality. Although deep learning models are being increasingly used in end-user facing applications, it is difficult to understand exactly how they work. Our goal is to study both data and model explainability through the lens of causal theory. This involves

Causal Discovery in Deep Neural Networks: Developing a way to represent a deep neural network as a structural causal model, with the ability to answer interventional and counterfactual questions about input data and components of the network
Causal Signals in Data: Devising methods to discover latent causal signals in data (images, audio and text) and develop a means to abstract out knowledge/rules about the data generation process
Novel Applications of Causality: Exploring applications of causality, leveraging the techniques developed above, to solve challenges in data and model explainability and testing.
We are happy to hear your thoughts and views and are looking for active collaborations to pursue this research.

### References
1. Peters, J., Janzing, D., & Schölkopf, B. (2017). Elements of causal inference: foundations and learning algorithms. MIT press.
2. Pearl, J. (2018). Theoretical impediments to machine learning with seven sparks from the causal revolution. arXiv preprint arXiv:1801.04016.
3. Petersen, M. L., & van der Laan, M. J. (2014). Causal models and learning from data: integrating causal modeling and statistical estimation. Epidemiology (Cambridge, Mass.), 25(3), 418-26.
4. Bottou, L., Peters, J., Quiñonero-Candela, J., Charles, D. X., Chickering, D. M., Portugaly, E., ... & Snelson, E. (2013). Counterfactual reasoning and learning systems: The example of computational advertising. The Journal of Machine Learning Research, 14(1), 3207-3260.
5. Schölkopf, B., Hogg, D., Wang, D., Foreman-Mackey, D., Janzing, D., Simon-Gabriel, C. J., & Peters, J. (2015, June). Removing systematic errors for exoplanet search via latent causes. In International Conference on Machine Learning (pp. 2218-2226).
6. Wang, Y., Liang, D., Charlin, L., & Blei, D. M. (2018). The Deconfounded Recommender: A Causal Inference Approach to Recommendation. arXiv preprint arXiv:1808.06581.
7. Kusner, M. J., Loftus, J., Russell, C., & Silva, R. (2017). Counterfactual fairness. In Advances in Neural Information Processing Systems (pp. 4066-4076).
8. Lopez-Paz, D., Nishihara, R., Chintala, S., Scholkopf, B., & Bottou, L. (2017). Discovering causal signals in images. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (pp. 6979-6987).
