---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a **postdoctoral researcher in machine learning** based in Lyon, France. My work sits at the interface of **deep learning, computer vision and scientific data**: I design models that learn from structured data (3D meshes and motion sequences, molecular graphs, mass-spectrometry signals) and I care about evaluating them rigorously, including with human observers.

**Current work (postdoc).** I develop deep-learning methods for **mass-spectrometry-based proteomics**, with two main lines of work:

- **Peptide fragmentation spectrum prediction with graph neural networks.** PepH-GAT is a hierarchical Graph Attention Network that represents each peptide (including post-translational modifications) as a two-level molecular graph, with atoms and amino acids as nodes, and predicts its HCD MS/MS spectrum. It is pre-trained on ProteomeTools/Prosit and fine-tuned on 21 PTM types (paper in preparation).
- **Bacterial identification from mass-spectrometry data.** I train CNN classifiers (ResNet, EfficientNet) on MS1 pseudo-images to identify bacterial genus and species, including a two-stage genus-to-species cascade evaluated by stratified cross-validation.

**PhD (2021–2025).** I received my PhD in Computer Science from Université Grenoble Alpes / [Inria](https://www.inria.fr/en), in the [Morpheo](https://www.inria.fr/en/morpheo) (Grenoble) and [VirtUs](https://www.inria.fr/en/virtus) (Rennes) teams, supervised by Dr. [Stefanie Wuhrer](https://swuhrer.gitlabpages.inria.fr/website/) and Dr. [Anne-Hélène Olivier](https://perso.univ-rennes2.fr/anne.helene.olivier). My thesis, *Generation and evaluation of 3D human motion*, covered:

- **Human motion retargeting**: a correspondence-free online method that transfers motion between 3D human bodies ([3DV 2024](https://arxiv.org/abs/2302.00556));
- **Perceptual quality assessment of 3D human animation**: a dataset of animated virtual humans rated in a user study, and learned metrics that predict perceived quality ([IEEE TVCG 2025](https://arxiv.org/abs/2505.23301));
- **A survey on realistic virtual human animation** ([Eurographics STAR / CGF 2024](https://hal.science/hal-04553021/document));
- the **4DHumanOutfit** multi-subject 4D capture dataset ([CVIU 2023](https://kinovis.inria.fr/4dhumanoutfit/)).

**Before that.** I graduated in 2021 from the National School of Engineering of Tunis ([ENIT](http://www.enit.rnu.tn/)) with an engineering degree in Telecommunications (EUR-ACE label, data science major) and a research master's degree in vision and intelligent machines. My master's thesis at Inria Sophia Antipolis used deep learning to estimate spatially varying hyperparameters for image denoising and deblurring, which later led to a paper at EUSIPCO 2025.

I also teach: about 145 hours so far in computer vision, 3D computer graphics and animation, algorithms and data structures, Python and applied mathematics, from first-year undergraduate to engineering-school level. See [Teaching](/teaching/).

**Research interests:** geometric deep learning and graph neural networks · 3D human motion generation and evaluation · perceptual studies and quality metrics · machine learning for mass spectrometry and proteomics.
