---
title: "🕵 Vulnerability Research"
permalink: /vr/
layout: default
---

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>

<body class="bg-gray-900 text-gray-100 font-sans">

  <div class="max-w-7xl mx-auto px-4">

    <!-- Layout avec sidebar + contenu -->
    <div class="flex flex-col lg:flex-row">
      
      <!-- Sidebar - cachée sur mobile, visible en desktop -->
      <aside class="lg:block lg:w-64 lg:sticky lg:top-0 lg:h-screen bg-gray-800 p-4 text-white">
        {% include sidebar.html %}
      </aside>
      
      <!-- Contenu principal -->
      <main class="flex-1 lg:pl-8 w-full">
  
        <!-- Hero Section -->
        <header class="bg-gray-800 py-12 md:py-16 text-center px-4 rounded-lg mt-4 lg:mt-0">
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2">🕵 Vulnerability Research</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400 px-2">Discover, analyze and exploit vulnerabilities from zero-day to CVE analysis</p>
        </header>

        <!-- Catégories Vulnerability Research -->
        <section class="py-8 md:py-12 px-4">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6 max-w-6xl mx-auto">
            
            <a href="#fuzzing" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🎲</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Fuzzing</h2>
                <p class="text-gray-400 text-sm md:text-base">AFL, LibFuzzer, custom fuzzers, coverage-guided fuzzing</p>
              </div>
            </a>

            <a href="#source-audit" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔍</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Source Code Audit</h2>
                <p class="text-gray-400 text-sm md:text-base">Manual code review, SAST tools, vulnerability patterns</p>
              </div>
            </a>

            <a href="#exploit-dev" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">💥</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Exploit Development</h2>
                <p class="text-gray-400 text-sm md:text-base">PoC creation, exploit chains, weaponization techniques</p>
              </div>
            </a>

            <a href="#cve" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">📋</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">CVE Analysis</h2>
                <p class="text-gray-400 text-sm md:text-base">Vulnerability deep dives, patch diffing, root cause analysis</p>
              </div>
            </a>

            <a href="#binary" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔬</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Binary Analysis</h2>
                <p class="text-gray-400 text-sm md:text-base">Vulnerability discovery in closed-source, binary diffing</p>
              </div>
            </a>

            <a href="#zero-day" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">💎</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Zero-Day Research</h2>
                <p class="text-gray-400 text-sm md:text-base">Novel vulnerability classes, advanced research techniques</p>
              </div>
            </a>

          </div>
        </section>

        <!-- Articles Fuzzing -->
        <section id="fuzzing" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-blue-600 pl-4">🎲 Fuzzing</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign fuzzing_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'fuzzing'" %}
            {% if fuzzing_posts.size > 0 %}
              {% for post in fuzzing_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No fuzzing articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Source Code Audit -->
        <section id="source-audit" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-green-600 pl-4">🔍 Source Code Audit</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign audit_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'source-audit'" %}
            {% if audit_posts.size > 0 %}
              {% for post in audit_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No source code audit articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Exploit Development -->
        <section id="exploit-dev" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-purple-600 pl-4">💥 Exploit Development</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign exploit_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'exploit-dev'" %}
            {% if exploit_posts.size > 0 %}
              {% for post in exploit_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No exploit development articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles CVE Analysis -->
        <section id="cve" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-yellow-600 pl-4">📋 CVE Analysis</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign cve_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'cve'" %}
            {% if cve_posts.size > 0 %}
              {% for post in cve_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No CVE analysis articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Binary Analysis -->
        <section id="binary" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-red-600 pl-4">🔬 Binary Analysis</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign binary_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'binary'" %}
            {% if binary_posts.size > 0 %}
              {% for post in binary_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No binary analysis articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Zero-Day Research -->
        <section id="zero-day" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-orange-600 pl-4">💎 Zero-Day Research</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign zeroday_posts = site.categories.vr | where_exp: "post", "post.subcategory == 'zero-day'" %}
            {% if zeroday_posts.size > 0 %}
              {% for post in zeroday_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                </h3>
                {% if post.excerpt %}
                <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                {% endif %}
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  {% if post.read_time %}
                  <span class="ml-4">⏱️ {{ post.read_time }}</span>
                  {% endif %}
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 text-center py-8 text-gray-500">
                <p class="text-lg">No zero-day research articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tous les articles (si pas de catégorisation) -->
        {% assign uncategorized_posts = site.categories.vr | where_exp: "post", "post.subcategory == nil" %}
        {% if uncategorized_posts.size > 0 %}
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-gray-600 pl-4">📚 All Vulnerability Research Articles</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% for post in uncategorized_posts %}
            <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
              <h3 class="text-xl md:text-2xl font-semibold">
                <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
              </h3>
              {% if post.excerpt %}
              <p class="text-gray-400 mt-2 text-sm md:text-base">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
              {% endif %}
              <div class="mt-4 flex items-center text-sm text-gray-500">
                <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                {% if post.read_time %}
                <span class="ml-4">⏱️ {{ post.read_time }}</span>
                {% endif %}
              </div>
            </article>
            {% endfor %}
          </div>
        </section>
        {% endif %}
  
      </main>
    </div>
  </div>
</body>
</html>
