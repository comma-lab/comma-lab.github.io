---
layout: page
title: Controllable Music Generation Using Deep Learning
description: PhD research Jincheng Zhang 2021–2025
img: /assets/img/projects/pianorollvisualization.png
order: 5
redirect: false
display: true
---

Computers can write music, even before neural networks and deep learning techniques, but a system that produces random tunes is of limited use to musicians, filmmakers, or content creators. What they need is the ability to steer it: "write something in the style of Chopin", "follow these chords", "make it sound sad", "fit this video clip". This project explored how to provide that kind of control across four studies.

**Borrowing from computer vision**

The work builds on AI image generation and other computer vision tasks with diffusion models. These are a class of probabilistic generative AI algorithms that create new data by gradually "diffusing" training data with random noise and then learning to reverse that diffusion process. Diffusion models work well for image, video, or audio synthesis, but their potential for symbolic music generation (e.g., in [MIDI](https://en.wikipedia.org/wiki/MIDI) format), which is made of discrete notes rather than continuous signal values, remains underexplored.

The key idea across these studies was to turn music into a picture, specifically a [piano roll](https://musiclab.chromeexperiments.com/Piano-Roll/), named after the punched paper rolls of old player pianos, where each note is drawn as a horizontal bar. 

**Four kinds of control**

[Zhang, Fazekas, and Saitis (2024)](https://arxiv.org/pdf/2310.14044) combined a vector quantized variational autoencoder (VQ-VAE) with discrete diffusion to train a model to generate music in the style of Liszt, Chopin, or Schubert, based on the MAESTRO dataset. The VQ-VAE compressed music into a short sequence of "building blocks" drawn from a learned musical vocabulary, with diffusion used to arrange those blocks (to model the VQ-VAE's discrete latent space). A composer classifier demonstrated a high accuracy of 72.36% compared to the MusicTransformer and VQ-Transformer models. In a listening test with 30 participants, the music was rated the richest and most varied of the AI models compared.

[Zhang, Fazekas, and Saitis (2025)](https://ieeexplore.ieee.org/document/11228274) introduced a novel diffusion model that incorporated a Transformer-Mamba block (to handle long sequences efficiently) and learnable wavelet transform (good at picking out sharp details such as where notes begin and end). The proposed model outperformed existing state-of-the-art methods for pianoroll generation in terms of music quality and controllability, both in terms of objective metrics and listener ratings.

The third study (preprint) explored generating music in one of four moods (happy, tense, sad or calm), defined by valence (how positive) and arousal (how energetic). Diffusion models are usually slow because each clean-up step must be small, so they need hundreds or thousands of steps. Here a GAN (Generative Adversarial Network) was used for the denoising instead, which allowed much larger steps: the model produced convincing music in just 15 steps, compared with 250 for a standard diffusion baseline. An emotion classifier judged 63.5% of the outputs to match their target, which is close to the network's own 65.4% accuracy on real music.

The fourth study (unpublished) investigated diffusion for video background music generation. The proposed approach innovated by using self-representation alignment, a form of self-teaching. The model's early, rougher processing stages are nudged to resemble the later, more refined stages of a slowly updated copy of itself. Compared with Diff-BGM, the leading system at the time, the music matched its video more often in a retrieval test. Its tonal and rhythmic statistics were also practically identical to those of human-written music, and listeners rated its rhythm 74 out of 100, against 54 for Diff-BGM.

