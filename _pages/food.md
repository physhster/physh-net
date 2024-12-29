---
layout: default
title: Items
---

<h1>Items</h1>

<div class="lists-container">
  {% for item in site.items %}
    <div class="item">
      <a href="{{ item.url }}">
        <img src="{{ item.image }}" alt="{{ item.title }}">
        <h2>{{ item.title }}</h2>
      </a>
    </div>
  {% endfor %}
</div>
