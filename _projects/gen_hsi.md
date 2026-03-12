---
layout: page
title: Generative Human-Scene Interactions
description: Breathing Life into Virtual Worlds through Generative Human-Scene Interaction
img: assets/img/project_preview/restaurant.gif
importance: 1
category: Generative 3D Content
related_publications: true
---

### The Vision
As virtual reality, the metaverse, and spatial computing continue to evolve, the demand for truly immersive digital environments has never been higher. However, populating these worlds with lifelike, intelligent characters remains a significant challenge. Traditional methods often rely on rigid, hand-crafted rules or focus solely on a single character's basic movements, ignoring the rich, dynamic context of the world around them.

Our projects introduce novel frameworks for **Generative Human-Scene Interaction**. Instead of merely placing static avatars in a 3D space, we give virtual characters the "cognitive ability" to understand their surroundings and the "physical awareness" to interact naturally with objects and other characters over time.

### How It Works: "Brains" for Smarter Virtual Interactions

To bridge the gap between high-level human intent and low-level 3D execution, our framework approaches behavior generation through two complementary, cutting-edge pathways:

- The Semantic Brain (**Multimodal Large Language Models**) {% cite li2025crafting %}: We leverage the advanced reasoning capabilities of AI language models, giving them "eyes" to see the virtual environment. By analyzing the spatial layout and semantic context of a scene, the AI can act like a virtual director. It drafts logical, context-aware "scripts" or activity descriptions—determining exactly what characters should do, where they should stand, and how they should interact with specific objects based on real-world common sense.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/apt.gif" title="multimodal LLM" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

- The Structural Brain (**Graph Generative Models**) {% cite li2023snippets %}: For complex scenarios involving multiple people and objects (like a waiter taking orders from two seated customers), we represent the scene as a dynamic web of relationships, or a "graph." Our system predicts how these relationships evolve frame-by-frame, generating fluid "activity snippets." This ensures that the interactions are not just meaningful in a single moment, but logically connected over time.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_preview/restaurant.gif" title="graph generative model" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Real-World Impact & Applications

By automating the creation of contextually meaningful, multi-character interactions, this project opens up exciting possibilities across various fields:

- **Immersive VR/AR Experiences**: Creating rich, populated digital worlds where non-player characters (NPCs) react organically to their environment and to users.

- **Social Metaverse**: Generating authentic social behaviors and crowd dynamics in shared virtual spaces.

- **Gaming & Content Creation**: Allowing developers and storytellers to populate scenes with complex activities using simple, high-level prompts rather than tedious manual animation.

- **Robotics & Simulation**: Providing highly realistic, synthetic training environments for teaching robots how to navigate human-centric spaces.