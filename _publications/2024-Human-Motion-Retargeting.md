---
title: "Correspondence-free online human motion retargeting"
collection: publications
date: 2024-03-18
venue: 'International Conference on 3D Vision (3DV)'
paperurl: 'https://arxiv.org/abs/2302.00556'
excerpt: "<img src='/images/retargeting-teaser.jpg' width='520'><br/>Animating any target body (scan, clothed capture, CAD character) with a source motion, without spatial or temporal correspondences, online."
citation: '<b>R. Rekik*</b>, M. Marsot*, A.-H. Olivier, J.-S. Franco, S. Wuhrer. &quot;Correspondence-free online human motion retargeting.&quot; <i>International Conference on 3D Vision (3DV)</i>, 2024. (*joint first authors)'
---

<video width="100%" controls muted loop playsinline poster="/images/retargeting-teaser.jpg">
  <source src="/files/retargeting-teaser.mp4" type="video/mp4">
</video>

**[Paper (arXiv)](https://arxiv.org/abs/2302.00556)** · **[HAL](https://hal.science/hal-03970689v2)** · **[Code](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023)** · **[Video](https://gitlab.inria.fr/rrekikdi/human-motion-retargeting2023/-/blob/main/doc/Correspondance-free_online_human_retargeting.mp4)**

## Summary
We animate a target 3D character with the motion of a source subject, in a data-driven and unsupervised way. The method needs **no spatial correspondences** between the source and target shapes and **no temporal correspondences** between frames. It can therefore work directly with raw 4D captures or consumer-device data, where meshes have no common topology. It combines a skeleton-aware motion transfer model, which preserves long-term motion context, with a geometry-aware deformation model, which preserves the surface details of the target. At inference it runs **online**, with one forward pass per frame. It reaches state-of-the-art results on two test sets, generalizes to unseen motions and body shapes, and works on multi-view captures.

## Method
<img src="/images/retargeting-pipeline.jpg" alt="Pipeline: 3D skeleton extraction, source motion retargeting model, deformation model" width="80%">

1. **3D skeleton extraction**: a PointNet regresses the articulated skeleton from the unordered points of each source frame and of the target shape.
2. **Source motion retargeting**: a recurrent model constrained by the kinematic tree (forward kinematics, adversarial motion prior) transfers the skeletal motion to the target proportions.
3. **Deformation model**: a learned skinning field maps the retargeted skeleton back to every point of the target, recovering its geometric details.

## Results
<img src="/images/retargeting-comparison.jpg" alt="Comparison with NPT and H4D" width="100%">

Compared with deformation transfer (NPT) and a motion-prior approach (H4D), our method better preserves both the source motion and the target shape.

## BibTeX
```
@inproceedings{rekik2024correspondence,
  title     = {Correspondence-free online human motion retargeting},
  author    = {Rekik, Rim and Marsot, Mathieu and Olivier, Anne-H{\'e}l{\`e}ne and Franco, Jean-S{\'e}bastien and Wuhrer, Stefanie},
  booktitle = {International Conference on 3D Vision (3DV)},
  year      = {2024}
}
```
