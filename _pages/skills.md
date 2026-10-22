---
layout: archive
title: "Technical skills"
permalink: /skills/
author_profile: true
---

{% include base_path %}

These are the skills I use in my research code: in the public repositories of my PhD ([motion retargeting](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023), [4DHumanQA](https://gitlab.inria.fr/rrekikdi/4dhumanqa)) and in my postdoc projects.

## Deep learning
- **Frameworks:** PyTorch (main framework), PyTorch Geometric, torchvision; TensorFlow/Keras.
- **Architectures I have implemented and trained:**
  - graph neural networks: graph attention (GATv2) on heterogeneous, hierarchical graphs, with attention-based pooling (Set Transformer);
  - point-cloud networks (PointNet);
  - recurrent networks for motion sequences, with adversarial training;
  - CNNs (ResNet, EfficientNet, AlexNet-style networks) for classification and regression.
- **Training methodology:** transfer learning and fine-tuning, class-imbalance handling (weighted losses, oversampling), data augmentation designed for the domain, learning-rate scheduling, early stopping, checkpointing, hyperparameter grid searches.

## Data analysis and evaluation
- **Data pipelines:** cleaning, curation and labelling of large heterogeneous datasets with full traceability; streaming datasets too large for memory (HDF5, chunked storage); multi-process preprocessing.
- **Evaluation:** task-specific metrics, ablation studies, stratified k-fold cross-validation, train/test splits that prevent information leakage, error analysis.
- **Perceptual studies:** design of user studies, ethics documentation, collection and statistical analysis of subjective scores (mean opinion scores), learning perceptual metrics from them.
- **Libraries:** NumPy, pandas, scikit-learn, Matplotlib, Seaborn.

## 3D vision and computer graphics
- 3D meshes and point clouds (Trimesh, Polyscope), parametric body models (SMPL, SMPL-H/SMPL-X), motion-capture data (AMASS).
- Skeletal animation: forward kinematics, linear blend skinning, motion retargeting, mesh reposing.
- Controlled generation of animation artefacts for perceptual studies; rendering with Blender.

## Scientific and biomedical data
- Molecular modelling with RDKit: building molecules and converting them into graphs with atom, bond and residue features.
- Mass-spectrometry and proteomics data: spectra, peptide sequences, chemical modifications.

## Software engineering and computing
- **Languages:** Python (expert), C++, C, Java, SQL, MATLAB.
- **Large-scale GPU computing:** training on remote high-performance computing clusters (SLURM, NVIDIA A100):
  - job orchestration and parallel hyperparameter searches run as batches of jobs;
  - multi-day training runs with checkpointing;
  - environment and dependency management on remote Linux servers;
  - offline experiment tracking and syncing (Weights & Biases).

  These skills transfer directly to cloud environments.
- **Reproducibility:** command-line configuration, fixed seeds, saved run options, experiment tracking with Weights & Biases, documented open-source releases (README, licences, BibTeX).
- **Tools:** Git (GitHub, GitLab), Linux, Bash.
