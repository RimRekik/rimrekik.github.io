---
title: "Hybrid learning and variational modelling for blind image denoising"
collection: publications
date: 2025-09-08
venue: 'European Signal Processing Conference (EUSIPCO), the flagship conference of EURASIP'
paperurl: 'https://arxiv.org/abs/2503.16010'
excerpt: "<img src='/images/eusipco-fig2.jpg' width='420'><br/>A network that learns pixel-wise Total Variation parameter maps for denoising when the noise type is unknown."
citation: 'C. Fantasia, L. Calatroni, X. Descombes, <b>R. Rekik</b>. &quot;Hybrid learning and variational modelling for blind image denoising.&quot; <i>European Signal Processing Conference (EUSIPCO)</i>, 2025.'
---

<img src="/images/eusipco-fig2.jpg" alt="Pipeline: noise classifier, Gaussian or Poisson parameter network, pixel-wise regularisation map" width="80%">

*Fig. 2: a noise classifier first identifies the noise type in the input image; the corresponding network then estimates a pixel-wise regularisation map in a sliding-window fashion.*

**[Preprint (arXiv)](https://arxiv.org/abs/2503.16010)** · **[Earlier version (HAL)](https://hal.science/hal-03596605)**

## Summary
Variational denoising with weighted **Total Variation (TV)** works well, but only if its regularization parameter is chosen correctly. The best choice varies across the image and depends on the noise. We propose a hybrid approach that keeps the variational model and **learns spatially adaptive TV parameter maps** with a neural network, for **blind** denoising where the noise model is unknown:

1. a binary classifier first identifies the noise model (Gaussian or Poisson);
2. a network then predicts, pixel by pixel in a sliding-window fashion, the best balance between TV regularization and data fidelity. It is trained on natural image patches to maximize SSIM.

On both noise models, the learned maps clearly improve over the best single scalar parameter.

This work continues my master's research at Inria Sophia Antipolis (Morpheme team).

## BibTeX
```
@inproceedings{fantasia2025hybrid,
  title     = {Hybrid learning and variational modelling for blind image denoising},
  author    = {Fantasia, Claudio and Calatroni, Luca and Descombes, Xavier and Rekik, Rim},
  booktitle = {European Signal Processing Conference (EUSIPCO)},
  year      = {2025}
}
```
