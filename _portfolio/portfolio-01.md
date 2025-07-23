---
title: "Learning an Optimal Transport Brenier Map"
excerpt: "<img src='/images/portfolio/gen_models.png'>"
collection: portfolio
category: Research Projects
---

* __With__: [Mathis Wauquiez](https://github.com/mathis-wauquiez)
* __Ressources__: [Report](/files/portfolio/gen_models_report.pdf) / [slides](/files/portfolio/gen_models_slides.pdf) / [Code](https://github.com/mathis-wauquiez/MonotoneGradientNetworks)
* __When__: 2025
* __Associated to__: [MVA](https://www.master-mva.com/)
* __Category__: Research, Generative Models, Optimal Transport
<image src='/images/portfolio/gen_models.png' width="100%" />


Project description
==============
This group project's goal was to investigate [Monotone Gradient Networks](https://arxiv.org/abs/2301.10862). Under some mild assumptions assumptions, these networks [have been shown](https://arxiv.org/html/2404.07361v2#S4) to be universal approximators of gradients of convex functions. These architecture's are motivated by the Brenier Theorem, in optimal transport:

Consider Monge's OT problem:

$$\inf_{T:\, T_\# p_X = p_Y} \mathbb{E}_{x\sim p_X}\left[c\bigl(x,T(x)\bigr)\right]$$


where $$T_\# p_X = p_Y$$ denotes that the mapping $T$ pushes forward the source measure $p_X$ onto the target measure $p_Y$ and $c$ is a cost function (typically, the squared Euclidean distance). When $c(x,y)=\|x-y\|^2$, **Brenier's Theorem**  guarantees that, under mild conditions, **the unique optimal transport map is characterized by being the gradient of a convex function**:

$$
T(x) = \nabla \varphi(x) \quad \text{for } p_X\text{-almost every } x.
$$

This result motivates learning the gradient directly from data when an explicit convex potential is difficult to construct.


Therefore, we implemented the **M-MGN** & **C-MGN** networks, and tested them on these tasks:

- Mapping one gaussian to another
- Mapping one GMM to another
- Mapping pixel distributions
- Learning a MNIST generative network


Moreover, we introcuced the use of two losses, that were not tested in the paper:
- Kullback-Leibler divergence
- Wasserstein distance approximation through the adversarial formulation (WGANs)
- We also experimented with Maximum Mean Discrepancy (MMD), similarly to MMD-GANs (but with a Monotone Gradient generator and a different source distribution)

We show promising results for low dimensional settings, but that the models severely lacks a sufficient complexity for learning generative networks in high-dimensional spaces. 
