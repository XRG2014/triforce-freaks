---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

<h1>{{ page.title }}</h1>

<div class="authors-list">
  {% for author_id, author in site.data.authors %}
  <div class="author-card" style="margin-bottom: 2em;">
    <!-- Avatar -->
    {% if author.avatar %}
    <img src="{{ author.avatar }}" alt="{{ author.name }}'s avatar" style="width: 100px; height: 100px; border-radius: 50%; margin-right: 10px; float: left;">
    {% endif %}
    
    <!-- Name -->
    <h2>{{ author.name }}</h2>
    
    <!-- Bio -->
    {% if author.bio %}
    <p>{{ author.bio }}</p>
    {% endif %}
    
    <!-- Links -->
    {% if author.links %}
    <p><strong>Links:</strong></p>
    <ul>
      {% for link in author.links %}
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
  </div>
  <div style="clear: both;"></div>
  {% endfor %}
</div>
