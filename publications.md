---
layout: default
title: Publications
nav_order: 4
---

## Lab Publications

{% if site.data.publications %}
{% for p in site.data.publications %}
- {{ p.authors }} ({{ p.year }}). **{{ p.title }}**. {{ p.venue }}. [link]({{ p.link }})
{% endfor %}
{% endif %}
