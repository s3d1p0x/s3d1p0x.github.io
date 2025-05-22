---
title: "🎯 Challenge of the week"
permalink: /ctf/challenge-of-the-week/
layout: single
---

<style>
  h1, h2, h3, h4 {
    border-bottom: 0 !important;
    box-shadow: none !important;
  }

  h2 {
    margin-bottom: 0rem !important;
  }

  .page__meta {
    margin-top: 0rem !important;
  }
</style>

{% assign challenge-of-the-week_posts = site.categories.challenge-of-the-week %}
{% for post in challenge-of-the-week_posts %}

<div class="list__item">
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>

    {% include page__meta.html type="list" %}
  </article>
</div>

{% endfor %}
