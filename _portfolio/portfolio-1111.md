---
title: "Image Completion Using Efficient Belief Propagation via Priority Scheduling and Dynamic Pruning"
excerpt: "<img src='/images/portfolio/inpainting.png'>"
collection: portfolio
category: Research Projects
---

* __With__: Supervised by [Pascal Monasse](https://ecoledesponts.fr/pascal-monasse)
* __Resources__: [Report](/files/portfolio/inpainting_report.pdf)
* __When__: 2024
* __Associated to__: [LIGM](https://siteigm.univ-mlv.fr/)

The project explores a semi-supervised patch-based image inpainting algorithm that relies on belief propagation rather than extensive training data. The method leverages nodes and labels to propagate candidate patches across masked regions, prioritizing areas with limited valid candidates. The belief propagation process involves alternating forward and backward message-passing iterations, progressively refining label assignments to generate visually coherent fills. Key contributions include a frugal approach to patch selection using SSD criteria and adaptive thresholds, along with performance evaluations across various images and textures. Despite some limitations in handling complex textures or gradients, the algorithm proved effective, particularly for texture completion tasks.
