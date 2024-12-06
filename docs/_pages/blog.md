---
permalink: /blog/
title: "Blog"
---

<ul>
{% for page in site.pages %}
  {% if page.path contains 'folder-name/' %}
  <li>
    <a href="{{ page.url | relative_url }}">{{ page.url }}</a>
  </li>
  {% endif %}
{% endfor %}
</ul>
