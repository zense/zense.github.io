---
layout: page
title: People
permalink: /people/
---

{% assign rows = site.people.size | divided_by: 3.0 | ceil %}
{% for i in (1..rows) %}
  {% assign offset = forloop.index0 | times: 3 %}
  {% assign offset = offset - 3 %}
  <div class="columns">
    {% for item in site.people limit:3 offset:offset %}
    <div class="column is-one-third has-text-centered person">
        {% avatar user=item.github size=200 %}
        <h2 class="title"><a href="{{ item.url }}">{{ item.name }}</a></h2>
        <p class="subtitle">{{ item.description }}</p>    
    </div>
    {% endfor %}
  </div>
{% endfor %}