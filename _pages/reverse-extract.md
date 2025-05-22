---
title: "🧬 Reverse extract"
permalink: /ctf/reverse-extract/
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

{% assign reverse-extract_posts = site.categories.reverse-extract %}
{% for post in reverse-extract_posts %}

<div class="list__item">
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork"{% if post.locale %} lang="{{ post.locale }}"{% endif %}>
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
