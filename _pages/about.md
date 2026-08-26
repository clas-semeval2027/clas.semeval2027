---

layout: about
title: home
permalink: /

subtitle:

profile:
align: left
image: # clas_logo.png
image_circular: false

selected_papers: false
social: false

announcements:
enabled: false
scrollable: true
limit: 5

latest_posts:
enabled: false
scrollable: true
limit: 3

---

We are happy to announce the **CLaS: Cross-Lingual Alignment and Steering of Large Language Models** Shared Task at *SemEval 2027*.

The CLaS shared task asks participants to control the output language of a large language model (LLM) using inference-time interventions. Given a question in a source language, participants steer the model to produce a relevant and coherent answer in a specified target language.

We encourage participants to go beyond existing steering approaches and explore how language steering can be improved. This can include making small changes to established methods, combining existing techniques, or developing entirely new approaches to language steering. We are particularly interested in methods that provide better language control while preserving the relevance and quality of the model's responses.

The task is also an opportunity to investigate how and where language information is represented inside multilingual language models, and whether steering methods generalize across languages, including low-resource languages. Participants are therefore welcome to experiment with different intervention strategies, model components, layers, and representations.

The codebase for obtaining training and validation data, running the baseline generations, and evaluating the results is available in our [GitHub repository](https://github.com/d-gurgurov/CLaS-SemEval-2027).

**More information is available on the [shared task page](https://clas-semeval2027.github.io/clas.semeval2027/).**
