---
layout: default
permalink: /blog/
---

<section class="hero is-medium is-light is-bold">
    <div class="hero-body">
        <div class="container has-text-centered">
            <span class="title" itemprop="name headline">Blog Posts</span>
        </div>
    </div>
</section>
{% if site.posts.size > 0 %}
    {% for post in site.posts %}
      {% include post.html post=post %}
    {% endfor %}

  <!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
{% endif %}