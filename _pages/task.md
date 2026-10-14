---
layout: page
title: the CLaS task
permalink: /task/
nav: true
nav_order: 1
---

The CLaS shared task, based on **CLaS-Bench** (Gurgurov et al., 2026), asks participants to control the output language of a large language model (LLM) using inference-time internal interventions. Given a question in a source language, participants steer the model to produce a relevant and coherent answer in a specified target language.

The task comprises three main tracks and one bonus track. The main tracks focus on language steering across high-resource and low-resource languages, while the bonus track investigates multilingual refusal behavior.

## Tracks

### T1: High-Resource Steering

Participants steer inputs from 10 high-resource languages into the same set of languages, excluding same-language pairs.

- **Languages:** `ar`, `de`, `en`, `es`, `fr`, `ja`, `zh`, `ru`, `hi`, `ko`
- **Language pairs:** 90
- **Evaluation:** Results are averaged across all language pairs.
- **Rankings:** Two rankings, one per model.

### T2: Low-Resource Steering

Participants steer inputs from the same 10 high-resource languages into 10 low-resource target languages.

- **Source languages:** The 10 high-resource languages from T1.
- **Target languages:** `cs`, `el`, `fa`, `vi`, `uk`, `mt`, `no`, `sw`, `th`, `tr`
- **Language pairs:** 100
- **Evaluation:** Results are averaged across all language pairs.
- **Rankings:** Two rankings, one per model.

### T3: Full Multi-Language Steering

Participants steer inputs from all 20 languages covered by T1 and T2 into one selected high-resource target language.

- **Target languages:** `ja`, `ru`, `de`
- **Source languages:** The other 19 languages for each selected target.
- **Evaluation:** Results are aggregated for each target language.
- **Rankings:** Six rankings, one per model and target language.

This track enables a more detailed analysis of steering into a specific target language across a broad range of source languages.

### Bonus Track: Multilingual Refusal

The bonus track focuses on generating appropriate refusals in the requested target language.

- **Source languages:** The 10 high-resource languages from T1.
- **Questions:** The same questions as T1, with 100 questions per language.
- **Evaluation:** The protocol for this track will be published separately.
- **Rankings:** Two rankings, one per model.

## Models

The two required models are:

- [`meta-llama/Llama-3.1-8B-Instruct`](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct)
- [`CohereLabs/tiny-aya-global`](https://huggingface.co/CohereLabs/tiny-aya-global)

Participants are welcome to explore additional models during method development. Official evaluation will use the two required models.

## Permitted Methods

The CLaS shared task focuses on **inference-time internal interventions** for controlling the output language of LLMs.

Adding a target-language instruction to the input or system prompt is not permitted as a steering method. Participants are expected to intervene directly in the model's internal computations using interpretable methods. Examples of permitted approaches include:

- **Neuron-level interventions:** identifying and manipulating individual MLP neurons.
- **Attention-head interventions:** identifying and modifying the contributions of individual attention heads.
- **Circuit-level interventions:** identifying and intervening in computational circuits within the model.
- **Activation-vector steering:** adding, subtracting, or modifying activation vectors to influence language generation.
- **Subspace-based interventions:** identifying and manipulating subspaces associated with language or other relevant attributes.
- **Sparse autoencoder (SAE) feature interventions:** identifying and modifying interpretable features learned by sparse autoencoders.
- **Probe-based methods:** using probes to identify interpretable directions or structures in the model's representations and intervening along them.
- **Other representation-level methods:** manipulating other interpretable internal representations or components of the model.

These examples are not exhaustive. Other methods are welcome provided they directly intervene in the model's internal computations.

## Evaluation

Submissions will be evaluated automatically by the organizers using two criteria:

- **Language compliance:** Whether the generated answer is in the requested target language, assessed using language identification.
- **Query relevance:** Whether the generated answer appropriately addresses the input question.

Optimizing for language compliance alone is not sufficient: answers must also remain relevant to the input query.

### Test set and submission procedure

The final evaluation will use **100 previously unseen questions per language** in the evaluation suite. Test questions will not be provided to participants in advance.

The organizers will run submitted systems on their own hardware, using A100 and H100 GPUs. Participants will submit their code and dependency requirements through a form on the shared task website. Further details about the submission format and requirements will be announced closer to the evaluation period.

During the evaluation period (**January 10-31, 2027**), each team will be allowed two test submissions per track and one final submission per track. The final submission will be used for the official rankings.

### Evaluation resources

The following resources are available in the [GitHub repository](https://github.com/d-gurgurov/CLaS-SemEval-2027):

- **FLORES-200 devtest:** Subsets for the languages used in the task, which participants can use to identify language-related components.
- **CLaS-Bench:** A validation dataset for developing and evaluating steering methods.
- **Baseline implementations and evaluation code:** Tools for running baseline generations and evaluating results.

A prompt-based language-steering baseline is provided for reference and comparison. Since the official task focuses on internal interventions, prompt-based target-language instructions are not eligible as the steering method for official rankings.

## Registration and Submission

Teams interested in participating in the CLaS Shared Task can [register here](/register/).

System submissions will open on **January 10, 2027**, and the evaluation period will run until **January 31, 2027**. Each team will be allowed two test submissions per track and one final submission per track. The final submission will be used for the official rankings.

Participants will submit their code and dependency requirements through a form on the shared task website. The submission form and detailed instructions will be made available closer to the evaluation period.

<div class="task-buttons" style="margin: 0;">
  <a href="/register/" class="btn btn--primary">Register your team</a>
  <span class="btn" aria-disabled="true" style="opacity: 0.55; cursor: not-allowed;">Submissions open January 10, 2027</span>
</div>
<div style="height: 16px;"></div>

## Ranking and Awards

We will maintain a separate ranking for each official evaluation category. Awards will be given to the **1st place** systems in each ranking.

In addition, we will present a **Best Interpretability Insights Award** to recognize particularly interesting findings about the internal mechanisms of multilingual language steering. This award will be decided during the paper reviewing period, taking into account reviewers' assessments and preferences.


## References

Andy Arditi, Oscar Obeso, Aaquib Syed, Daniel Paleka, Nina Panickssery, Wes Gurnee, and Neel Nanda. 2024. [Refusal in language models is mediated by a single direction](https://proceedings.neurips.cc/paper_files/paper/2024/hash/f545448535dfde4f9786555403ab7c49-Abstract-Conference.html). *Advances in Neural Information Processing Systems*, 37, 136037–136083.

Daniil Gurgurov, Yusser Al Ghussin, Tanja Baeumel, Cheng-Ting Chou, Patrick Schramowski, Marius Mosbach, Josef Van Genabith, and Simon Ostermann. 2026. [CLaS-Bench: A Cross-Lingual Alignment and Steering Benchmark](https://aclanthology.org/2026.findings-acl.1086/). In *Findings of the Association for Computational Linguistics: ACL 2026*, pages 21591–21628. Association for Computational Linguistics.