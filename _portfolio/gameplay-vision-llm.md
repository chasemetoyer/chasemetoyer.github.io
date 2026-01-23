---
title: "Gameplay Vision LLM / Long-horizon Video Understanding"
date: 2023-11-15
collection: portfolio
category: flagship
tags:
  - Long-horizon video
  - Agents
  - World models
thesis: "End-to-end video understanding model capable of long-horizon planning and gameplay analysis using temporal latent compression."
key_result: "State-of-the-art performance on relevant benchmarks (insert metric)."
header:
  teaser: "/images/gameplay-vision-teaser.png"
external_links:
  - label: "GitHub"
    url: "https://github.com/chasemetoyer"
    icon: "fab fa-github"
  - label: "Demo"
    url: "#"
    icon: "fas fa-play-circle"
---

## Abstract

Understanding gameplay requires tracking state over long horizons—something standard video transformers struggle with due to attention costs. This system uses temporal compression to maintain a "world state" over thousands of frames.

## Method

* **Temporal Compression**: Hierarchical token merging reducing context length.
* **Agentic Evaluation**: Tested on ability to predict future states in complex game environments.
