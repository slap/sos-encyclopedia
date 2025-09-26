---
layout: default
title: SOS Encyclopedia
---

## Examples

### Polynomials over $\mathbb{Q}$ that are SOS over $\mathbb{R}$ but not over $\mathbb{Q}$
<ul>
{%- assign polys_rat = site.polynomials | where_exp: "p", "p.tags contains 'rational'" -%}
{% for p in polys_rat %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>

### Polynomials in the positive boundary of the SOS cone
<ul>
{%- assign polys_pos = site.polynomials | where_exp: "p", "p.tags contains 'positive-boundary'" -%}
{% for p in polys_pos %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>

### Polynomials with long length that provide lower bounds for the Pythagoras numbers
<ul>
{%- assign polys_pythagoras = site.polynomials | where_exp: "p", "p.tags contains 'pythagoras'" -%}
{% for p in polys_pythagoras %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>

## All examples

<ul>
{% for p in site.polynomials  %}
  <li><a href="{{ site.baseurl }}{{ p.url }}">{{ p.author }}. {{ p.title }}</a> — degree: {{ p.degree }} — tags: {{ p.tags | join: ", " }}</li>
{% endfor %}
</ul>
