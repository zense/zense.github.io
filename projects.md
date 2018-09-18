---
layout: default
title: Projects
permalink: /projects/
---
<section class="hero is-medium is-light is-bold">
    <div class="hero-body">
        <div class="container has-text-centered">
            <span class="title" itemprop="name headline">Projects</span>
        </div>
    </div>
</section>

{% for item in site.projects %}
{% assign colour_value = "danger, info, warning, primary, link, dark, light" | split: ', ' %}
{% assign random = colour_value | sample %}
{% assign bold = " is-bold,  " | split: ', ' | sample %}
{% assign colour_tag = "hero is-" | append: random | append: bold %}
<section class="{{ colour_tag }}">
  <div class="hero-body">
    <div class="container is-fluid">
      <a href="{{ item.url | relative_url }}">
        <h1 class="title">
            {{ item.title | escape }}
        </h1>
        <h2 class="subtitle" style="white-space: normal; text-overflow: clip">
          {{ item.excerpt | strip_html | truncatewords:20 }}
        </h2>
      </a>
    </div>
  </div>
</section>
{% endfor %}

