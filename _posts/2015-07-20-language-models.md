---
layout: post
title: Language models
---

A language model is a probability distribution, mapping a specific sequence of words/characters/tokens to its likelihood of occuring. This is useful for many NLP tasks: word prediction, spell checkers, machine translation, speech recognition, information retrieval, summarization, etc. By training a language model on a large amount of (presumably (mostly) correct) natural language text, likely word sequences can be distinguished from unlikely ones.

This includes word sequences that are correct, but contain uncommon words or phrases. For example, `"a good"` is more likely to be followed by the word `"day"` than the word `"goose"`. The language model knows this because in the data, it saw `"a good day"` more than it saw `"a good goose"`. (And `"good day"` more than `"good goose"`, and `"day"` more than `"goose"`...)

Language models can also distinguish between grammatical and ungrammatical phrases, but not because they actually know what is ungrammatical. A language model will assign low probability to ungrammatical sequences, simply because those sequences were not seen in the data.

There are a lot of details I'm leaving out (some of which I've yet to learn myself), but I'll address those in the next few weeks. I am going to do a series of posts about language models, divided (roughly) into the following sections:

- Data
- N-gram models
	- Unknown words
	- Smoothing
- Neural net models
- Other models
- Evaluation

More than just describing these concepts, I will actually be implementing as much as I can. The code will be available on github, and maybe even useful to someone else out there trying to break into the NLP world!
