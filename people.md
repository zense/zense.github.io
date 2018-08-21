---
layout: page
title: People
permalink: /people/
---

{% for item in site.people %}
  <h2><a href="{{ item.url }}">{{ item.name }}</a></h2>
  <p>{{ item.description }}</p>
{% endfor %}

