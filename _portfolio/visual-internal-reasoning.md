---
title: "Visual Internal Reasoning"
date: 2024-01-01
collection: portfolio
category: flagship
tags:
  - Multimodal
  - Mechanistic eval
  - Latent tokens
  - Causal intervention
thesis: "Decoder-only transformer that generates discrete VQGAN visual latents as an internal scratchpad; blindfold intervention shows visual state is causally necessary for spatial reasoning."
key_result: "90.5% → 57% under blindfold (collapse to text-only baseline)"
header:
  teaser: "/images/visual-reasoning-teaser.png" 
external_links:
  - label: "GitHub"
    url: "https://github.com/chasemetoyer"
    icon: "fab fa-github"
  - label: "Blog"
    url: "#"
    icon: "fas fa-rss"
  - label: "PDF"
    url: "#"
    icon: "fas fa-file-pdf"
  - label: "Demo"
    url: "#"
    icon: "fas fa-play-circle"
---

## Abstract

Standard multimodal models reason by aligning text and image representations, but they often lack an internal "visual scratchpad" to plan or simulate spatial transformations. This project explores a decoder-only architecture that can generate discrete VQGAN visual latents as intermediate reasoning steps.

## Motivation

How do we ensure that a model is actually "seeing" and reasoning spatially, rather than just matching statistical patterns in text? By forcing the model to generate visual latents, we can inspect its internal state.

## Method

* **Architecture**: Decoder-only transformer.
* **Intervention**: "Blindfolding" the model (suppressing visual latent generation) to see if reasoning performance drops.

## Results

The model achieves 90.5% accuracy on spatial reasoning tasks. When the visual generation pathway is blocked, performance drops to 57%, which matches the text-only baseline. This indicates the generated visual state is causally necessary.
