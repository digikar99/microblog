---
title: Documentation is Troublesome
description: Documentation is Troublesome
slug: documentation
date: 2025-10-30 15:39:12+0100
tags:
    - problem-solving
    - lisp
---

About two months ago, I decided to design a programming language with Python/Julia-like syntax that transpiled to Common Lisp. I called it [Moonli](https://moonli-lang.github.io/). It took about a month of reading, tinkering and thinking to play nice with the extensibility of Lisps. That was very challenging and rewarding. It's usable now.

But the hardest -- most boring -- part has been documentation. I intend the language to cater to people who are new to programming, or at least to Lisps. There have been excellent books on Lisps in general as well as Common Lisp in particular. However, many of them prevent free modification. There are some Common Lisp resources such as [The Cookbook](https://lispcookbook.github.io/cl-cookbook/) that permit reuse, but unfortunately, to me, these do not feel suitable for a beginner. I had originally intended to rely on [ThinkPython](https://allendowney.github.io/ThinkPython/), but it quickly turned out that Lisp concepts can be fairly distant from Python*. Talk of the ideas of image-based development, REPL, symbols, seemed fairly distant (non-existent) in Python-land. Without these concepts, one is essentially throwing the Lisp baby out with the bath water.

I'm evaluating my options:

1. Hire someone: How much am I willing to pay? How familiar will they be with Lisp concepts?
2. Post on lisp community: This feels like being lazy. On the other hand, it is true that after a certain point of time, writing code feels easier that explaining code. At least that's true of me. An ideal documentor needs to be someone who actively enjoys *explaining* code -- and writing down the explanations.
3. Do it myself: I'm currently on this option, at least until I get a first draft. This will probably be slow. Yet, as long as I remain consistent at 6ish hours per week, I get 300 hours a year and 1500 hours over the course of 5 years. That's a lot of time.

Of course, if you wanted to start with Moonli, you can simply open up the Lisp REPL, load Moonli, and dig around and tinker until things start making sense to you. That's how Lisp Hackers operate :).

However, documentation has been a drag on life in general. Active thinking generates a *lot* of thoughts. Connections from one topic to another, new ideas to try out the topics, multiple *aspects* of the same topic linking to different topics in different ways. Often times, I end up leaving them as annotations in pdf files. The worries are two-fold:

1. If I haven't documented my thoughts, what even was the use of thinking actively?
2. If I document my thoughts, they at least need to be interpretable, and this slows down reading a lot.

More so, it is fun to think at the edges. It is fun to make something that was difficult to conceptualize into something that is easier to conceptualize *for myself*. However, the real *output* of thinking lies in whether those conceptualizations make any sense *to others*. But even after conceptualization, there is a step of explication that involves making those vague intuition-based concepts more precise, ideally precise enough for implementation as a computer program. Without this, I'm just cooking up stories or playing word-salad with no grounding. This is cumbersome.

Summarized differently, knowledge may be divided into:

1. You know you know and have documented it for others to know.
2. You know you know.
3. You know you don't know but you can figure it out.
4. You know you don't know how to figure it out, but can figure out how to figure it out.
5. You know you don't know nor how to figure out how to figure it out.
6. You don't know.

I can't have any stances on what I don't know, so 6 is out of discussion. 5 is what I enjoy, but 1 is where things pay off.

*If anything, the use of Lisp concepts is one of the primary motivations to develop Moonli instead of using Python or Julia.

