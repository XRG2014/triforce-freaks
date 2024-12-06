---
permalink: /blog/
title: "Blog"
---

<ul>
{% for page in site.pages %}
  {% if page.path contains '_posts/' %}
  <li>
    <a href="{{ page.url | relative_url }}">{{ page.url }}</a>
  </li>
  {% endif %}
{% endfor %}
</ul>
