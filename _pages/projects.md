---
layout: page
title: Presentations
permalink: /projects/
description: Invited talks, conference presentations, and posters.
nav: true
nav_order: 2
display_categories: [Talks, Posters]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <div class="category-section mb-5">
    <a id="{{ category | slugify }}" href=".#{{ category | slugify }}">
      <h2 class="category">{{ category }}</h2>
    </a>
    {% assign down_category = category | downcase %}
    {% assign up_category = category | capitalize %}
    {% assign categorized_projects = site.projects | where_exp: "item", "item.category == category or item.category == down_category or item.category == up_category" %}
    {% assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    <div class="row row-cols-1 g-4 mb-4">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  </div>
  {% endfor %}

{% else %}

<!-- Display projects without categories -->
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  <div class="row row-cols-1 g-4 mb-4">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
{% endif %}
</div>
