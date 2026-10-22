---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

I develop deep-learning models that respect the structure of the data, and I evaluate them against perceptual or experimental ground truth. My work spans 3D virtual humans (computer vision and graphics) and peptides and pathogens (bioinformatics and AI for health).

---

## Axis 1: Structure-aware, hierarchical learning on non-grid data

### Correspondence-free online human motion retargeting (3DV 2024)
*R. Rekik\*, M. Marsot\*, A.-H. Olivier, J.-S. Franco, S. Wuhrer (\*joint first authors)*

The task is to transfer the motion of a source human onto a target body of any shape, such as a CAD character or a clothed or naked scan, **without point-to-point correspondences** and online, frame by frame. The method goes from the fine level to the structural level and back:
- a **PointNet** regresses the articulated skeleton from raw, unordered points;
- a **recurrent network constrained by the kinematic tree** (forward kinematics, adversarial prior) retargets the skeletal motion;
- a learned **skinning field** transfers the motion back to every point of the target.

Trained on AMASS motion capture.
**[→ Paper page](/publications/2024-Human-Motion-Retargeting/)** · [arXiv](https://arxiv.org/abs/2302.00556) · [HAL](https://hal.science/hal-03970689v2) · [Code](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023)

### Graph neural networks for peptide mass spectrometry (ongoing)
Predicting how peptides behave in a mass spectrometer is central to protein identification in proteomics, and it is especially hard for chemically modified peptides. I develop **hierarchical graph neural networks** that represent peptides at the molecular level, so that the model can handle chemical modifications it has rarely seen. A paper is in preparation.

<img src="/images/peptide-graph-abstract.png" alt="From peptide sequence to molecular structure, hierarchical atom–residue graph and predicted spectrum" width="100%">

---

## Axis 2: Evaluation grounded in perception and measurement

### Quality assessment of 3D human animation (IEEE TVCG 2025)
*R. Rekik, S. Wuhrer, L. Hoyet, K. Zibrek, A.-H. Olivier*

Standard geometric errors say little about whether an animation *looks* wrong. I built **4DHumanPercept**, a set of 240 animated sequences of real 4D-captured humans (from 4DHumanOutfit). Each sequence is degraded with six controlled, physically motivated distortions (foot sliding, moonwalking, foot contact, over-smoothing, temporal twist, self-intersection) at five strength levels and rated by participants in a user study (mean opinion scores). On this data I trained **4DHumanQA**, a learned metric that predicts perceived quality, and compared it with existing metrics.
**[→ Paper page](/publications/2025-QualityAssessment-TVCG/)** · [arXiv](https://arxiv.org/abs/2505.23301) · [HAL](https://inria.hal.science/hal-05116550) · [Code and dataset](https://gitlab.inria.fr/rrekikdi/4dhumanqa)

### A survey on realistic virtual human animations (CGF, Eurographics STAR 2024)
What does "realistic" mean for a virtual human, which features drive it, and how should it be measured, subjectively and objectively? A 90-minute State-of-the-Art Report at Eurographics 2024.
**[→ Paper page](/publications/2024-StarVH/)** · [PDF](https://hal.science/hal-04553021/document)

### Evaluation in proteomics
In my postdoc, models are evaluated against experimental measurements, with data splits designed to prevent information leakage between training and test sets.

---

## Axis 3: Computer vision for health and science

### Pathogen identification from mass-spectrometry data (ongoing)
Mass-spectrometry acquisitions of clinical samples can be represented as images. I apply **computer-vision models** to them to identify bacteria, an application of vision methods to clinical microbiology.

### 4DHumanOutfit (CVIU 2023)
A multi-subject 4D capture dataset of people in varying outfits with large displacements, captured on the Kinovis platform. It provides the reference reconstructions used in 4DHumanPercept.
**[→ Paper page](/publications/2023-4DHumanOutfit/)** · [Dataset](https://kinovis.inria.fr/4dhumanoutfit/)

### Learned regularization for blind image denoising (EUSIPCO 2025)
CNNs predict spatially adaptive Total Variation parameter maps, combining learning with variational modelling. This started as my master's research at Inria Sophia Antipolis, and I later co-supervised an M2 student on it.
**[→ Paper page](/publications/2025-BlindDenoising-EUSIPCO/)** · [arXiv](https://arxiv.org/abs/2503.16010)

---

## Where this is going
I want to keep building models that **encode the known structure of a problem** (anatomy, chemistry, physics) and that are **validated against human or experimental ground truth**. Natural next steps include 3D and graph representations for molecular and biomedical data, perceptually and clinically grounded evaluation metrics, and generative models for structured data, from human motion to molecules.
