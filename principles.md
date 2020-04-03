---
title: The Principles Of Love First
permalink: /principles/
---

Our principles are the foundations of our ways of being. We have personal values, beliefs, and behaviors that define our inner layer of identity.



Dive deeper into the principles below:

<ul class="principles-list">

{% assign principles = site.pages | where_exp: "item", "item.principle" | sort: "principle" %}
{% for page in principles %}
<li><a href="{% link {{ page.path }} %}"><strong>{{ page.title }}</strong></a><br/>
  {{ page.principle_byline }}</li>
{% endfor %}

</ul>
