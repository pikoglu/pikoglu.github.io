---
title: "Constraint-Guided Prediction Refinement via Deterministic Diffusion Trajectories"
excerpt: "<img src='/images/portfolio/diffusion_constraints.png'>"
collection: portfolio
category: Research Projects
---

* __With__: Pantelis Dogoulis, Fabien Bernier, Karim Tit, Maxime Cordy  
* __Resources__: [arXiv Preprint](https://arxiv.org/abs/2506.12911v1)  
* __When__: 2025  
* __Associated to__: [University of Luxembourg](https://wwwen.uni.lu/)

This project introduces **CARDIFF**, a general-purpose, model-agnostic framework for refining predictions to satisfy hard constraints using deterministic diffusion models (DDIMs). The approach enables post hoc correction of outputs from any base model, by guiding them along learned diffusion trajectories and injecting constraint gradient information at each denoising step.

Unlike traditional constrained generation or prediction pipelines, CARDIFF does not require retraining the base model or embedding constraints directly into the architecture. It is particularly effective in cases involving nonlinear or non-convex equality constraints.

We applied the method in two domains:
- **Adversarial attacks** on tabular data, ensuring that generated examples obey column-level constraints;
- **AC power flow prediction**, improving compliance with Kirchhoff’s laws in power grid simulations.

In both cases, CARDIFF significantly reduced constraint violations while maintaining or improving task performance. The work provides both theoretical insights and empirical evidence for its utility in constraint-aware AI applications.
