---
layout: default
title: News
nav_order: 3
---

## Lab News & Blog

<div class="news-list">
{% assign sorted_posts = site.posts | sort: "date" | reverse %}
{% for post in sorted_posts %}
  <div class="news-item">
    {% if post.image %}{% include card-image.html src=post.image alt=post.title fit=post.image_fit focus=post.image_focus scale=post.image_scale %}{% endif %}
    <div class="news-item-content">
      <h3>{{ post.title }}</h3>
      <div class="news-item-date">{{ post.date | date: "%B %d, %Y" }}</div>
      <p>{{ post.excerpt }}</p>
    </div>
  </div>
{% endfor %}
</div>
