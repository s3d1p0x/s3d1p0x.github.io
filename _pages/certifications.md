---
title: "Certifications"
permalink: /certifications/
layout: single
---

<ul>
  {% assign cert_posts = site.categories.certifications %}
  {% for post in cert_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> – {{ post.date | date: "%d %B %Y" }}</small>
    </li>
  {% endfor %}
</ul>
