---
title: "Certifications"
permalink: /certifications/
layout: single
---

<style>
  h1, h2, h3, h4 {
    border-bottom: 0 !important;
    box-shadow: none !important;
  }
</style>

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}

<div class="list__item">
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>

    {% include page__meta.html type="list" %}
  </article>
</div>

{% endfor %}
