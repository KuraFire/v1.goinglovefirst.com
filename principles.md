---
title: The Principles Of Love First
permalink: /principles/
image: /assets/images/principles/principles-love-first.jpg
---

Our principles are the foundations of our ways of being. They underpin the personal values, beliefs, and behaviors that define our unique inner layer of identity.


> Principles are ways of successfully dealing with reality to get what you want out of life.
<cite><em>Principles</em>, by Ray Dalio</cite>

The principles use active voice so you can clearly see how to apply them in your life. They are specific, allowing you to focus on one at a time if necessary. They don’t require academic knowledge or special training, making them easy and accessible for everyone to benefit from. Lastly, they are not prescriptive, so wield them gracefully however much you want.

## The Elemental Principles
The first five principles are the core foundations upon which Love First builds, and correspond to the classic elements: heart, water, fire, air, and earth.



<ul class="principles-list">

{% assign principles = site.principles | sort: "principle_order" %}
{% for principle in principles %}
  {% if principle.element %}{% capture elem %}{{ principle.element }}{% endcapture %}
  {% capture elem_icon %}{% include element-icon.html element=elem %}{% endcapture %}
  {% else %}{% capture elem_icon %}{% endcapture %}
  {% endif %}
<li>{{ elem_icon }}<a href="{{ principle.url }}"><strong>{{ principle.title }}</strong></a><br/>
  {{ principle.excerpt }}</li>
{% endfor %}

</ul>
