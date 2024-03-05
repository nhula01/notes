+++
title = "ml_introduction"
author = ["DESKTOP-PNLN52S"]
date = 2024-02-29T00:00:00-07:00
lastmod = 2024-02-29T00:00:00-07:00
tags = ["noexport"]
draft = false
+++

**Link**:


## Types of Learning {#types-of-learning}


### Supervised (Inductive) learning {#supervised--inductive--learning}

-   This study is done when the training data and desired outputs (labels) are given

-   There are a few algorithms in supervised learning:

<!--listend-->

1.  Regression
    Given a set of \\[ (x\_i,y\_i)\\], we use the set to train the function \\[ f(x)\\] to
    predict y given any value of x.
2.  Classification
    We still train like regression with a different model. In this model, the outputs
    y are classified (like 0 or 1).


### Unsuperivsed Learning {#unsuperivsed-learning}

-   We are only given the data to train without the desired outputs

-   Given x which can have dimension d, each dimention is an attribute.

-   The study of the output will give us some hidden structure of x's


### Semi-supervised learning {#semi-supervised-learning}

-   Similar to supervised learning, but only a few desired outputs are given


### Reinforcement learning {#reinforcement-learning}

-   We give rewards for the actions done
