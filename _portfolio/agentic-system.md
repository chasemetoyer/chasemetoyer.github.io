---
title: "Agentic World Modeling System"
date: 2023-08-20
collection: portfolio
category: flagship
tags:
  - Agents
  - World models
  - Evaluation
thesis: "A generative world model used to train agents in simulation, transferring zero-shot to complex environments."
key_result: "Zero-shot transfer success rate of X%."
header:
  teaser: "/images/agentic-system-teaser.png"
external_links:
  - label: "GitHub"
    url: "https://github.com/chasemetoyer"
    icon: "fab fa-github"
  - label: "Paper"
    url: "#"
    icon: "fas fa-file-pdf"
---

## Abstract

Training agents in the real world is expensive and dangerous. This project builds a high-fidelity generative world model that acts as a simulator, allowing agents to learn policies that transfer to the real environment.

## Method

* **Generative Simulator**: Diffusion-based next-state prediction.
* **Policy Learning**: RL agent trained inside the hallucinations of the world model.
