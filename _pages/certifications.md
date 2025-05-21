---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}

  {% if post.header.teaser %}
    {% capture teaser %}{{ post.header.teaser }}{% endcapture %}
  {% else %}
    {% assign teaser = site.teaser %}
  {% endif %}

  {% if post.id %}
    {% assign title = post.title | markdownify | remove: "<p>" | remove: "</p>" %}
  {% else %}
    {% assign title = post.title %}
  {% endif %}

  <div class="list__item">
    <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
      
      <h2 class="archive__item-title no_toc" itemprop="headline">
        <a href="{{ post.url | relative_url }}" rel="permalink">{{ title }}</a>
      </h2>

      {% include page__meta.html post=post type="list" %}

    </article>
  </div>

{% endfor %}
