---
layout: page
title: Items
permalink: /food/
---

<div class="lists-container">
  {% for food_list in site.food %}
    <div class="food_list_page">
      <a href="{{ food_list.list_url }}" target="_blank">
        {% if food_list.list_image %}
           <img src="{{ food_list.list_image }}" alt="{{ food_list.list_title }}">
        {% endif %}
        <h2>{{ food_list.list_title }}</h2>
      </a>
    </div>
  {% endfor %}
</div>
