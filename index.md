---
layout: splash
title: "Accueil"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero.jpg
  actions:
    - label: "Lire les derniers articles"
      url: "#articles"
excerpt: "Pentest • Reverse • Exploit Dev • Malware Analysis"
---

## À propos du blog

Ce blog est dédié à tous ceux qui aiment comprendre, démonter, contourner et exploiter. Que vous soyez pentester, étudiant en cybersécurité ou amateur de CTFs, vous trouverez ici des analyses profondes, des write-ups et des retours d’expérience concrets.

## Catégories principales

- 🔍 Pentest Web
- 🌐 Pentest Réseau
- 🖥️ Windows / Linux
- ⚔️ Reverse & Exploitation
- 🧪 Analyse Malware
- 🧠 Crypto & CTF

## Derniers articles

{% for post in site.posts limit:6 %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%d %B %Y" }}
{% endfor %}

## Restons connectés

Suivez-moi pour plus de contenu ou proposez un sujet :

- [GitHub](#)
- [Twitter](#)
- [LinkedIn](#)
- [HTB](#)
