---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}

  {% assign title = post.title | markdownify | remove: "<p>" | remove: "</p>" %}

  <div class="list__item">
    <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
      <h2 class="archive__item-title no_toc" itemprop="headline">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>

      {% include page__meta.html type="list" %}
    </article>
  </div>

{% endfor %}
