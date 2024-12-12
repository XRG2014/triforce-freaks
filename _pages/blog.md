---
permalink: /blog/
title: "Blog"
---

<ul>
{% for post in site.blog %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
