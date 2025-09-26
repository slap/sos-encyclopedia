---
layout: default
title: SOS Encyclopedia
---

## Examples

### Polynomias over Q that are SOS over R but not over Q
<ul>
{%- assign polys_rat = site.polynomials | where_exp: "p", "p.tags contains 'rational'" -%}
{% for p in polys_rat %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>


## All examples

<ul>
{% for p in polys %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>
