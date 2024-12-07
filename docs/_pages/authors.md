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
