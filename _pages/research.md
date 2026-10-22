---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

## Postdoctoral research: machine learning for mass-spectrometry proteomics

### PepH-GAT: hierarchical graph attention for peptide fragmentation spectra
*With Léo Schneider, Stéphane Derrode and Zied Bouyahia (paper in preparation)*

Predicting the MS/MS spectrum of a peptide is central to identifying peptides in proteomics, and it becomes much harder when residues carry **post-translational modifications (PTMs)**. Sequence-based models such as Prosit represent each residue as a token. PepH-GAT instead represents the peptide as its **molecule**:

- each peptide is built with **RDKit** from per-residue templates and converted into a **heterogeneous graph** with two node types (atoms and amino acids) and three edge types (atom–atom, atom–residue, residue–residue);
- a stack of **GATv2** layers, one per edge type, passes messages bottom-up from atoms to residues, and a **Set Transformer** readout predicts the 174 fragment-ion intensities (y/b ions, charges 1+ to 3+);
- the model is **pre-trained on ProteomeTools/Prosit** and **fine-tuned on 21 PTM types** (PRIDE PXD009449), with splits made by peptide backbone so that no sequence leaks between train and test;
- ablations compare graph structures (atoms only, residues only, full graph), encoders (sequential and cyclic) and feature standardization.

*Engineering:* PyTorch Geometric pipeline that streams millions of graphs from disk in chunks, multi-process graph generation, training and hyperparameter grid searches on an A100 GPU cluster (SLURM), experiment tracking with Weights & Biases.

### Bacterial identification from MS1 pseudo-images
Mass-spectrometry acquisitions of clinical bacterial isolates are converted into 2D **pseudo-images** (retention time × m/z). I train image classifiers on them to identify the organism:

- transfer learning with **ResNet-18/34/50 and EfficientNet-B0**, adapted to single-channel inputs;
- class imbalance handled with weighted losses and oversampling, plus domain-specific augmentations (retention-time shifts, multiplicative intensity noise) tuned by grid search;
- a **two-stage cascade** (genus model, then a species model per genus) across 11 species, evaluated by **stratified k-fold cross-validation**;
- a traceable data-curation step that maps raw acquisitions to species labels and reports every unresolved file for manual checking.

---

## PhD research: generation and evaluation of 3D human motion
*Inria Morpheo & VirtUs, 2021–2025*

### Correspondence-free online human motion retargeting (3DV 2024)
A data-driven method that transfers the motion of a source 3D human onto a target body with a different shape, **without requiring point-to-point correspondences** between the meshes, and that works online, frame by frame.
[Paper](https://arxiv.org/abs/2302.00556)

### Quality assessment of 3D human animation (IEEE TVCG 2025)
A dataset of animated virtual humans with **perceptual quality scores collected in a user study**, followed by learned objective metrics that predict how people perceive the animations, and a comparison with existing metrics.
[Paper](https://arxiv.org/abs/2505.23301)

### Survey on realistic virtual human animation (Computer Graphics Forum, Eurographics STAR 2024)
A state-of-the-art report defining what makes a virtual human animation "realistic", which features contribute to it, and how realism is evaluated, both subjectively and objectively. Presented as a 90-minute STAR session at Eurographics 2024.
[Paper](https://hal.science/hal-04553021/document)

### 4DHumanOutfit dataset (CVIU 2023)
A multi-subject 4D dataset of human motion sequences in varying outfits with large displacements, captured on the Kinovis platform.
[Project page](https://kinovis.inria.fr/4dhumanoutfit/)

---

## Earlier work: learned regularization for image restoration
*Inria Sophia Antipolis (Morpheme), 2021*

Deep learning to estimate **spatially adaptive Total Variation parameter maps** for blind image denoising, combining CNNs and variational modelling. Published at EUSIPCO 2025 with C. Fantasia, L. Calatroni and X. Descombes.
[Preprint](https://arxiv.org/abs/2503.16010)
