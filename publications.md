---
layout: default
title: Publications
nav_order: 4
---

## Lab Publications

{% if site.data.publications %}
{% for year_group in site.data.publications %}
### {{ year_group[0] }}

{% for pub in year_group[1] %}
- {{ pub.authors }}. **{{ pub.title }}**. {{ pub.venue }}. [link]({{ pub.link }})
{% endfor %}

{% endfor %}
{% endif %}
