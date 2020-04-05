---
title: The Principles Of Love First
permalink: /principles/
featured_image: /assets/images/principles/principles-love-first.jpg
---

Our principles are the foundations of our ways of being. We have personal values, beliefs, and behaviors that define our inner layer of identity.



Dive deeper into the principles below:

<ul class="principles-list">

{% assign principles = site.pages | where_exp: "item", "item.principle" | sort: "principle" %}
{% for page in principles %}
  {% if page.element %}{% capture elem %}{{ page.element }}{% endcapture %}
  {% capture elem_icon %}{% include element-icon.html element=elem %}{% endcapture %}
  {% endif %}
<li>{{ elem_icon }}<a href="{{ page.url }}"><strong>{{ page.title }}</strong></a><br/>
  {{ page.principle_byline }}</li>
{% endfor %}

</ul>
