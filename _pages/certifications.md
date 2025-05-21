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
      {% include readtime.html content=post.content %}
    </li>
  {% endfor %}
</ul>
