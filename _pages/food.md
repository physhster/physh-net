---
layout: default
title: Items
---

<h1>Items</h1>

<div class="lists-container">
  {% for item in site.food_lists %}
    <div class="food_list">
      <a href="{{ food_list.url }}">
        <img src="{{ food_list.image }}" alt="{{ food_list.title }}">
        <h2>{{ food_list.title }}</h2>
      </a>
    </div>
  {% endfor %}
</div>
