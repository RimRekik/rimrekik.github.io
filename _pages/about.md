---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a **postdoctoral researcher in machine learning** in Lyon, France. I design **structure-aware deep-learning models for non-grid data**, such as 3D bodies in motion, molecular graphs and mass-spectrometry signals, and I **evaluate them against what really matters for the application**: human perception in computer graphics, physical measurements in biochemistry.

My PhD at [Inria](https://www.inria.fr/en) developed this approach on **3D humans**. My postdoc applies it to **molecules and health**.

<p align="center"><img src="/images/research-thread.svg" alt="Research thread: the same structure-aware, hierarchical learning approach applied to 3D humans (PhD) and to peptides (postdoc)" width="100%"></p>

### One research thread, two application domains

**1. Learning through structure, from fine elements to meaningful units.**
In my PhD, I retargeted motion between 3D humans without any mesh correspondence. A PointNet regresses an articulated skeleton from raw points. A recurrent network moves that skeleton, constrained by the kinematic tree. A learned skinning field maps the motion back to every point ([3DV 2024](https://arxiv.org/abs/2302.00556)).
In my postdoc, PepH-GAT applies the same idea to peptides. Atoms are aggregated into amino acids, which are then aggregated along the peptide chain, by a hierarchical graph attention network that predicts MS/MS fragmentation spectra, including for post-translationally modified peptides.
In both cases, the model is told what the structure is (joints and bones; atoms, residues and bonds) instead of rediscovering it from a flat sequence. This lets it generalize to **unseen body shapes** and to **unseen chemical modifications**.

**2. Evaluating against the ground truth that matters.**
For virtual humans, the reference is human perception. I built the **4DHumanPercept** dataset (240 distorted animations with mean opinion scores from a user study) and learned metrics that predict perceived quality ([IEEE TVCG 2025](https://arxiv.org/abs/2505.23301)), after a survey of how realism is defined and measured ([Eurographics STAR 2024](https://hal.science/hal-04553021/document)).
For peptides and pathogens, the reference is the instrument: spectral-angle distance to measured spectra, splits that keep peptide backbones out of the test set, and stratified cross-validation across clinical isolates.

**3. Computer vision beyond natural images.**
Mass-spectrometry acquisitions can be read as images. I train CNNs (ResNet, EfficientNet) on MS1 **pseudo-images** to identify bacterial genus and species from clinical samples, with a genus-to-species cascade. Vision methods, applied to a diagnostic problem.

### Background
- **Postdoc** (since 2025): deep learning for mass-spectrometry proteomics and clinical microbiology, Lyon.
- **PhD in Computer Science** (2021–2025), Université Grenoble Alpes / Inria, [Morpheo](https://www.inria.fr/en/morpheo) and [VirtUs](https://www.inria.fr/en/virtus) teams, supervised by [Stefanie Wuhrer](https://swuhrer.gitlabpages.inria.fr/website/) and [Anne-Hélène Olivier](https://perso.univ-rennes2.fr/anne.helene.olivier): *Generation and evaluation of 3D human motion*.
- **Engineering degree** (Telecommunications, data science) and **research master's** (vision and intelligent machines), [ENIT](http://www.enit.rnu.tn/), Tunis. Master's research at Inria Sophia Antipolis on learned regularization for image denoising, published at EUSIPCO 2025.
- **Teaching:** about 145 hours in computer vision, 3D graphics and animation, algorithms, Python and applied mathematics. See [Teaching](/teaching/).

**Research interests:** geometric deep learning and graph neural networks · 3D human motion and virtual humans · perceptual evaluation and quality metrics · machine learning for mass spectrometry, proteomics and molecular data · AI for health.

I am open to research positions in **computer vision, computer graphics, and bioinformatics / computational chemistry**, the areas where these approaches meet.
