---
title: "Visual Internal Reasoning"
date: 2025-12-29
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
    url: "https://github.com/chasemetoyer/visual-internal-reasoning"
    icon: "fab fa-github"
---

# Visual Internal Reasoning: Causal Dependency on Latent Image Tokens

## **Abstract**

Large language models (LLMs) exhibit strong performance on linguistic reasoning tasks but continue to struggle with problems requiring spatial and visual reasoning, often relying on shallow textual heuristics rather than grounded internal representations. In this work, we investigate whether equipping a transformer-based language model with an explicit internal visual latent representation improves performance on visually grounded reasoning tasks.

We propose a unified decoder-only architecture in which discrete image tokens, obtained from a pretrained vector-quantized autoencoder (VQGAN), are incorporated directly into the model’s vocabulary alongside standard text tokens. The model is trained autoregressively to generate an intermediate sequence of image tokens—interpreted as an internal “imagined” visual state—prior to producing a textual answer.

Our results demonstrate that models trained with forced internal visual intermediates outperform text-only baselines on spatial reasoning tasks and exhibit significant performance degradation when the imagined visual tokens are disrupted (Blindfold Accuracy: 57.0% vs. Imagined Accuracy: 90.5%), indicating that the visual representation is causally utilized.

---

## **Key Findings (N=200)**

We evaluated the model on a "Forced Choice" spatial reasoning task (*"Does the Red Square overlap the Blue Circle?"*). The results demonstrate a clear causal dependency on the internal visual state.

| Condition | Description | Accuracy | Interpretation |
| --- | --- | --- | --- |
| **Teacher Forced** | Ground truth visual tokens provided. | **100.0%** | **Upper Bound:** The model can perfectly interpret clear visual data. |
| **Imagined (Greedy)** | Model generates its own visual latents. | **90.5%** | **Method:** Internal simulation provides a +33.5% gain over baseline. |
| **Text-Only** | Visual tokens omitted entirely. | 59.0% | **Baseline:** Text priors alone are insufficient for this task. |
| **Blindfold** | Visual tokens replaced with VQ-noise. | 57.0% | **Control:** Performance collapses to random chance (57% majority class) without visual structure. |

> **Verdict:** The degradation from **90.5%** (Imagined) to **57.0%** (Blindfold) rejects the null hypothesis that the model relies solely on text shortcuts.
<img width="700" height="700" alt="BarGraph" src="https://github.com/user-attachments/assets/0f88db07-0829-4556-9808-f5a8a8692f43" />
