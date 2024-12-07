---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

<ul>
  {% for author.name, author in site.data.authors %}
  <li>{{ author.name }}: {{ author.name }}</li>
  {% endfor %}
</ul>
