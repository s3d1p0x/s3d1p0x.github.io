---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  <big><a href="{{ post.url | relative_url }}">{{ post.title }}</a></big>
  <p><small><small>{% include page__meta.html content=post.content %}</small></small></p>
{% endfor %}
