---
layout: default
title: People
nav_order: 5
---

## Lab Members

<div class="grid grid-3">
{% for person in site.data.people %}
  <div class="person-card">
    <img src="{{ person.image }}" alt="{{ person.name }}">
    <h3>{{ person.name }}</h3>
    <p class="role">{{ person.role }}</p>
    <p>{{ person.bio }}</p>
    {% if person.email %}<p><a href="mailto:{{ person.email }}">Contact</a></p>{% endif %}
  </div>
{% endfor %}
</div>

## About the Principal Investigator

**Dr. Edith Kubik** directs the Planetary Evolution & Accretion Research Laboratory. Her research focuses on understanding planetary formation and evolution through isotopic and geochemical analysis of meteoritic and planetary materials.

Edith received her Ph.D. in Planetary Science from [University] and has conducted research at [institutions]. She is committed to advancing our understanding of planetary processes while mentoring the next generation of scientists through both research and outreach activities.

## Former Members

<div class="grid grid-3">
{% for person in site.data.alumni %}
  <div class="person-card">
    <img src="{{ person.image }}" alt="{{ person.name }}">
    <h3>{{ person.name }}</h3>
    <p class="role">{{ person.role }}</p>
    <p>{{ person.bio }}</p>
    {% if person.email %}<p><a href="mailto:{{ person.email }}">Contact</a></p>{% endif %}
  </div>
{% endfor %}
</div>


### Contact & Resources

- **Email**: edith.kubik@proton.me
- **Office**: [Building and Room Number]
- **Office Hours**: [Schedule]
- **CV**: [Download PDF]

### Collaborations & Affiliations

PEARL Lab collaborates with researchers worldwide on projects investigating planetary materials, isotopic systems, and accretion dynamics.
