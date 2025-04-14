---
layout: page # Or a custom theme_landing layout if you create one
title: Quant Code Arsenal
permalink: /arsenal/
---

## Welcome to the Quant Code Arsenal!

This section contains essential code components, templates, scripts, and utilities curated to accelerate your algorithmic trading development. Explore these resources to find building blocks for your strategies.

### Arsenal Components:

<ul>
  {% assign arsenal_items = site.arsenal | sort: "title" %}
  {% for item in arsenal_items %}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a> - {{ item.description }}
      {% if item.difficulty %}<span class="difficulty-badge" style="margin-left: 5px; padding: 2px 5px; font-size: 0.8em; background-color: #eee; border-radius: 3px;">{{ item.difficulty }}</span>{% endif %}
    </li>
  {% else %}
    <li>No Arsenal components found yet. Add items to the _arsenal folder!</li>
  {% endfor %}
</ul>
