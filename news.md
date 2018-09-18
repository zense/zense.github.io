---
layout: default
title: News
permalink: /news/
---
<section class="hero is-medium is-light is-bold">
    <div class="hero-body">
        <div class="container has-text-centered">
            <span class="title" itemprop="name headline">News</span>
        </div>
    </div>
</section>

{% if site.news.size > 0 %}
    {% for item in site.news %}
      {% include post.html post=item %}
    {% endfor %}
{% endif %}
