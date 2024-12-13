---
title: "Authors"
layout: single
permalink: /authors/
authors:
  - XRG2014
  - superdatanimations
---

<div class="authors-list">
  {% for author in site.data.authors %}
  <div class="author-card" style="margin-bottom: 2em;">
    <!-- Avatar -->
    {% assign author_data = author[1] %}
    {% if author_data.avatar %}
    <img src="https://xrg2014.github.io{{ '/' | relative_url }}{{ author_data.avatar }}" alt="{{ author_data.name }}'s avatar" style="width: 100px; height: 100px; border-radius: 50%; margin-right: 10px; float: left;">
    {% endif %}
    
    <!-- Name -->
    <h2>{{ author_data.name }}</h2>
    
    <!-- Bio -->
    {% if author_data.bio %}
    <p>{{ author_data.bio }}</p>
    {% endif %}
    
    <!-- Links -->
    {% if author_data.links %}
    <p><strong>Links:</strong></p>
    <ul>
      {% for link in author_data.links %}
      <li>
        <a href="{{ link.url }}" target="_blank">
          {% if link.icon %}
          <i class="{{ link.icon }}"></i>
          {% endif %}
          {{ link.label }}
        </a>
      </li>
      {% endfor %}
    </ul>
    {% endif %}
    
    <!-- Follow Button -->
    {% for link in author_data.links %}
      <p>
        <a href="{{ link.url }}" class="btn btn-primary" target="_blank">Follow</a>
      </p>
      {% break %}
    {% endfor %}
  </div>

  <div style="clear: both;"></div>
  {% endfor %}
</div>

{% include follow-button.html %}