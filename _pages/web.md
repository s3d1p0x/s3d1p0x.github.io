---
title: "🔍 Web"
permalink: /web/
layout: default
---

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>

<body class="bg-gray-900 text-gray-100 font-sans">

  <!-- Layout avec sidebar + contenu -->
  <div class="flex flex-col lg:flex-row">
      
      <!-- Sidebar - cachée sur mobile, visible en desktop -->
      <aside class="hidden lg:block lg:w-64 lg:fixed lg:left-0 lg:h-screen bg-gray-800 p-6 text-white overflow-y-auto z-40" style="top: 64px; height: calc(100vh - 64px);">
        <div class="mb-8">
          <h2 class="text-2xl font-bold mb-2">S3D1P0X</h2>
          <p class="text-gray-400 text-sm">Offensive Security</p>
        </div>
        
        <nav class="space-y-2">
          <a href="/" class="block py-2 px-3 rounded hover:bg-gray-700 transition">🏠 Home</a>
          <a href="/#articles" class="block py-2 px-3 rounded hover:bg-gray-700 transition">📖 Articles</a>
          
          <div class="mt-6 mb-3">
            <p class="text-gray-500 text-xs uppercase font-semibold">Categories</p>
          </div>
          
          <a href="/web/" class="block py-2 px-3 rounded bg-gray-700 transition text-sm">🔍 Web Pentest</a>
          <a href="/network/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">🌐 Network</a>
          <a href="/ad/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">🗂️ Active Directory</a>
          <a href="/re/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">⚔️ Reverse Eng.</a>
          <a href="/malware/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">🧪 Malware Analysis</a>
          <a href="/vr/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">🕵 Vuln Research</a>
          <a href="/cryptography/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">🧠 Cryptography</a>
          <a href="/write-up/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">📝 Write-Ups</a>
          <a href="/projects/" class="block py-2 px-3 rounded hover:bg-gray-700 transition text-sm">💡 Projects</a>
        </nav>
        
        <div class="mt-8 pt-8 border-t border-gray-700">
          <p class="text-gray-500 text-xs">© 2024 S3D1P0X</p>
        </div>
      </aside>
  <div class="max-w-7xl lg:ml-64 mx-auto px-4">

      <!-- Contenu principal -->
      <main class="flex-1 w-full">
  
        <!-- Hero Section -->
        <header class="bg-gray-800 py-12 md:py-16 text-center px-4 rounded-lg mt-4 lg:mt-0">
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold">🔍 Web Pentest</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400">Explore vulnerabilities and exploitation techniques for web applications</p>
        </header>

        <!-- Catégories Client/Server -->
        <section class="py-8 md:py-12 px-4">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6 max-w-4xl mx-auto">
            
            <a href="#client" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">💻</span>
                <h2 class="text-2xl md:text-3xl font-bold mb-2">Client Side</h2>
                <p class="text-gray-400 text-sm md:text-base">XSS, CSRF, DOM-based vulnerabilities, and client-side attacks</p>
              </div>
            </a>

            <a href="#server" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🖥️</span>
                <h2 class="text-2xl md:text-3xl font-bold mb-2">Server Side</h2>
                <p class="text-gray-400 text-sm md:text-base">SQLi, RCE, SSRF, file upload, and server-side vulnerabilities</p>
              </div>
            </a>

          </div>
        </section>
    
        <!-- Articles Client Side -->
        <section id="client" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-blue-600 pl-4">💻 Client Side Articles</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign client_posts = site.categories.web | where_exp: "post", "post.side == 'client'" %}
            {% if client_posts.size > 0 %}
              {% for post in client_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow hover:shadow-xl transition">
                <h3 class="text-xl md:text-2xl font-semibold mb-2">
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
                <p class="text-lg">No client-side articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Server Side -->
        <section id="server" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-green-600 pl-4">🖥️ Server Side Articles</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign server_posts = site.categories.web | where_exp: "post", "post.side == 'server'" %}
            {% if server_posts.size > 0 %}
              {% for post in server_posts %}
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow hover:shadow-xl transition">
                <h3 class="text-xl md:text-2xl font-semibold mb-2">
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
                <p class="text-lg">No server-side articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tous les articles (si pas de catégorisation) -->
        {% assign uncategorized_posts = site.categories.web | where_exp: "post", "post.side == nil" %}
        {% if uncategorized_posts.size > 0 %}
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-purple-600 pl-4">📚 All Web Articles</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% for post in uncategorized_posts %}
            <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow hover:shadow-xl transition">
              <h3 class="text-xl md:text-2xl font-semibold mb-2">
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
</div>
