---
layout: default
title: Food Lists
---

<h1>Food Lists by Continent</h1>

{% assign continents = site.food_lists | map: "continent" | uniq %}

{% for continent in continents %}
  <h2>{{ continent | capitalize }}</h2>
  <div class="food-grid">
    {% assign continent_items = site.food_lists | where: "continent", continent %}
    {% for item in continent_items %}
      <div class="food-card">
        {% if item.list_image %}
          <img src="{{ item.list_image }}" alt="{{ item.list_title }}">
        {% endif %}
        <h3>{{ item.list_title }}</h3>
        <a href="{{ item.list_url }}" target="_blank">Visit Site</a>
      </div>
    {% endfor %}
  </div>
{% endfor %}