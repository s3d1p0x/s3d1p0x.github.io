---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  {% include posts-taxonomy.html post=post %}
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  {% include page__meta.html post=post %}
{% endfor %}
