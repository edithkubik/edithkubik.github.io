---
layout: default
title: Home
nav_order: 1
---

## Welcome to PEARL

The Planetary Evolution & Accretion Research Laboratory investigates the fundamental processes that shape terrestrial planets, from small objects in the protoplanetary disk to fully-grown and differentiated planets.

### Current Projects

<div class="grid grid-2">
{% for project in site.data.projects %}
  <div class="project-card">
    {% include card-image.html src=project.image alt=project.title fit=project.image_fit focus=project.image_focus scale=project.image_scale %}
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </div>
{% endfor %}
</div>
