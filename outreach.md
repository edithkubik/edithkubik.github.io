---
layout: default
title: Outreach
nav_order: 6
---

## Outreach & Education

{{ site.data.outreach.intro }}

{% for block in site.data.outreach.blocks %}
  {% if forloop.index0 | modulo: 2 == 0 %}
    <div class="outreach-block outreach-block-normal">
      <div class="outreach-text">
        <h3>{{ block.title }}</h3>
        <p>{{ block.body }}</p>
      </div>
      {% if block.image %}
        <div class="outreach-image">
          <img src="{{ block.image }}" alt="{{ block.title }}">
        </div>
      {% endif %}
    </div>
  {% else %}
    <div class="outreach-block outreach-block-alternate">
      {% if block.image %}
        <div class="outreach-image">
          <img src="{{ block.image }}" alt="{{ block.title }}">
        </div>
      {% endif %}
      <div class="outreach-text">
        <h3>{{ block.title }}</h3>
        <p>{{ block.body }}</p>
      </div>
    </div>
  {% endif %}
{% endfor %}
