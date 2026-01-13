---
title: The role of Open Source and Data Privacy for Security
slug: data-security
date: 2026-01-13 18:08:32+0100
tags:
    - life
    - software
    - open-source
---

Internet has been amazing. You send a message. And it reaches the other end of the Earth in seconds. Even more, you can communicate with live video and audio! It seems magical.

Yet it is not. All communication is transmission of energy. Energy travels through space -- which may be occupied by matter or may not. Most space through which communications travel is openly available to everyone. The same space is used by multiple communicators. Does that mean everyone can access the messages I send over the internet?

That's a scary thought. All your bank account details, passwords, private messages, your voice, your tone, your looks*, all travel over the internet. Are these all available to the public at large? (\*You know now with generative AI, your voice and looks are sufficient to prepare videos as if you had done or said things you hadn't!)

Unfortunately, in an unencrypted world, it would be true that everyone can see everyone's messages. You can read malicious users' messages, and they can read yours. Furthermore, what even determines that a message your messaging app says was sent by your friend was really sent by your friend? And not someone else disguised as your friend?

Humans, some of them, are smart. These problems have been known since the dawn of the internet in the 20th century, possibly before. Solutions have been devised against them. Today, for most communication problems in the general, we know that 

<center>
If communications satisfy certain assumptions, then certain particular security benefits are <em>guaranteed</em>. 
</center>

In other words,

<center>
If we build communication softwares that satisfy certain assumptions, then we get certain particular security benefits.
</center>

These benefits include:

- Knowing that the message your messaging app says was sent by a friend was really sent by your friend's device. 
- Ensuring that only you and your friend can read messages sent to each other. That is, your messages are inaccessible to anyone else.
- ... and many more ...

In general, the "friend" may be any other communication end-point, such as your bank, where security is just as important if not more. However,

<center>
How do we know that communication softwares actually satisfy the assumptions required for security?
</center>

Three methods:

1. We trust the word of the person or institute who developed the software *and make profits from the software*. In general, the greater motive here is making monetary profits, since that is a very essential aspect of livelihood of the person or institute. 
2. We trust the word of the person or institute who is *motivated to study and develop the software and ensure the software satisfies the assumptions required for security*. In general, monetary profit as a motive is either absent or very much secondary.
3. We study the workings of the software ourselves.

Both 2nd and 3rd methods require that how the software works is publicly accessible. This means the source code (but also the infrastructure details) are publicly available. In other words,

<center>
Trusting the claim that a particular software is secure becomes easier when the workings of the software are publicly known, that is, it is open source.
</center>

How to find open source softwares?

<center>
An easy method to find the open source alternative for a software is to simply google "open source alternative to <em>software that interests you</em>". You can also append the search by "site:reddit.com" or "site:stackexchange.com" or you can also consult one of your tech-geek friends or family-members.
</center>

It is trivial to see that between two people or institutes:

- One who is motivated by monetary profits
- Another who is motivated by software security

The second category of people or institutes would end up with more secure softwares in any particular class of softwares in the longer run. In other words, in the longer run, the first category of people or institutes are likely to make mistakes even if, besides making money, they too want to make their softwares secure. This is simply because, for the software developers, motivation for software security drives learning and brings in the time to spend on the software and make changes that may go against the monetary motivation.

That people and software developers can make mistakes brings us to the second point of this blog post. Your data includes - your name, phone numbers, email addresses, passwords, bank account numbers, people or institutes you send messages to or receive messages from, what messages you send, which websites you access, how frequently, at what time, for how long, your phone location, when do you leave your home, office or visit a friend, and much more. 

<center>
You would <em>WISH</em> that the banks, institutes, and messaging softwares that have access to your data are actually storing them securely, in a manner that does not permit thieves and malicious actors from misusing your data.
</center>

This is also called a data breach. In 2025 alone, there were [at least 5 data breaches with banking softwares](https://www.cybersecurity-insiders.com/top-5-banking-data-breaches-of-2025-2/) resulting in millions of individuals losing their banking details to malicious hackers. It is not just banking softwares. Data breaches can happen with [car companies](https://therecord.media/8-million-affected-zoomcar-data-breach), [education providers](https://en.wikipedia.org/wiki/Kido_International_cyberattack), [beer companies](https://www.computing.co.uk/news/2025/security/asahi-breach-exposes-customers-details), [sim providers](https://www.scworld.com/brief/almost-27m-sk-telecom-sim-records-compromised), [luxury brands](https://www.yahoo.com/news/articles/kering-confirms-data-breach-192611717.html), and pretty much everything that is connected to internet.

If the softwares were open source, it would be easier to ensure security. However, the next best thing to open source might be data privacy. How do you prevent your data from being misused?

<center>
To prevent your data from being misused, you restrict your data from being accessible. That is, you keep your data <em>private</em>.
</center>

How do you make your data more private? This is a bit like asking *How do I make myself more healthy?* There's no simple answer, although one can try some guidelines! See [here](https://www.reddit.com/r/privacy/wiki/index/#wiki_what_can_i_do_to_protect_my_privacy.3F) or [here](https://www.reddit.com/r/privacy/comments/1cposnq/starting_from_scratch_how_to_delete_my_online/) for a detailed guide. Here's an attempt at some guidelines:

1. Reduce reliance on closed source softwares for information processing. This includes Microsoft Word, Powerpoint, Excel, as well as Google Docs, Slides, and Sheets, and also Apple. Of course, you may be forced to use these apps *because your colleague uses them*. In that case, either convince them to shift to open source alternatives or use the open source alternatives for your personal use cases. Simple alternatives include [markdown](https://www.markdownguide.org/getting-started/), [latex](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes), and [open document formats](https://blog.documentfoundation.org/blog/2025/05/16/what-is-odf/).

2. Try out [Kubuntu](https://www.youtube.com/watch?v=2W7Pi26ZHm8) on newer laptops or [Xubuntu](https://www.youtube.com/watch?v=lnzMl7BFM0Q) to renew old laptops. Be sure to use the "Long-Term Support (LTS)" versions, currently 24.04. You can also try it as a [virtual machine](https://www.youtube.com/watch?v=2uxX0UtInhQ).

3. Switch to secure open-source messaging softwares:

     - [Signal](https://signal.org/) or [Molly](https://molly.im/) *in addition to* Whatsapp, Messenger, Instagram. 
     - [Jitsi](https://jitsi.guide/blog/jitsi-vs-zoom/) *in addition to* Zoom or Google Meet or Teams 
     
4. Use [password managers](https://www.pcmag.com/explainers/why-you-need-a-password-manager-and-how-to-choose-the-right-one) like [Bitwarden](https://bitwarden.com/).  

5. ... You are motivated enough. Read one of those detailed guides now :)

### To sum up

1. Open source aids security. You can find open source alternatives by simply googling "open source alternatives to \<app you want\>". Optionally, you can append the search with "site:reddit.com" or "site:stackexchange.com".

2. Privacy aids security. Privacy is a bit like moving towards a healthy lifestyle. There are lots of small changes in the way. See [this](https://www.reddit.com/r/privacy/wiki/index/#wiki_what_can_i_do_to_protect_my_privacy.3F) or [this](https://www.reddit.com/r/privacy/comments/1cposnq/starting_from_scratch_how_to_delete_my_online/) for a detailed guide.
