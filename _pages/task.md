---
layout: page
title: the task
permalink: /task/
nav: true
nav_order: 1
---

### The CLaS task

The CLaS shared task, based on CLaS-Bench (Gurgurov et al., 2026), asks participants to control the output language of a large language model (LLM) using inference-time interventions. Given a question in a source language, participants must steer the model to produce a relevant, coherent answer in a specified language.


There will be three tracks and a bonus track: 

**T1: High-Resource Steering.** Participants steer
all questions from 10 high-resource languages into
the same set of high-resource languages, crosslingually (excluding same-language steering), resulting in a total of 90 language pairs. Final results
are reported as the average score across all language pairs.

**T2: Low-Resource Steering.** Participants steer
all questions from 10 high-resource languages into
a set of 10 low-resource languages, cross-lingually,
resulting in 90 language pairs. Final results are
again averaged across language pairs.

**T3: Full Multi-Language Steering.** Participants steer from all 20 languages covered in T1
and T2 into one selected high-resource target language (e.g., Japanese) out of 5 pre-selected ones.
This track is intended to support deeper analysis of
steering into a specific target language and to test
whether methods generalize across a broad range
of source languages, including low-resource ones.

**Bonus Track: Multilingual Refusal.** Participants steer the model into refusal mode in a specified target language, inspired by Arditi et al. (2024)
who do this for English. Given a set of source language prompts, the steered model must produce refusal responses in the target language. This
track aims to push safety-relevant interpretability
research beyond English.

**More information coming soon!**

#### References

Andy Arditi, Oscar Obeso, Aaquib Syed, Daniel Paleka, Nina Panickssery, Wes Gurnee, and Neel Nanda. 2024. [Refusal in language models is mediated by a single direction](https://proceedings.neurips.cc/paper_files/paper/2024/hash/f545448535dfde4f9786555403ab7c49-Abstract-Conference.html). Advances in Neural Information Processing Systems, 37, 136037-136083.

Daniil Gurgurov, Yusser Al Ghussin, Tanja Baeumel, Cheng-Ting Chou, Patrick Schramowski, Marius Mosbach, Josef Van Genabith, and Simon Ostermann. 2026. [CLaS-Bench: A Cross-Lingual Alignment and Steering Benchmark](https://aclanthology.org/2026.findings-acl.1086/). In Findings of the Association for Computational Linguistics: ACL 2026, pages 21591–21628, San Diego, California, United States. Association for Computational Linguistics.





