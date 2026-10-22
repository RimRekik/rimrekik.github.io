---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

My research follows one line: **deep learning that respects the structure of the data, evaluated against the ground truth that matters for the application.** I developed it on 3D virtual humans during my PhD (computer vision and graphics), and I now apply it to peptides and pathogens (bioinformatics and AI for health).

<p align="center"><img src="/images/research-thread.svg" alt="Research thread diagram" width="100%"></p>

---

## Axis 1: Structure-aware, hierarchical learning on non-grid data

### Correspondence-free online human motion retargeting (3DV 2024)
*R. Rekik, M. Marsot, A.-H. Olivier, J.-S. Franco, S. Wuhrer*

<img src="/images/retargeting-teaser.jpg" alt="Motion retargeted from a source onto a CAD character, a clothed scan and a naked body" width="100%">

The task is to transfer the motion of a source human onto a target body of any shape, such as a CAD character or a clothed or naked scan, **without point-to-point correspondences** and online, frame by frame. The method goes from the fine level to the structural level and back:
- a **PointNet** regresses the articulated skeleton from raw, unordered points;
- a **recurrent network constrained by the kinematic tree** (forward kinematics, adversarial prior) retargets the skeletal motion;
- a learned **skinning field** transfers the motion back to every point of the target.

Trained on AMASS motion capture.
[Paper](https://arxiv.org/abs/2302.00556) · [HAL](https://hal.science/hal-03970689v2) · [Code](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023)

### PepH-GAT: hierarchical graph attention for peptide fragmentation spectra (in preparation)
*R. Rekik, L. Schneider, S. Derrode, Z. Bouyahia*

The same principle moves from bodies to molecules. Predicting a peptide's MS/MS spectrum is central to peptide identification in proteomics. It is especially hard for **post-translational modifications (PTMs)**, which sequence-token models such as Prosit only see as new, rare tokens. PepH-GAT works on the molecule itself:
- each peptide, including its PTMs, is built with **RDKit** and encoded as a **heterogeneous graph** with atoms and amino acids as nodes and atom–atom, atom–residue and residue–residue edges. The two levels play the same role as points and joints in the retargeting work;
- **GATv2** message passing, one block per edge type, goes bottom-up from atoms to residues, and a **Set Transformer** readout predicts the 174 fragment-ion intensities;
- the model is **pre-trained on ProteomeTools/Prosit** and **fine-tuned on 21 PTM types**, with ablations over graph structure (atoms only, residues only, full graph) and encoder design.

*Engineering:* PyTorch Geometric pipeline streaming millions of graphs, multi-process graph construction, A100 cluster training (SLURM), Weights & Biases tracking.

---

## Axis 2: Evaluation grounded in perception and measurement

### Quality assessment of 3D human animation (IEEE TVCG 2025)
*R. Rekik, S. Wuhrer, L. Hoyet, K. Zibrek, A.-H. Olivier*

<img src="/images/4dhumanqa-teaser.jpg" alt="4DHumanQA pipeline: perceptual study, analysis, training and inference of a perceptual score" width="100%">

Standard geometric errors say little about whether an animation *looks* wrong. I built **4DHumanPercept**, a set of 240 animated sequences of real 4D-captured humans (from 4DHumanOutfit). Each sequence is degraded with six controlled, physically motivated distortions (foot sliding, moonwalking, foot contact, over-smoothing, temporal twist, self-intersection) at five strength levels and rated by participants in a user study (mean opinion scores). On this data I trained **4DHumanQA**, a learned metric that predicts perceived quality, and compared it with existing metrics.
[Paper](https://arxiv.org/abs/2505.23301) · [HAL](https://inria.hal.science/hal-05116550) · [Code and dataset](https://gitlab.inria.fr/rrekikdi/4dhumanqa)

### A survey on realistic virtual human animations (CGF, Eurographics STAR 2024)
What does "realistic" mean for a virtual human, which features drive it, and how should it be measured, subjectively and objectively? A 90-minute State-of-the-Art Report at Eurographics 2024.
[Paper](https://hal.science/hal-04553021/document)

### The same rigour in biochemistry
In my postdoc, the reference is the mass spectrometer instead of the observer. Models are scored by the **spectral-angle distance** to measured spectra, with impossible fragments masked. PTM data are split **by peptide backbone**, so no sequence leaks between train and test, and every PTM type must appear in each split. Every discarded spectrum is logged with a reason.

---

## Axis 3: Computer vision for health and science

### Bacterial identification from mass-spectrometry pseudo-images
LC-MS acquisitions of clinical bacterial isolates are rendered as 2D **pseudo-images** (retention time × m/z), which turns a diagnostic question into a vision problem:
- transfer learning with **ResNet-18/34/50 and EfficientNet-B0** adapted to single-channel intensity maps;
- class imbalance handled by weighted losses and oversampling, and domain-specific augmentations (retention-time shifts, multiplicative intensity noise) selected by grid search;
- a **genus → species cascade** over 11 species, evaluated by stratified k-fold cross-validation;
- traceable curation from raw acquisitions to labels, with every ambiguous sample reported for expert review.

### 4DHumanOutfit (CVIU 2023)
A multi-subject 4D capture dataset of people in varying outfits with large displacements, captured on the Kinovis platform. It provides the reference reconstructions used in 4DHumanPercept.
[Project page](https://kinovis.inria.fr/4dhumanoutfit/)

### Learned regularization for blind image denoising (EUSIPCO 2025)
CNNs predict spatially adaptive Total Variation parameter maps, combining learning with variational modelling. This started as my master's research at Inria Sophia Antipolis, and I later co-supervised an M2 student on it.
[Preprint](https://arxiv.org/abs/2503.16010)

---

## Where this is going
I want to keep building models that **encode the known structure of a problem** (anatomy, chemistry, physics) and that are **validated against human or experimental ground truth**. Natural next steps include 3D and graph representations for molecular and biomedical data, perceptually and clinically grounded evaluation metrics, and generative models for structured data, from human motion to molecules.
