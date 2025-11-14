---
title: Some issues with Probabilities and Bayesianism for Unified Models of Cognition or Artificial General Intelligence 
slug: prob-issues
date: 2025-11-14 13:49:34+0100
math: true
tags:
    - cognitive-science
    - artificial-intelligence
---

Bayesian Methods provide a reasonable model of updating Probabilities of Beliefs in the face of upcoming information. Taken as a framework theory (unfalsifiable) of cognition or intelligence for a particular task, these can be pretty good for providing a precise null theory to compare cognition against (citation needed). Similarly, it also provides a good alternative to the Frequentist approaches to statistical inference.

However, it becomes problematic when it starts being used as a model of unified cognition or general intelligence.

Wikipedia provides the motivation for [Probability Theory](https://en.wikipedia.org/wiki/Probability_theory) as:

> Probability is a way of assigning every "event" a value between zero and one, with the requirement that the event made up of all possible results (in our example, the event {1,2,3,4,5,6}) be assigned a value of one. To qualify as a probability distribution, the assignment of values must satisfy the requirement that if you look at a collection of mutually exclusive events (events that contain no common results, e.g., the events {1,6}, {3}, and {2,4} are all mutually exclusive), the probability that any of these events occurs is given by the sum of the probabilities of the events.

This already presents several issues:

1. You require a well-specified set. There's no specification how to assign probability to a new event that is outside the set.
2. Probabilities should be kept consistent with each other, respecting [its axioms](https://en.wikipedia.org/wiki/Probability_axioms). Not doing so leads to [Dutch books](https://en.wikipedia.org/wiki/Dutch_book_theorems#Dutch_books).
3. The uncertainties quantified by probabilities are relative uncertainties rather than absolute ones. This relates to the first point. [I have argued about this before.](https://digikar99.github.io/microblog/p/nars-prob-nov-2025/)
4. When one tries to quantify the uncertainty of all beliefs by probabilities, and tries to remain consistent, this can require updation across a wide range of beliefs. This can be computationally expensive. It is also dissimilar to humans who seem to be able to hold mutually contradictory beliefs (as long as they are "far apart" in reasoning chains).

To actually state the resulting unified model of cognition or general intelligence rigorously, one needs to specify what the probabilities are *of*, that is, what are the elements of the set? I have seen zero discussion of this in Cognitive Science. Fortunately, there is a relevant entry in the [Stanford Encyclopaedia of Philosophy](https://plato.stanford.edu/entries/logic-probability/) that discusses Modal Probability Logics and First-order Probability Logic.

Classical mathematical (first-order) logic has several issues. Chapter 1 of Pei Wang's book on [Non-Axiomatic Logic](https://www.worldscientific.com/worldscibooks/10.1142/8665#t=aboutBook) discusses these. Several of them remain even after mixing probabilities and first order logics:

1. The truth-value itself may be dependent on assumptions. Thus, a change of assumptions (which a unified model of cognition must be able to handle) can necessitate revision of truth-values.
2. Reasoning involves induction, abduction, analogy, and other types of inference beyond deduction itself.
3. Classical logic leads to logically correct but intuitively problematic inferences. See [Paradoxes of Material Implication](https://en.wikipedia.org/wiki/Paradoxes_of_material_implication).

There is talk on how bayesian updates provides revision. There is work on how hierarchical bayesian models can be used for induction, abduction, etc. There is work on incorporating causality into probabilities. Intuitively, until they are fully specified, that is, as good as a mathematical theory, they are simply models of cognition with unspecified assumptions in the researchers' heads. They are not yet unified models of cognition that can be implemented in a machine to yield artificial general intelligence. Concretely, I still do not grasp the arguments.

Is there an alternative? There are already [many branches of logic](https://en.wikipedia.org/wiki/Outline_of_logic#Branches_of_logic). There's also a book written by Graham Priest on [Non-Classical Logic](https://en.wikipedia.org/wiki/An_Introduction_to_Non-Classical_Logic). And finally, the one that introduced me to these issues is Pei Wang's work on [Non-Axiomatic Logic](https://www.worldscientific.com/worldscibooks/10.1142/8665#t=aboutBook) that tries to draw upon several non-classical logics at once.
