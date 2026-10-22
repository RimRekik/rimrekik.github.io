---
title: "Quality assessment of 3D human animation: Subjective and objective evaluation"
collection: publications
date: 2025-05-29
venue: 'IEEE Transactions on Visualization and Computer Graphics (TVCG) · Q1 · Impact factor 6.8'
paperurl: 'https://doi.org/10.1109/TVCG.2025.3631385'
excerpt: "<img src='/images/4dhumanqa-teaser.jpg' width='520'><br/>A perceptual dataset of animated 4D humans and a learned quality metric that reaches 90% correlation with human judgements."
citation: '<b>R. Rekik</b>, S. Wuhrer, L. Hoyet, K. Zibrek, A.-H. Olivier. &quot;Quality assessment of 3D human animation: Subjective and objective evaluation.&quot; <i>IEEE Transactions on Visualization and Computer Graphics</i>, 2025.'
---

<img src="/images/4dhumanqa-teaser.jpg" alt="4DHumanQA overview: perceptual evaluation, analysis, training and inference" width="100%">

**[Paper (IEEE)](https://doi.org/10.1109/TVCG.2025.3631385)** · **[arXiv](https://arxiv.org/abs/2505.23301)** · **[HAL](https://inria.hal.science/hal-05116550)** · **[Code and dataset](https://gitlab.inria.fr/rrekikdi/4dhumanqa)** · **[Supplementary video](https://gitlab.inria.fr/rrekikdi/4dhumanqa/-/blob/main/supplementary_material.mp4)**

## Summary
Virtual human animations are used widely in virtual and augmented reality. Automatic methods can now generate them, but **assessing their quality remains difficult**. Existing learned metrics only apply to animations produced with parametric body models. We propose the first quality-assessment measure for animated virtual humans that are **not** generated with a parametric model, based on a data-driven framework:

1. we generate a dataset of virtual human animations and collect **subjective realism scores in a user study**;
2. we use this dataset to **learn to predict perceptual scores**.

A linear regressor trained on our dataset reaches a **correlation of 90%** with human judgements and outperforms a state-of-the-art deep-learning baseline.

## The 4DHumanPercept dataset
<video width="100%" controls muted loop playsinline poster="/images/4dhumanpercept-distortions.jpg">
  <source src="/files/4dhumanpercept-example.mp4" type="video/mp4">
</video>
*One stimulus: an acquired 4D human (blue) and five strengths of the "gliding" distortion.*

- **240 stimuli** built from real 4D reconstructions (4DHumanOutfit): several subjects, two outfits, two motions (walking, hopscotch);
- **six physically motivated distortions**: foot-skate gliding, moonwalking, foot contact, motion smoothness, temporal twist, self-intersection;
- **five strength levels** per distortion, rated against the reference animation, with **mean opinion scores** released with the data (CC BY-NC-SA 4.0).

## BibTeX
```
@article{rekik2025quality,
  title   = {Quality assessment of 3D human animation: Subjective and objective evaluation},
  author  = {Rekik, Rim and Wuhrer, Stefanie and Hoyet, Ludovic and Zibrek, Katja and Olivier, Anne-H{\'e}l{\`e}ne},
  journal = {IEEE Transactions on Visualization and Computer Graphics},
  year    = {2025},
  doi     = {10.1109/TVCG.2025.3631385}
}
```
