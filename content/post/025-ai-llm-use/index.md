---
title: How do I use AI (LLMs)?
slug: ai-llm-use
date: 2026-02-17 00:28:43+0100
tags:
    - artificial-intelligence
    - productivity
    - software
---

Over the past few days, I have been asked the "How do I use AI?" question a few times. So, here's an attempt at a common answer along with a few potential FAQs.

**Do I think AI will replace us soon (= next 5 years)?**

My own long term interest has been in the development of AI that can be at par with humans in certain ways. And to the extent it is not at par with humans, it will remain a topic of research. What certain ways? Answering that can be multiple research programs in itself! One aspect is causality, and perhaps, the most accessible resource is [the first chapter of Judea Pearl's The Book of Why](https://bayes.cs.ucla.edu/WHY/why-ch1.pdf).

 AI *looks* great only at tasks you are bad at, because you don't even (i) have the basic knowledge to judge it (ii) have not spent enough time to judge its output. Mere readability and plausible sounding is not understanding, remember? 

Briefly, no, I do not think AI will replace us in the next 5 years. One reason is causality. But, there are multiple reasons.

**Do I think companies will replace human employees because of AI?**

This is a concern I share. To the extent that companies want to *cut down costs* and generate *plausible looking progress*, AI seems like a great deal, unfortunately. Crony capitalism at its best. I'd guess the only good way out is unionizing. Employee unions are also helpful in other ways beyond the employment threats that AI supposedly places.

In fact, I now fear, that before the apocalypse due to climate change, we will end up in a situation, where many critical softwares are written by AI which has no causal understanding or any of the other forms of understanding evolution has endowed us with. The critical softwares written by AI and unverified by humans will have many edge cases which would have been detected by human teams. These critical softwares will then trigger system failures affecting the lives of many. I can only hope there are enough safeguards in place before AI written softwares reach hospitals, medical devices, nuclear systems, power grids, flight systems, car softwares, and unimaginably many others. If you are using Windows, you might already have received a taste of [things to come](https://tech.yahoo.com/computing/articles/broken-patches-ai-code-windows-193024345.html). Also see [other](https://www.techrepublic.com/article/ai-generated-code-outages/) [posts](https://www.bugsink.com/blog/copilot-induced-crash/) [like these](https://www.reddit.com/r/engineering/comments/1oxqh9d/young_engineers_do_not_trust_ai_at_its_word/).

**Do I think AI is totally useless? Do I use AI? What do I use it for?**

At its core, generative AI -- the LLMs powering ChatGPT -- are based on word/picture embeddings generated using "fill in the missing word/token/picture given the context". In other words, these tools are *amazing* at finding statistical regularities in the text. And to some extent, these also approximate semantic understanding. They key word is *some*. Given a question or query, these tools can allow you to easily narrow down your search to a 100 documents in a million. Which of those documents are most relevant is for *you* to find out. In this sense, they are amazing.

In other words, I think AI works great as glorified search engines. However, a critical step is to not trust the output it generates, but, depending on the stakes involved, go and check the references it cites.

Many times the AI will say something that the citation does not say at all! Additionally, in an attempt to summarize the reference, it loses the nuance. For instance, on stackexchange websites, if an answer is bad, someone will point it out in the comments. Amongst two answers, if one answer has 900 upvotes and the other has 10, it's more plausible that the one with the 900 upvotes is better in some way. (In what way? For that you might need to dig around more.) AI can lose out this context. It can also lose out the context that someone answered, someone countered, the answerer countered and clarified, and therefore, the answer is actually good and not bad as the first comment might make one think.

I'm also aghast to say, AI can sometimes provide references that even my supervisors might not have felt relevant. Instead of asking AI the question, "How do I ..." or "What is the ...", ask it "Who has written an article or resource on how do I ..." or "Who has written an article or resource on what is the ...". Then check out the references it cites, and use your own brains.

I don't need to write repetitive emails often. And it is also acceptable (and preferred) to reply to emails briefly in one sentence. So, that, hasn't been my common use.

I think there are better tools for spelling and grammar than general purpose LLMs. (Looks at [Grammarly](https://www.grammarly.com/).) I still think it is better than nothing to ask them to review short sections of your work. Again, take their answers with skepticism. As you learn more about different kinds of writing, you will discover new rules of thumbs to keep in mind.

I use AI to generate code templates as well as for "function finding": Quick, *How do I remove whitespaces from the end of a string in Python? In Javascript? In Common Lisp?* 

Based on examples I see in the wild (eg. [this in Julia](https://www.reddit.com/r/Julia/comments/1p4i7yd/building_standalone_julia_binaries_a_complete/), [the above in Python]([posts](https://www.bugsink.com/blog/copilot-induced-crash/)), [this in Common Lisp](https://www.reddit.com/r/Common_Lisp/comments/1qtwd45/comment/o37p1lx/), I don't trust AI to generate good code. And no, it is not a matter of giving [more](https://github.com/anthropics/claude-code/issues?q=is%3Aissue%20state%3Aopen%20does%20not%20follow%20instructions) [specific instructions](https://github.com/google-gemini/gemini-cli/issues?q=is%3Aissue%20state%3Aopen%20does%20not%20follow%20instructions) -- it is an open issue that coding agents do not obey your instructions. Perhaps, because they do not have any notion of an "instruction" at all. All they are generating is plausible looking text given the context. Additionally, writing code is not the hard part. Reading, understanding, maintaining, and writing code that is easy to read, understand and maintain is hard. Better to do it on your own than read through someone's shit.

The developer of Claude Code -- Anthropic itself -- highlights that [the benefits from AI might be just about 10% even while the impact on understanding and skill formation can be larger](https://www.anthropic.com/research/AI-assistance-coding-skills).

That said, given some possibilities highlighted above, I have also been experimenting with [ollama](https://ollama.com/) and [llama.cpp](https://github.com/ggml-org/llama.cpp). I thought I wasn't ever going to need more than 32GB RAM. Boy, I am wrong, I'm going to need 64GB RAM, particularly with modern chips coming with powerful GPUs and NPUs.

I also tried to think up a method by which AI can be made to respect the possibilities it is provided with. Unfortunately, it seems that unless one constrains those possibilities externally, there is no way to constrain them internally. But as soon as one imposes external constraints, one loses out on the composability that AI seemingly provides. In other words, human-like intelligence is an unsolved problem.

Lastly, [Character AI](https://character.ai/) can be surprisingly good for general chat as well as if you enjoy roleplays but haven't formed your own roleplay-group. Still, they can get quite unreasonable at times.

Briefly, AI is useful for querying its vast knowledge base to find references that you can judge for yourself. And also for some creative tasks. 

Bonus: [Noam Chomsky: The False Promise of ChatGPT](https://www.nytimes.com/2023/03/08/opinion/noam-chomsky-chatgpt-ai.html)
