---
layout: page
title: Items
permalink: /food/
---

<h1>Food Lists by Continent</h1>

{% assign continents = site.food_lists | keys %}

{% for continent in continents %}
  <h2>{{ continent | capitalize }}</h2>
  <div class="food-list-container">
    {% assign items = site.food_lists[continent] %}
    {% for item in items %}
      {% include food_list item=item %}
    {% endfor %}
  </div>
{% endfor %}
