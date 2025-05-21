---
title: "Certifications"
permalink: /certifications/
layout: single
---

{% assign cert_posts = site.categories.certifications %}
{% for post in cert_posts %}
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p><small> {{ post.date | date: "%d %B %Y" }}</small></p>
{% endfor %}
