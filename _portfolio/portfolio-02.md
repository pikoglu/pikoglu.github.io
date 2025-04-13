---
title: "Promptable Image inpainting using the latent space of StyleGAN2-Ada"
excerpt: "<img src='/images/portfolio/stylegan.png'>"
collection: portfolio
category: Research Projects
---

* __With__: Alone
* __Ressources__: [Slides](/files/portfolio/delires_slides.pdf) / [Code](https://github.com/mathis-wauquiez/StyleGANInpainting)
* __When__: 2025
* __Associated to__: [MVA](https://www.master-mva.com/)
* __Category__: Research, Generative Models, GANs
<image src='/images/portfolio/stylegan.png' width="100%" />


Project description
==============

The goal of this project was to use StyleGAN2-Ada to solve image inpainting problems.  The first idea consists in finding a latent code compatible with the parts of the image we can observe: 
$$w^* = \text{arg}\min\limits_w \| (x - G(w))\odot(1-M)\|^2_2$$

This problem is solved through gradient descent on the latent code $w$, with an initialization that is either random or given by an encoder. Alternatives are to use a different optimization algorithm, such as $\texttt{Adam}$ or $\texttt{L-BFGS}$, or to use different similarity loss (more about that later).

This project investigates wether or not the model produces something realistic inside the region to inpaint.

This code also investigates more regularization options, to improve the quality of the inpainting. More precisely, we investagate LPIPS and an adversarial loss.


### Semanticly constrained inpainting

We can also constrain the inpainting, using a classifier or a CLIP model, by minimizing a loss (typically, BCE for classifiers or negative cosine similarity for CLIP) between the output of the network and the target output.

More on CLIP: CLIP is made of two neural networks. The first is the textual encoder: it maps sentences to textual embeddings. The second is the image encoder, which maps the images to image embeddings. These two embeddings are in the same dimension, and match when their cosine similarity is close to 1. Therefore, one could add $-\text{cos}(E_I(G(w)), E_T(\text{phrase}))$ to the loss, to enforce the semantic constraint.

### Results and future directions

We show that the inversion greatly benefits from the LPIPS loss, as the MSE alone produces blurry results. We also interpret why such complicated problems are well solved, and showed that CLIP was a powerful tool to semantically guide the inversion of our images, producing natural and rich images, at least for generative models trained on the FFHQ dataset. We also underline the compute needed to inverse the images, and the need for having good encoders and avoid as much as possible the lengthy optimization problem.