---
title: "Analyzing Gaussian Frosting: A mesh representation for 3D Gaussian Splatting"
excerpt: "<video width='100%' autoplay loop muted><source src='https://mathisw59assets.pages.dev/gda_dance.mp4' type='video/mp4'></video>"
collection: portfolio
category: Research Projects
---

* __With__: Félix Fourreau
* __Ressources__: [Report](/files/portfolio/gda_report.pdf); [Slides](/files/portfolio/gda_slides.odp)
* __When__: 2025
* __Associated to__: [MVA](https://www.master-mva.com/)

Project Description
=======================
The project was based on the [Gaussian Frosting](https://anttwo.github.io/frosting/) paper, by [Antoine Guédon](https://anttwo.github.io/) and [Vincent Lepetit](https://vincentlepetit.github.io/). Their method extracts accurate and editable meshes from 3D Gaussian Splatting representations within minutes on a single GPU. The specifity of their meshes is that contain gaussian splats, which allows volumetric rendering and thus better preserves the quality of the 3D GS representation.

After understanding the details of how 3DGS and [SuGaR](https://imagine.enpc.fr/~guedona/sugar/) works, we delved into the methodology of Gaussian Frosting, and used this method ourselves to animate a figurine and render fuzzy scenes.

This project also includes a complete related work section, were take a deep dive into image based rendering (IBR) methods, their evolution, and the current landcape of the research domain.

Abstract
========================
Recently, 3D gaussian splatting demonstrated promising results in inverse image rendering by representing radiance
fields as a set of gaussians, enabling fast and accurate
3D reconstruction. However, gaussian representations are
incompatible with mesh-based 3D editing software. The
SuGaR method addresses this by retrieving a mesh from the
gaussians, facilitating integration with standard 3D modeling tools for editing, animating, sculpting and relightning.
Although SuGaR is significantly faster than state-of-the-art
Neural Signed Distance Fields (neural SDF), the conversion to a mesh incurs visual quality loss as the gaussians
are constrained to the mesh, which limits volumetric rendering. To overcome this, Gaussian Frosting creates a ”frosting” layer that encases the mesh, used for volumetric rendering using gaussian splatting. Additionally, the proposed
approach supports deformable meshes, automatically adjusting the radiance field carried by the mesh, therefore enabling easy scene editing while maintaining competitive visual quality.

Results
========================

Results using SuGaR for mesh extraction:
<video width='100%' height='100%' controls autoplay loop muted><source src='https://mathisw59assets.pages.dev/gda_2.mp4' type='video/mp4'></video>
Results using Gaussian Frosting for mesh extraction:
<video width='100%' height='100%' controls autoplay loop muted><source src='https://mathisw59assets.pages.dev/gda_1.mp4' type='video/mp4'></video>
<video width='100%' height='100%' controls autoplay loop muted><source src='https://mathisw59assets.pages.dev/gda_3.mp4' type='video/mp4'></video>
<video width='100%' height='100%' controls autoplay loop muted><source src='https://mathisw59assets.pages.dev/gda_dance.mp4' type='video/mp4'></video>
