---
permalink: /blog/
title: "Blog"
---

## Blog pages

<ul>
{% for post in site.blog %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
