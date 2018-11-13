---
title: "The Road to Strong AI (According to Judea Pearl)"
layout: post
date: 2018-10-28 19:51
image: /assets/images/markdown.jpg
headerImage: false
tag:
- causality
- ai
- judea pearl
- machine learning
- intelligence
blog: true
author: tanmayee
description: What more do we need in order to reach a stage where Artificial Intelligence rivals human intelligence?
---

*This post is a brief summary of Judea Pearl's paper "Theoretical Impediments to Machine Learning With Seven Sparks from the Causal Revolution" [[arxiv](https://arxiv.org/abs/1801.04016)]*

-----

What more do we need in order to reach a stage where Artificial Intelligence rivals human intelligence?

Consider an eagle's eyesight - its vision system has evolved over a period of millions of years, by taking in a stream of sensory inputs and optimizing its performance.

This is Darwin's evolutionary process at work, and it's slow. Most machine learning algorithms operate in this way.

![Eagle](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Golden_Eagle_eye.jpg/512px-Golden_Eagle_eye.jpg)
<figcaption class="caption">The Eye of a Golden Eagle (Wikimedia Commmons)</figcaption>
<br>

On the other hand, humans were able to invent telescopes and microscopes in a few thousands of years, which rival or surpass the best vision systems found in nature.

**How did this super-evolutionary process happen?**

Pearl argues that this was possible because humans have a "blueprint of the environment", a mental model of how things work, and this helps in imagining alternate universes and hypothetical situations that have not actually happened.

![Telescope](https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/12.6%22_Fitz_telescope_in_Ann_Arbor.jpg/512px-12.6%22_Fitz_telescope_in_Ann_Arbor.jpg)
<figcaption class="caption">The Fitz Telescope at Ann Arbor (Wikimedia Commmons)</figcaption>
<br>

How might we build a system that can answer retrospective, hypothetical "what-if" questions? According to Pearl, just data is not enough, and model-driven reasoning is necessary for strong AI.

### The Causal Hierarchy
Causal theory helps in classifying information into a three level hierarchy. This sharp categorization helps in reasoning over the nature of information required to answer questions from a certain level. Questions at a particular level can be answered only if information from successive levels are available.

![Causal Hierarchy](https://raw.githubusercontent.com/triptoes1/triptoes1.github.io/master/assets/images/causal-hierarchy.png)

1. Association questions are inferred from just data, and nothing more.
2. Intervention questions involve changing what is observed.
3. Counterfactual questions are retrospective, they ask what would have happened if we had made a change.

Counterfactual questions subsume association and intervention questions.

Structural Causal Models (SCM) can answer counterfactual questions. Hence, they have the capacity to answer even intervention and association questions. The theory of Structural Causal Models allows us to formally codify background knowledge, and warns about the limitations of methods that only use data for estimation. Basically, certain classes of questions (specifically interventions and counterfactuals) cannot be answered from data alone.

### SCM Inference Engine
![SCM Engine](https://raw.githubusercontent.com/triptoes1/triptoes1.github.io/master/assets/images/scm-inference-engine.png)

If we were to build an inference engine using SCM, it would look like this -

1. Inputs:
    * Query, which is the question that needs to be answered
    * Assumptions, which are usually codified by a directed graph
    * Data
2. Outputs:
    * Estimand is a recipe or formula to answer the query based on assumptions
    * Estimate is the answer to the query, which is computed from the estimand and the data
    * Fit indices are a measure of compatibility between the data and the assumptions

### Conclusion
There are theoretical limitations to the kinds of questions that can be answered from data alone. It is worthwhile to explore if model-driven reasoning is the missing link to human level artificial intelligence. As Pearl says -

> Data alone are hardly a science, regardless how big they get and how skillfully they are manipulated.
