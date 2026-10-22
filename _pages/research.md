---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

I develop **deep-learning methods to model and analyse complex data** (molecular graphs and mass-spectrometry signals, 3D shapes and human motion, images) across biomedical, computer vision and computer graphics applications.

**How I evaluate.** Every project is evaluated with protocols that fit the application:
- **quantitative**: task-specific metrics, ablation studies, cross-validation and data splits that prevent information leakage;
- **qualitative**: visual inspection and error analysis;
- **perceptual**: user studies that measure how people perceive the results (ethics procedures, statistical analysis of subjective scores).

---

## 1. Biomedical data: proteomics and clinical microbiology
*Postdoc, [Imagine team](https://liris.cnrs.fr/equipe/imagine), LIRIS, École Centrale de Lyon, since 2025*

### Graph neural networks for peptide mass spectrometry (ongoing)
Predicting how peptides behave in a mass spectrometer is central to protein identification in proteomics, and it is especially hard for chemically modified peptides. I develop **hierarchical graph neural networks** that represent peptides at the molecular level, from atoms to amino acids, so that the model can handle modifications it has rarely seen. Models are evaluated against experimental spectra. A paper is in preparation.

<img src="/images/peptide-graph-abstract.png" alt="From peptide sequence to molecular structure, hierarchical atom–residue graph and predicted spectrum" width="100%">

### Bacterial identification from mass-spectrometry data (ongoing)
Mass-spectrometry acquisitions of clinical samples can be represented as images. I apply **computer-vision models** to them to identify bacteria, and evaluate them with cross-validation across clinical isolates.

---

## 2. 3D humans: 4D vision, animation and perception
*PhD, Inria [Morpheo](https://www.inria.fr/en/morpheo) (now Kinetix) and [VirtUs](https://team.inria.fr/virtus/) teams, 2021–2025*

### Correspondence-free online human motion retargeting (3DV 2024)
*R. Rekik\*, M. Marsot\*, A.-H. Olivier, J.-S. Franco, S. Wuhrer (\*joint first authors)*

This method transfers the motion of a source human onto a target body of any shape (CAD character, clothed or naked scan) **without spatial or temporal correspondences**, online, frame by frame. A PointNet extracts the 3D skeleton from raw points, a kinematic-tree-aware recurrent model retargets the motion, and a learned deformation model restores the surface details of the target. It is evaluated with quantitative metrics on two test sets and with a user study.
**[→ Paper page](/publications/2024-Human-Motion-Retargeting/)** · [arXiv](https://arxiv.org/abs/2302.00556) · [HAL](https://hal.science/hal-03970689v2) · [Code](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023)

### 4DHumanOutfit dataset (CVIU 2023)
A multi-subject 4D capture dataset of people in varying outfits with large displacements, captured on the Kinovis platform and organized along three axes: identity, outfit and motion.
**[→ Paper page](/publications/2023-4DHumanOutfit/)** · [Dataset](https://kinovis.inria.fr/4dhumanoutfit/)

### Quality assessment of 3D human animation (IEEE TVCG 2025)
*R. Rekik, S. Wuhrer, L. Hoyet, K. Zibrek, A.-H. Olivier*

Standard geometric errors say little about whether an animation *looks* wrong. I built **4DHumanPercept**, 240 animations of real 4D-captured humans degraded with six controlled distortions at five strength levels and rated in a user study. I then learned **4DHumanQA**, a metric that predicts perceived quality with 90% correlation to human judgements.
**[→ Paper page](/publications/2025-QualityAssessment-TVCG/)** · [arXiv](https://arxiv.org/abs/2505.23301) · [HAL](https://inria.hal.science/hal-05116550) · [Code and dataset](https://gitlab.inria.fr/rrekikdi/4dhumanqa)

### A survey on realistic virtual human animations (CGF, Eurographics STAR 2024)
What does "realistic" mean for a virtual human, which features drive it, and how should it be measured, subjectively and objectively? Presented as a 90-minute State-of-the-Art Report at Eurographics 2024.
**[→ Paper page](/publications/2024-StarVH/)** · [PDF](https://hal.science/hal-04553021/document)

---

## 3. Images: inverse problems

### Learned regularisation for blind image denoising (EUSIPCO 2025)
A noise classifier identifies the noise type, then a network predicts spatially adaptive Total Variation parameter maps, combining learning with variational modelling. This started as my master's research at Inria Sophia Antipolis, and I later co-supervised an M2 student on it.
**[→ Paper page](/publications/2025-BlindDenoising-EUSIPCO/)** · [arXiv](https://arxiv.org/abs/2503.16010)

---

## Perspectives
I want to keep developing deep-learning methods for complex, structured data where **evaluation is as carefully designed as the model**. This includes 3D and graph representations for biomedical data, computer vision for health, the generation and analysis of human motion from 4D capture, and evaluation metrics grounded in human perception or experimental measurement.
