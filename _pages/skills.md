---
layout: archive
title: "Technical skills"
permalink: /skills/
author_profile: true
---

{% include base_path %}

<style>
.skills-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:16px;margin:1em 0 2em}
.skill-card{border:1px solid #e3e6ea;border-radius:10px;padding:14px 16px;background:#fafbfc}
.skill-card h3{margin:0 0 10px;font-size:1em;letter-spacing:.02em}
.chip{display:inline-block;margin:0 6px 7px 0;padding:3px 10px;border-radius:999px;font-size:.78em;line-height:1.5;background:#e8f1f8;color:#1f4e79;border:1px solid #cfe0ee}
.chip.main{background:#1f4e79;color:#fff;border-color:#1f4e79;font-weight:600}
.skills-table{width:100%;border-collapse:collapse;font-size:.88em}
.skills-table td{padding:8px 10px;border-bottom:1px solid #eceff2;vertical-align:top}
.skills-table td:first-child{width:38%;font-weight:600}
.skills-note{font-size:.8em;color:#666}
</style>

<div class="skills-grid">

<div class="skill-card">
<h3>Programming</h3>
<span class="chip main">Python</span><span class="chip">C++</span><span class="chip">C</span><span class="chip">Java</span><span class="chip">SQL</span><span class="chip">MATLAB</span><span class="chip">Bash</span>
</div>

<div class="skill-card">
<h3>Deep learning</h3>
<span class="chip main">PyTorch</span><span class="chip main">PyTorch Geometric</span><span class="chip">torchvision</span><span class="chip">TensorFlow / Keras</span><span class="chip">scikit-learn</span>
</div>

<div class="skill-card">
<h3>Models</h3>
<span class="chip main">Graph neural networks (GAT)</span><span class="chip">CNNs (ResNet, EfficientNet)</span><span class="chip">PointNet</span><span class="chip">RNNs</span><span class="chip">Transformers</span><span class="chip">Adversarial training</span><span class="chip">Autoencoders</span>
</div>

<div class="skill-card">
<h3>3D vision &amp; graphics</h3>
<span class="chip main">Meshes &amp; point clouds</span><span class="chip">SMPL body models</span><span class="chip">Motion capture (AMASS)</span><span class="chip">Skinning &amp; kinematics</span><span class="chip">Trimesh</span><span class="chip">Polyscope</span><span class="chip">Blender</span><span class="chip">OpenCV</span>
</div>

<div class="skill-card">
<h3>Data analysis &amp; evaluation</h3>
<span class="chip main">Evaluation protocols</span><span class="chip">Cross-validation</span><span class="chip">Ablation studies</span><span class="chip">User studies</span><span class="chip">Statistical analysis</span><span class="chip">NumPy</span><span class="chip">pandas</span><span class="chip">Matplotlib</span><span class="chip">Seaborn</span><span class="chip">PsychoPy</span>
</div>

<div class="skill-card">
<h3>Scientific &amp; biomedical data</h3>
<span class="chip main">RDKit</span><span class="chip">Molecular graphs</span><span class="chip">Mass spectrometry</span><span class="chip">Proteomics</span><span class="chip">HDF5</span>
</div>

<div class="skill-card">
<h3>Computing &amp; MLOps</h3>
<span class="chip main">GPU clusters (SLURM, A100)</span><span class="chip">Parallel hyperparameter search</span><span class="chip">Weights &amp; Biases</span><span class="chip">Large-scale data pipelines</span><span class="chip">Git</span><span class="chip">Linux</span>
</div>

<div class="skill-card">
<h3>Languages</h3>
<span class="chip main">English (fluent)</span><span class="chip main">French (fluent)</span><span class="chip">Arabic (native)</span><span class="chip">German (basic)</span>
</div>

</div>

## Skills in action

<table class="skills-table">
<tr><td>Graph neural networks on molecular graphs</td><td>Hierarchical graph attention network predicting peptide spectra from atoms and amino acids, with RDKit and PyTorch Geometric. <a href="/publications/2026-PepH-GAT/">PepH-GAT</a></td></tr>
<tr><td>Computer vision for biomedical data</td><td>Transfer learning (ResNet, EfficientNet) for bacterial identification from mass-spectrometry data, with stratified cross-validation.</td></tr>
<tr><td>3D deep learning &amp; animation</td><td>Correspondence-free motion retargeting: PointNet skeleton extraction, kinematic-tree RNN, learned skinning. <a href="/publications/2024-Human-Motion-Retargeting/">3DV 2024</a></td></tr>
<tr><td>Perceptual evaluation</td><td>User study design, ethics, statistical analysis of subjective scores, and learned perceptual metrics. <a href="/publications/2025-QualityAssessment-TVCG/">IEEE TVCG 2025</a></td></tr>
<tr><td>Large-scale training</td><td>Multi-day GPU training and parallel hyperparameter searches on A100 clusters, with streamed datasets of millions of samples.</td></tr>
<tr><td>Open, reproducible research</td><td>Released and documented code and datasets. <a href="https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023">Retargeting code</a> · <a href="https://gitlab.inria.fr/rrekikdi/4dhumanqa">4DHumanQA &amp; dataset</a></td></tr>
</table>

<p class="skills-note">Dark tags mark the tools I use most.</p>
