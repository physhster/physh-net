---
layout: page
title: Items
permalink: /food/
---

<h1>Food List</h1>

{% assign categories = site.food_lists | map: "relative_path" | map: "split" | map: "first" | uniq %}

{% for category in categories %}
  <h2>{{ category | capitalize }}</h2>
  <div class="food-container">
    {% assign category_items = site.food_lists | where_exp: "item", "item.relative_path contains category" %}
    {% for item in category_items %}
      <div class="food-item">
        {% if item.list_image %}
          <a href="{{ item.list_url }}">
            <img src="{{ item.list_image }}" alt="{{ item.list_title }}">
          </a>
        {% endif %}
        <a href="{{ item.list_url }}">
          <h3>{{ item.list_title }}</h3>
        </a>
      </div>
    {% endfor %}
  </div>
{% endfor %}
