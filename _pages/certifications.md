---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  <big><a href="{{ post.url | relative_url }}">{{ post.title }}</a></big>
  <small>{% include page__meta.html post=post %}</small>
{% endfor %}
