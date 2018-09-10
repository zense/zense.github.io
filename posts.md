---
layout: default
---

<div class="">
  {% if page.title %}
    <h1 class="page-heading">yabadada</h1>
  {% endif %}


  {% if site.posts.size > 0 %}
    <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2>
    <!-- <ul class="post-list"> -->
      {% for post in site.posts %}
      {% assign colour_value = ["danger", "info", "warning", "primary", "link"] %}
      <h1>{{ colour_value.first }}</h1>
      {% assign colour_tag = "hero is-" | append: colour_value[0] %}
      <h1>{{ colour_tag }}</h1>
      <section class="{{ colour_tag }}">
      <div class="hero-body">
      <a class="container">
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
          <h1 class="title is-2" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </h1>
        <h1 class="subtitle is-4">{{ post.date | date: date_format }}</h1>
        {% if site.show_excerpts %}
          {{ post.excerpt }}
        {% endif %}
        </a>
        </div>
      </section>
      {% endfor %}
    <!-- </ul> -->

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {% endif %}

</div>
