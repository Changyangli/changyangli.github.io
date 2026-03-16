---
layout: page
title: Text-to-Motion Diffusion
description: Directing Virtual Humans with Context-Aware Text-to-Motion Diffusion
img: assets/img/project_preview/text2motion.gif
importance: 1
category: Generative 3D Content
related_publications: true
---

Imagine being able to direct a 3D animated movie simply by speaking, or telling a video game character exactly what to do using natural language. This project demonstrates a **Scene-Aware Text-to-Motion Diffusion system**. We empower creators to generate highly realistic, expressive 3D human movements that are dynamically tailored to a specific environment and target location, bridging the gap between imagination and spatial reality.

### How It Works: The "Director-to-Actor" Pipeline

At its core, this system acts as a intelligent digital stunt double that listens to your commands and understands its physical surroundings. The process is driven by three key inputs:

- **The Action Prompt (Text)**: The natural language command, such as "Walk over to the sofa and sit down."

- **The Environment (Scene)**: The 3D geometry of the virtual room or space the character is in.

- **The Mark (Target Location)**: The specific destination coordinate or object within that scene.

Using a <a href="https://lilianweng.github.io/posts/2021-07-11-diffusion-models/#:~:text=Diffusion%20models%20are%20inspired%20by,data%20samples%20from%20the%20noise">Diffusion Model</a>, we "sculpt" raw temporal data into fluid movement. However, instead of just generating an isolated action, our system continuously cross-references the scene's geometry and the target destination. The output of is a rich, generative <a href="https://smpl.is.tue.mpg.de/">SMPL</a> motion sequence.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/text2motion.gif" title="text-to-motion" class="img-fluid rounded z-depth-1 w-75" %}
    </div>
</div>


### Real-World Impact & Applications

By combining natural language control with strict spatial awareness, compelling applications include:

**Next-Gen Gaming & NPCs**: Moving beyond repetitive, pre-baked animation loops, game developers can spawn dynamic characters that react to unique environments on the fly.

**Film & Animation Pre-visualization**: Directors and animators can prototype complex scenes by simply typing out stage directions, saving hundreds of hours of manual keyframe animation.

**Spatial Computing & VR**: Populating immersive mixed-reality spaces with intelligent virtual avatars that interact with scanned real-world furniture and layouts.

**Synthetic Data Generation**: Automatically generating massive datasets of humans interacting with environments to train future AI systems, robotics, and autonomous vehicles.