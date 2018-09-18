---
layout: page
title: News
permalink: /news/
---

{% if site.news.size > 0 %}
    {% for item in site.news %}
      {% include post.html post=item %}
    {% endfor %}
{% endif %}
