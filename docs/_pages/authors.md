---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

<pre>{{ site.data.authors }}</pre>

<ul>
  {% for author in site.data.authors %}
  <li>{{ author }}</li>
  {% endfor %}
</ul>

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
    
  </div>
