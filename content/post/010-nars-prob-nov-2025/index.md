---
title: A non-equivalence between Non-Axiomatic Logic and Probability Theory (Nov. 2025)
slug: nars-prob-nov-2025
date: 2025-11-05 18:32:41+0100
math: true
tags:
    - cognitive-science
---

People have beliefs about the world*. The beliefs have uncertainties. How do we characterize or represent these uncertainties?

In both the (computational) cognitive and computational sciences, beliefs are often represented as a parameter value $\theta = \theta_0$. The truth value of the belief may be true or false characterized by a scalar value $P(\theta = \theta_0)$, called the probability of the belief. The spread of the probability distribution $P(\theta)$ (often the standard deviation $\sigma$) gives us the uncertainty of the belief.

However, note that this uncertainty is characterized in the context of a belief space, that is, the set $\mathit S$ of values of $\theta$. The uncertainty then is with respect to other beliefs $\theta_0\' \neq \theta_0$.

The [non-axiomatic logic framework](https://link.springer.com/book/10.1007/1-4020-5045-3) by [Pei Wang](https://cis.temple.edu/~pwang/) et al. instead characterize the truth-value of the belief by a two-length tuple $(f,c)$, the *frequency* and the *confidence* respectively. This allows us to characterize beliefs independently of each other. The different beliefs may later be compared against each other.

Contrast the two situations:

1. 10 coin tosses with 8 heads
2. 1000 coin tosses with 800 heads

It is true that the bias of the coin in the second situation may be judged as being less uncertain than the first. Probability theory explains it as the two probability distributions same mean but different variations. Non-axiomatic logic explains it as two beliefs having the same frequency but different confidence.

For the class of situations involving coin tosses, it is also the case that different values of $\theta$ are mutually exclusive. It is this mutual exclusivity that allows the use of Probability theory to model belief updates. In cases where mutual exclusivity fails, Probability theory becomes misapplied. NAL can take-over in those situations with contradictory beliefs.

However, events can always be modeled so that they are mutually exclusive. To talk about the uncertainty of a particular belief $\theta = \theta_0$ independent of other beliefs $\theta = \theta_0\'$ requires assigning each belief to its individual probability distribution. ~Often this could be a normal distribution $\sout{\mathit N(\theta, \sigma)}$ characterized by a mean $\sout{\theta}$ and standard deviation $\sout{\sigma}$.~ However, this implies that the set of mutually exclusive alternatives is $\mathit S: \\\{\theta = \theta_0\', \theta \neq \theta_0\'\\\}$ and likewise for each value of $\theta$. Each of the two elements of the set can then obtain a probability independent of other values of $\theta$. But, this does not allow us to represent what might be considered the *uncertainty* in probability.

Even besides this non-equivalence, the two frameworks diverge a fair bit. Pei Wang has also talked about [Belief Revision in Probability Theory](https://arxiv.org/pdf/1303.1517) discussing other issues with probabilities. I remain failed to grasp anything beyond intuitive ideas, perhaps, lacking a background in philosophy and history of probality theory or my own peculiarities. While Non-axiomatic Logic has seen a lot of development, it remains true that the research developments in Probability Theory has been humongous.

*Or if you are a Cognitive Semanticist like Gardenfors, I'd restate as: these are beliefs about represented features of the world.

