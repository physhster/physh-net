---
title: Food Lists
layout: collection
permalink: /food/
collection: food_lists
entries_layout: grid
classes: wide
---


{% for food_list in site.food_lists %}
 <img src="{{ food_list.image }}" alt="{{ food_list.image_alt }}">
 <span>{{ food_list.url }}</span>
{% endfor %}