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

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");

*, *::before, *::after {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif !important;
}

:root {
  --global-theme-color: #0d9488 !important;
  --global-hover-color: #0284c7 !important;
}

.navbar {
  border-top: 3px solid #0d9488 !important;
}

.navbar-nav .nav-item.active > .nav-link {
  color: #0d9488 !important;
  font-weight: 600 !important;
  border-bottom: 2px solid #0d9488 !important;
}

.navbar-nav .nav-link,
.navbar-brand,
.post-header .post-title,
h2,
h2 a {
  text-transform: capitalize !important;
}

.projects h2.category {
  color: #0d9488 !important;
  border-bottom: 2px solid var(--global-divider-color) !important;
  padding-bottom: 0.5rem !important;
  margin-top: 2rem !important;
  margin-bottom: 1.5rem !important;
  text-align: left !important;
  font-size: 1.6rem !important;
  font-weight: 700 !important;
  display: block;
  width: 100%;
}

.projects .card {
  border: 1px solid var(--global-divider-color) !important;
  border-left: 3px solid #0d9488 !important;
  border-radius: 8px !important;
  background-color: var(--global-card-bg-color) !important;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04) !important;
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease !important;
}

.projects .card .card-body {
  padding: 1.5rem !important;
}

.projects .card .card-title {
  font-size: 1.25rem !important;
  font-weight: 600 !important;
  color: var(--global-text-color) !important;
  line-height: 1.4 !important;
  margin-bottom: 0.75rem !important;
}

.projects .card .card-text {
  color: var(--global-text-color-light) !important;
  font-size: 0.95rem !important;
  line-height: 1.5 !important;
  margin-bottom: 0 !important;
}

.projects .card:hover {
  transform: translateY(-2px) !important;
  box-shadow: 0 8px 24px rgba(13, 148, 136, 0.18) !important;
  border-left-color: #0284c7 !important;
}

.projects .card:hover .card-title {
  color: #0d9488 !important;
}
</style>
