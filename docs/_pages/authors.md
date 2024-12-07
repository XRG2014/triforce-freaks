---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

<ul>
  {% for author.id, author in site.data.authors %}
  <li>{{ author.id }}: {{ author.name }}</li>
  {% endfor %}
</ul>
