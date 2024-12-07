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
    {% if author.avatar %}
    <img src="{{ author.avatar }}" alt="{{ author.name }}'s avatar" style="width: 100px; height: 100px; border-radius: 50%; margin-right: 10px; float: left;">
    {% endif %}
    <h2>{{ author.name }}</h2>
    {% if author.bio %}
    <p>{{ author.bio }}</p>
    {% endif %}
    {% if author.location %}
    <p><strong>Location:</strong> {{ author.location }}</p>
    {% endif %}
    {% if author.links %}
    <p><strong>Links:</strong></p>
    <ul>
      {% for link in author.links %}
      <li><a href="{{ link.url }}" target="_blank">{{ link.label }}</a></li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
  <div style="clear: both;"></div>
  {% endfor %}
</div>
