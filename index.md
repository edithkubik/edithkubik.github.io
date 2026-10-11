---
layout: default
title: Home
nav_order: 1
---

## Welcome to PEARL

The Planetary Evolution & Accretion Research Laboratory investigates the fundamental processes that shape terrestrial planets, from the protoplanetary disk to differentiated planets.

### Current Projects

<div class="grid grid-2">
{% for project in site.data.projects %}
  <div class="project-card">
    <img src="{{ project.image }}" alt="{{ project.title }}">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </div>
{% endfor %}
</div>
