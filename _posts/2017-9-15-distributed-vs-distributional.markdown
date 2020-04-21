---
title: Distributional Similarity vs Distributed Representation
layout: post
date: 2017-9-15 12:17
image: /assets/images/markdown.jpg
headerImage: false
tag:
- nlp
- deep learning
- distributional similarity
- distributed representation
- language
- natural language processing
blog: true
author: tanmayee
description: What is the difference between distributional similarity and distributed representation?
image: /assets/images/brain.png
headerImage: false
use_math: true
---
If you are an NLP beginner (like me), then it is common to come across the terms *distributional similarity* and *distributed representation* in the context of word embeddings. <!--more-->It's easy to get confused between the two, or even assume that they mean the same thing. (They do sound very similar to each other.) Distributed representations are usually computed from distributional similarity, but on a conceptual level, they mean different things.

### Distributional Similarity
{%epigraph 'You shall know a word by the company it keeps.' 'J R Firth, 1957' %}

Distributional similarity is an important hypothesis in linguistics, and the main idea is surprisingly simple - the meaning of a word depends on the words that surround it (its context), and words which have similar contexts must be related to each other.

For example, let's take the word *top*, and two sentences -

> This purple top will go well with my white skirt.

> We took two hours to reach the top of the hill.

Even though the same word *top* was used in both sentences, they convey different meanings because of the other words that surrounded them.

Now, let's replace *top* in the first sentence with *shirt*. The new sentence - 'This purple shirt will go well with my white skirt' is a perfectly sensible sentence. Distributional similarity hypothesizes that *top* and *shirt* must be related to each other because they have similar contexts.

The opposite of distributional similarity is denotation. The denotation of a word is the dictionary meaning, or its precise, literal meaning, devoid of emotion, attitude and colour. In some sense, denotation of a word is an absolute meaning of sorts, and distributional similarity is relative to a word's context.

### Distributed Representation
Before we understand distributed representations, let's look at its opposite, localist representations. Suppose we have a fixed vocabulary of size $V$, and we want a vector representation of a word from this vocabulary. The localist representation would be to take a vector of length $V$ where $V_i = 1$ where $i$ is the index of the word in some ordering of the vocabulary. For all $V_j$ where $j \neq i$, the entry in the vector would be $0$. (One hot encoding)

For example, if we had a vocabulary {aardvark, apple, ..., zebra}, the localist representation of apple would be $\begin{bmatrix}0 & 1 & 0 & \ldots & 0\end{bmatrix}$.

The size of these vectors scales linearly with vocabulary size $V$. Also, there is no in-built notion of similarity between them.

Distributed representations are the opposite of localist representations. They are dense vectors, which are typically much smaller than the vocabulary size, and are designed in such a way that they capture similarity between related words. [Word2vec](https://code.google.com/archive/p/word2vec/) and [GloVe](https://nlp.stanford.edu/projects/glove/) are distributed representations for large vocabulary sizes.


### References
Lecture 2 | Word Vector Representations: word2vec. (2017). YouTube. Retrieved 15 September 2017, from <https://youtu.be/ERibwqs9p38>
