---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

{% for author in site.data.authors %}
  <div class="author-card" style="margin-bottom: 2em;">
    {% assign author_data = author[1] %}

    {% if author_data.avatar %}
    <img src="{{ author_data.avatar }}" alt="{{ author_data.name }}'s avatar" style="width: 100px; height: 100px; border-radius: 50%; margin-right: 10px; float: left;">
    {% endif %}
    
    <h2>{{ author_data.name }}</h2>
    {% if author_data.bio %}
    <p>{{ author_data.bio }}</p>
    {% endif %}
    
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
  </div>
  <div style="clear: both;"></div>
{% endfor %}
