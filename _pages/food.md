---
title: Food Lists
layout: collection
permalink: /food/
collection: food_lists
entries_layout: grid
classes: wide
---

{% for food_list in site.food_lists %}
<div class="food_list-item">
  <div class="food_list-image">
    <img src="{{ food_list.image }}" alt="{{ food_list.title }}">
  </div>
  <div class="food_list-content">
    <h2>{{ food_list.title }}</h2>
    <a href="{{ food_list.url }}" class="food_list-link" target="_blank">View on Maps</a>
  </div>
</div>
{% endfor %}

<style>
.food_list-item {
  margin-bottom: 2rem;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  overflow: hidden;
}

.food_list-image img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}

.food_list-content {
  padding: 1rem;
}

.food_list-content h2 {
  margin: 0 0 1rem 0;
  font-size: 1.5rem;
}

.food_list-link {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: #007bff;
  color: white;
  text-decoration: none;
  border-radius: 4px;
}

.food_list-link:hover {
  background-color: #0056b3;
}
</style>