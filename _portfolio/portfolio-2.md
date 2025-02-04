---
title: "Few-Shot Learning: ImageNet-Sketch Classification"
excerpt: "<img src='/images/portfolio/sketchnet.jpeg'>"
collection: portfolio
category: Deep Learning
---

* __With__: Alone
* __Ressources__: [Report](/files/portfolio/recvis_challenge_report.pdf); [Code](https://github.com/mathisw59/recvis24_a3)
* __When__: 2024
* __Associated to__: [MVA](https://www.master-mva.com/)

ImageNet-Sketch is a dataset of 500 classes, with only 5 samples per class, augmented into 4 different views. The goal of the challenge was to classify the sketches into the 500 classes.

I explored many approaches to this problem, including:
- Using a pre-trained models like ResNet50, ViT, Swin Transformer, etc. and fine-tuning them on the dataset.
- Using a foundation model like CLIP and use it for image classification by retrieval using the KNN algorithm or linear probing.
- Pre-train a model using contrastive learning and fine-tune it on the dataset.

In order to train all of these models, I created a simple pipeline that can be used to train any of these models using yaml files, specifying the model, the dataset, the optimizer, the loss function, etc., similar to Hydra.

My best performance was above 90% accuracy on the test set, using the DINOv1 ViT-H/14 pretrained model and KNN retrieval.