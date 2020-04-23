---
layout: page
title: Language Matters
permalink: /definitions/
---

<p><nobr>Love First</nobr> aims to be precise about its use of language, as it introduces a number of new concepts that build on common terms which don’t always have a widely shared understanding. This page collects posts detailing important terminology.</p>

{% for category in site.categories %}
  {% if category[0] == 'Definitions' %}
  {% for post in category[1] %}
  <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
  <p>{{ post.excerpt | strip_html | truncatewords:40 }}</p>
  {% endfor %}
  {% endif %}
{% endfor %}
