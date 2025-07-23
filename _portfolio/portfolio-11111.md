---
title: "Instability of Hamiltonian Dynamics with Machine-Learned Potentials"
excerpt: "<img src='/images/portfolio/molecular_dynamics.png'>"
collection: portfolio
category: Research Projects
---

* __With__: With [Maryam El Yaagoubi](https://github.com/maryamelyaagoubi)  Supervised by [M. Marinica](https://scholar.google.com/citations?user=Yfj9RqUAAAAJ&hl=en), CEA Paris-Saclay  
* __Resources__: [Report](/files/portfolio/MOPSI_FELIX_MARYAM.pdf)  
* __When__: 2024 
* __Associated to__: [CEA Paris-Saclay](https://www.cea.fr/)

This project explores the instability of molecular dynamics simulations when using neural network-based force fields. Starting with a simple MLP trained on the Müller-Brown potential, the study progresses to graph neural networks (GNNs), including architectures like GraphSAGE and PhysNet, known for their physical equivariance.

The simulations were conducted using the MD17 dataset—focusing on ethanol and aspirin molecules—analyzing the effects of various hyperparameters (e.g., batch size, number of features, cutoff radius, force loss weight) on the stability of Hamiltonian trajectories.

Two distinct types of instabilities were identified: gradual energy drift and sudden explosive divergence. The work highlights the importance of incorporating physical constraints, such as force terms and symmetry properties, into model design. Even with optimized parameters, around 4% of the simulations exhibited instabilities, suggesting future directions like Hessian-informed training to further improve robustness in learned molecular dynamics.
