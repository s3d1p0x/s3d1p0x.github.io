---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
{% endfor %}
