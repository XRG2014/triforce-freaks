---
permalink: /blog/
title: "Blog"
---

<ul>
{% for page in site.pages %}
  {% if page.path contains 'docs/_blog/' %}
  <li>
    <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
  </li>
  {% endif %}
{% endfor %}
</ul>
