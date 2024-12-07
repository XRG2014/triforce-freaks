---
title: "Authors"
layout: single
permalink: /authors/
author_profile: false
---

<ul>
  {% for author_id, author in site.data.authors %}
  <li>{{ author_id }}: {{ author.name }}</li>
  {% endfor %}
</ul>
