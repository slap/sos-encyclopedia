---
layout: default
title: SOS Encyclopedia
---

## Examples

<ul>
{% for p in site.polynomials %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>
