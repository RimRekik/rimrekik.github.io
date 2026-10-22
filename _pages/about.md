---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a **postdoctoral researcher in machine learning** in Lyon, France. I design **structure-aware deep-learning models for non-grid data** (3D bodies in motion, molecular graphs, mass-spectrometry signals) and I evaluate them against what matters for the application: human perception in computer graphics, physical measurements in biochemistry.

### Research

**Structure-aware, hierarchical learning.**
I develop models that reason from fine elements up to meaningful units. During my PhD at [Inria](https://www.inria.fr/en), I designed a correspondence-free method that retargets motion between 3D humans of any shape. It regresses an articulated skeleton from raw points, moves it under kinematic constraints and transfers the motion back through a learned skinning field ([3DV 2024](https://arxiv.org/abs/2302.00556)). I now develop **PepH-GAT**, a hierarchical graph attention network that goes from atoms to amino acids to predict peptide MS/MS fragmentation spectra, including for post-translationally modified peptides.

**Evaluation grounded in perception and measurement.**
I built **4DHumanPercept**, a dataset of 240 animated 4D humans rated in a user study, and learned metrics that predict perceived animation quality ([IEEE TVCG 2025](https://arxiv.org/abs/2505.23301)). I also co-authored a survey on realistic virtual human animation ([Eurographics STAR 2024](https://hal.science/hal-04553021/document)). In proteomics, I evaluate models against measured spectra, with leakage-free splits and cross-validation across clinical isolates.

**Computer vision for health.**
I train CNNs on mass-spectrometry pseudo-images to identify bacterial genus and species from clinical samples.

### Background
- **Postdoc** (since 2025): deep learning for mass-spectrometry proteomics and clinical microbiology, Lyon.
- **PhD in Computer Science** (2021–2025), Université Grenoble Alpes / Inria, [Morpheo](https://www.inria.fr/en/morpheo) and [VirtUs](https://www.inria.fr/en/virtus) teams, supervised by [Stefanie Wuhrer](https://swuhrer.gitlabpages.inria.fr/website/) and [Anne-Hélène Olivier](https://perso.univ-rennes2.fr/anne.helene.olivier): *Generation and evaluation of 3D human motion*.
- **Engineering degree** (Telecommunications, data science) and **research master's** (vision and intelligent machines), [ENIT](http://www.enit.rnu.tn/), Tunis. Master's research at Inria Sophia Antipolis on learned regularization for image denoising, published at EUSIPCO 2025.
- **Teaching:** about 145 hours in computer vision, 3D graphics and animation, algorithms, Python and applied mathematics. See [Teaching](/teaching/).

**Research interests:** geometric deep learning and graph neural networks · 3D human motion and virtual humans · perceptual evaluation and quality metrics · machine learning for mass spectrometry and molecular data · AI for health.
