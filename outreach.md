---
layout: default
title: Outreach
nav_order: 6
---

## Outreach & Education

{{ site.data.outreach.intro }}

{% for block in site.data.outreach.blocks %}
  {% if forloop.index0 | modulo: 2 == 0 %}
    <!-- Even index (0, 2, 4...) - normal layout: text left, image right -->
    <div class="outreach-block outreach-block-normal">
      <div class="outreach-text">
        <h3>{{ block.title }}</h3>
        {{ block.body | markdownify }}
      </div>
      {% if block.image %}
        <div class="outreach-image">
          <img src="{{ block.image }}" alt="{{ block.title }}">
        </div>
      {% endif %}
    </div>
  {% else %}
    <!-- Odd index (1, 3, 5...) - alternate layout: text right, image left, dark bg -->
    <div class="outreach-block outreach-block-alternate">
      {% if block.image %}
        <div class="outreach-image">
          <img src="{{ block.image }}" alt="{{ block.title }}">
        </div>
      {% endif %}
      <div class="outreach-text">
        <h3>{{ block.title }}</h3>
        {{ block.body | markdownify }}
      </div>
    </div>
  {% endif %}
{% endfor %}
