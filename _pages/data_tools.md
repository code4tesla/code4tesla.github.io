---
layout: page # Or a custom theme_landing layout
title: Quant Code Data Tools
permalink: /data-tools/
---

## Welcome to the Quant Code Arsenal!

Brief description of the Arsenal theme...

### Components:

<ul>
  {% assign arsenal_items = site.arsenal | sort: "title" %}
  {% for item in arsenal_items %}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a> - {{ item.description }}
      {% if item.difficulty %}<span class="difficulty-badge">{{ item.difficulty }}</span>{% endif %}
    </li>
  {% endfor %}
</ul>