---
layout: default
---

<section class="hero">
  <div class="hero-body">
    <div class="container has-text-centered">
      <h1 class="title">Posts</h1>
    </div>
  </div>
</section>

{% if site.posts.size > 0 %}
    {% for post in site.posts %}
      {% include post.html post=post %}
    {% endfor %}

  <!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
{% endif %}