---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}

<div class="list__item">
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
    <big>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </big>

    {% include page__meta.html type="list" %}
  </article>
</div>

{% endfor %}
