---
title: Memory (Oct. 2025)
description: Thoughts on Memory as of Oct. 2025
slug: memory-oct-2025
date: 2025-10-31 13:00:08+0100
math: true
tags:
    - cognitive-science
---

How humans learn and store information and knowledge has been interesting to me. Although not enough to pursue a doctoral research on it. Although, it is also the case that I was advised not to silo myself into a "topic of cognition" but rather to start from an intriguing phenomenon and let that phenomenon guide my investigation. I think I like that advice.

So, how do I think human learning and memory work? Here's an attempt.

Given an organism in an environment, the organism's sensors make (transduce) sensory representations $S$ from the environment. This could involve electromagnetic radiation such as light, or vibrations such as by sound or ultrasound, or tactile such as by touch, or something more exotic. The environment may be external to the organism or it could be internal, to account for hunger, thirst, etc. For simplicity, one may assume that the same environment produces the same sensory representations. Thus, its sensors may be said to be *functional* (as in [functional programming](https://www.reddit.com/r/explainlikeimfive/comments/1cq60cn/eli5_what_is_functional_programming_and_how_is_it/)). If we allowed sensors to be non-functional in characteristic, it seems possible to attribute the entire process of cognition to sensors alone (citation needed). Such a sensory representation may also have a temporal component.

Such a sensory representation $S$ only lasts very briefly (citations on classic sensory memory experiments). It must be *transformed* into a conceptual representation $C_S$ for it to be available in the long run. The conceptual representation in turn may depend on an earlier conceptual structure, so we label the conceptual representation with a timestamp $t$: $C_{S,t}$. Doing so devoids the conceptual representation from a temporal component.

It is ubiquitous that episodic (layman speak: contextual) and semantic (layman speak: context-free) memories are two aspects of our experience. How do these two aspects arise?

A conceptual representation $C$ is a structure built out of concepts available from an existing concept-database $\mathcal C$. The structure may be atomic or compound. The concept databases includes atomic-concepts (nouns) as well as relation-concepts (adjectives, verbs, prepositions) to describe or combine existing structures into new compound structures. This raises several questions:

1. What are atomic-concepts? Or what determines whether some concept is atomic?
2. How are relation-concepts created?

The concept database also allows us to compute the probability $P(C\' | \mathcal C_{S,t}, S)$ of new conceptual structure $C\'$ given the current concept-database $\mathcal C$, the current conceptual representation $C_{S,t}$, and sensory representation $S$. I use probability for convenience, but it could be any other measure of uncertainty.

To answer the questions, we require postulating two concept-learning processes. 

- The first process $\mathcal P_{\text{atomic}}$ can make new atomic concepts out of sensory representations. An atomic concept $C\'$ is characterized by *traces* of sensory representations that were used to make the concept, as well as some conditional probabilities $P(C\' | \mathcal C_{S,t}, S)$. What exact conditional probabilities are involved might be an open question. Perhaps they correspond to the concepts $C_{S,t}$ used to *predict* this new concept $C'$? Additionally, what do I mean by *traces*?
- The second process $\mathcal P_{\text{relational}}$ can make new relational concepts out of sensory representations as well as existing concepts.

Stating this also partly answers question 2: A concept is atomic if it depends  solely on sensory representations. A concept is relational if it depends on both sensory representations or other concepts. But this raises yet another question: what do I mean here by *depend on*?

Semantic Memory is identical to the concept database $\mathcal C$.

We say that a concept is *active* if it is a part of the current conceptual representation $C_{S,t}$.

Episodic Memory works as follows:

1. The organisms cognitive system produces a sequence of conceptual representations $(C_1, ..., C_t)$ from the sucessive sensory representations its sensors produce. In a well-functioning organism, the production of such a sequence also creates a *sequence* of *activations* corresponding to different concepts. This sequence of activations is recorded by some cognitive-subsystem (perhaps hippocampus?).
2. During recall, this sequence of activations is replayed back by the cognitive-subsystem that had recorded the activations. Because recall involves relations to concepts that are earlier or later in the sequence, episodic memory is conceptual.

Open questions include:

- What exactly do I mean by *depend*? 
- How exactly do the concept-generating processes operate? This needs to be specified in (much) more detail.
- What do I mean by *traces*?

And finally, what predictions does this make?

Of course, comparison with existing literature is an open task on its own.
