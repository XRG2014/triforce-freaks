---
title: "Authors"
layout: single
permalink: /authors/
---

{% for author_id, author in site.data.authors %}
<div style="margin-bottom: 2em;">
  <h2>{{ author.name }}</h2>
  {% if author.avatar %}
  <img src="{{ author.avatar }}" alt="{{ author.name }}'s avatar" style="width: 100px; height: 100px; border-radius: 50%;">
  {% endif %}
  <p>{{ author.bio }}</p>
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
{% endfor %}
