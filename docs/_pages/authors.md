---
title: "Authors"
layout: single
permalink: /authors/
---

{% for author_id, author in site.data.authors %}
### {{ author.name }}

{% if author.avatar %}
![{{ author.name }}'s avatar]({{ author.avatar }})
{% endif %}

**Bio**: {{ author.bio }}

{% if author.location %}
**Location**: {{ author.location }}
{% endif %}

{% if author.links %}
**Links**:
<ul>
  {% for link in author.links %}
  <li><a href="{{ link.url }}" target="_blank">{{ link.label }}</a></li>
  {% endfor %}
</ul>
{% endif %}
---
{% endfor %}
