---

layout: page
title: the CLaS task
permalink: /task/
nav: true
nav_order: 1

---

The CLaS shared task, based on **CLaS-Bench** (Gurgurov et al., 2026), asks participants to control the output language of a large language model (LLM) using inference-time interventions. Given a question in a source language, participants steer the model to produce a relevant and coherent answer in a specified target language.

## Tracks

There are three main tracks and one bonus track.

### T1: High-Resource Steering

Participants steer inputs from **10 high-resource languages** into the same set of languages, excluding same-language pairs.

* Languages: `ar`, `de`, `en`, `es`, `fr`, `ja`, `zh`, `ru`, `hi`, `ko`
* **90 language pairs**
* Final results are averaged across all language pairs.
* **2 rankings**, one per model.

### T2: Low-Resource Steering

Participants steer inputs from the same 10 high-resource languages into **10 low-resource languages**.

* Source languages: the 10 languages from T1
* Target languages: `cs`, `el`, `fa`, `vi`, `uk`, `mt`, `no`, `sw`, `th`, `tr`
* **100 language pairs**
* Final results are averaged across all language pairs.
* **2 rankings**, one per model.

### T3: Full Multi-Language Steering

Participants steer inputs from all **20 languages** covered by T1 and T2 into one selected high-resource target language.

* Target languages: `ja`, `ru`, `de`
* **19 source languages per target language**
* This track supports a more detailed analysis of steering into a specific target language.
* **6 rankings**, one per model and target language.

### Bonus Track: Multilingual Refusal

Participants steer inputs from the 10 high-resource languages into a refusal mode in the target language.

* Source languages: the 10 high-resource languages from T1
* **10 × 10 language pairs**
* **2 rankings**, one per model.

## Models

The two required models are:

* `meta-llama/Llama-3.1-8B-Instruct`
* `CohereLabs/tiny-aya-global`

Participants are also free to explore additional models.

## Evaluation

Submissions will be evaluated automatically on our side. To keep the final test data private, participants should submit their **code and requirements file**, or a **Docker image**. More details about the submission process and requirements will be provided closer to the evaluation stage.

More details about the evaluation process and submission format are available in our [GitHub repository](https://github.com/d-gurgurov/CLaS-SemEval-2027).

## Data

We provide:

* **FLORES-200 devtest** subsets for the languages used in the task, for identifying language-related components.
* **CLaS-Bench** as a validation dataset.

## Baseline

A simple baseline using prompt-based language steering is provided in the code repository for reference.

## References

Andy Arditi, Oscar Obeso, Aaquib Syed, Daniel Paleka, Nina Panickssery, Wes Gurnee, and Neel Nanda. 2024. [Refusal in language models is mediated by a single direction](https://proceedings.neurips.cc/paper_files/paper/2024/hash/f545448535dfde4f9786555403ab7c49-Abstract-Conference.html). *Advances in Neural Information Processing Systems*, 37, 136037–136083.

Daniil Gurgurov, Yusser Al Ghussin, Tanja Baeumel, Cheng-Ting Chou, Patrick Schramowski, Marius Mosbach, Josef Van Genabith, and Simon Ostermann. 2026. [CLaS-Bench: A Cross-Lingual Alignment and Steering Benchmark](https://aclanthology.org/2026.findings-acl.1086/). In *Findings of the Association for Computational Linguistics: ACL 2026*, pages 21591–21628. Association for Computational Linguistics.
