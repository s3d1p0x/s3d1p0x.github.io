---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  <span class="page__meta-readtime">
    <i class="far fa-clock" aria-hidden="true"></i>
    {% assign words = post.content | number_of_words %}
    {% assign words_per_minute = site.words_per_minute | default: 200 %}
    {% if words < words_per_minute %}
      {{ site.data.ui-text[site.locale].less_than | default: "less than" }} 1 {{ site.data.ui-text[site.locale].minute_read | default: "minute read" }}
    {% elsif words == words_per_minute %}
      1 {{ site.data.ui-text[site.locale].minute_read | default: "minute read" }}
    {% else %}
      {{ words | divided_by: words_per_minute }} {{ site.data.ui-text[site.locale].minute_read | default: "minute read" }}
    {% endif %}
  </span>
{% endfor %}
