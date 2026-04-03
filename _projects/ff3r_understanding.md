---
layout: page
title: Feed-Forward 3D Reconstruction & Understanding
# description: with background image
img: assets/img/project_preview/ff_3r_understanding.gif
importance: 1
category: Scene Understanding & Perception
related_publications: true
---


### The Vision: Holistic Spatial Intelligence
Next-generation spatial intelligence—whether for augmented reality, robotics, or autonomous navigation—requires devices to perceive the world not just as a collection of pixels or raw 3D point clouds, but as distinct, meaningful entities. 

Recently, "feed-forward" 3D reconstruction models have made incredible strides, allowing us to recover dense 3D geometry directly from unposed 2D images in a single pass. However, a critical gap remains: these models lack semantic awareness. They can build the 3D structure of a room, but they cannot tell you where a chair ends and a desk begins. 

### The Project: FAST3DIS
To bridge this gap, I worked on **FAST3DIS** {% cite li2026fast3dis %}. The goal of this project was to build a unified, fully end-to-end architecture capable of simultaneously reconstructing the 3D geometry of a scene and segmenting it into distinct, class-agnostic instances—all from unposed multi-view RGB images.

Instead of treating 3D reconstruction and semantic understanding as separate, disjointed steps, FAST3DIS integrates them into a seamless, single-pass pipeline.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/ff_3r_understanding.gif" title="FAST3DIS segmentation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    FAST3DIS extracts 3D geometry and instance boundaries from 2D views in a single forward pass.
</div>

### How It Works: Embedding Physics into Transformers
To achieve this end-to-end scene understanding, the architecture relies on several key geometric and structural innovations:

* **Dual-Pass Geometric Backbone:** We leverage strong geometric priors (via <a href="https://github.com/ByteDance-Seed/Depth-Anything-3">Depth Anything V3</a>) to extract dense depth and camera parameters. Through a lightweight LoRA adaptation, we simultaneously extract multi-scale visual features while perfectly preserving the backbone's zero-shot 3D reconstruction capabilities.
* **Dynamic 3D Anchors:** Instead of searching blindly, the model generates learnable "3D anchors." Think of these as dynamic digital probes deployed into the continuous 3D world space. They physically ground our object queries, acting as the spatial centers of potential objects.
* **Anchor-Sampling Cross-Attention:** To efficiently gather visual evidence, these 3D anchors are mathematically projected back onto the 2D multi-view feature maps. This allows the model to sample local context precisely where the object should be across different camera views, naturally enforcing multi-view consistency without the crushing memory burden of global attention.
* **Spatial Overlap Regularization:** To ensure sharp boundaries between physically adjacent objects, we introduced a dynamically scheduled overlap penalty that actively prevents multiple queries from claiming the same spatial region.

### The Impact
FAST3DIS demonstrates that explicit feature and spatial regularization can successfully elevate feed-forward models from pure geometric reconstruction to holistic 3D scene understanding. By formulating instance segmentation as a direct set prediction problem in continuous 3D space, the framework delivers robust segmentation on complex indoor environments with exceptional inference efficiency and memory scalability.
