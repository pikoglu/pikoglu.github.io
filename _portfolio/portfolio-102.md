---
title: "EchoCem: Cement quality assessment through ultrasonic image segmentation"
excerpt: "<img src='/images/portfolio/echocem.png'>"
collection: portfolio
category: Research Projects
---

* __With__: [Félix FOURREAU](github.com/pikoglu)
* __Ressources__: [Report](/files/portfolio/echocem_report.pdf) / [slides](/files/portfolio/echocem_slides.pdf) / [Code](https://github.com/mathis-wauquiez/EchoCemDataChallenge)
* __When__: 2025
* __Associated to__: [MVA](https://www.master-mva.com/)
* __Category__: Research, Signal Processing, Computer Vision
<image src='/images/portfolio/echocem.png' width="100%" />


Project description
==============
This was a group project associated to [Stéphane Mallat](https://www.di.ens.fr/~mallat/mallat.html)'s course "[Génération de données par transport et débruitage](https://www.college-de-france.fr/fr/agenda/cours/generation-de-donnees-en-ia-par-transport-et-debruitage)", taught at the prestigious [Collège de France](https://www.college-de-france.fr/fr). In this project, we tried numerous approaches to detect the interfaces between cement and casing, and between the cement and geological formation in oil wells, in isolation scanners' images.

Our main approaches were:
- Classic "naive" U-Net segmentation
- Modelisation of the physical phenomenon, followed by regression. This involved detecting the form of the reflected waves automatically, through Convolutional Dictoinary Learning, and then regressing a sparse model using this wave form.
- This ended up being similar to Wavelet Transforms with a learned wavelet. We then applied wavelet transform and Gabor filters as a preprocessing, and fed the more informative variables into a U-Net, which computed the segmentation
- We applied a lot of post-processing to the segmentation
- One of the key elements in our conclusion was that, by itself, a U-Net was expressive enough to do our preprocessing, and that U-Nets are capable of finding appropriate basis for denoising images. But using the more refined features permitted to create solutions that generalized better, by decreasing the effective domain gap between train and test time.