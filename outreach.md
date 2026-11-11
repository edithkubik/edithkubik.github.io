---
layout: default
title: Outreach
nav_order: 6
---

## Outreach & Education

{{ site.data.outreach.intro }}

{% for block in site.data.outreach.blocks %}
{% assign row_parity = forloop.index0 | modulo: 2 %}
{% if row_parity == 0 %}
<div class="outreach-block outreach-block-normal">
<div class="outreach-text">
<h3>{{ block.title }}</h3>
<p>{{ block.body }}</p>
</div>
{% if block.image %}
<div class="outreach-image">
{% include card-image.html src=block.image alt=block.title fit=block.image_fit focus=block.image_focus scale=block.image_scale %}
</div>
{% endif %}
</div>
{% else %}
<div class="outreach-block outreach-block-alternate">
{% if block.image %}
<div class="outreach-image">
{% include card-image.html src=block.image alt=block.title fit=block.image_fit focus=block.image_focus scale=block.image_scale %}
</div>
{% endif %}
<div class="outreach-text">
<h3>{{ block.title }}</h3>
<p>{{ block.body }}</p>
</div>
</div>
{% endif %}
{% endfor %}
