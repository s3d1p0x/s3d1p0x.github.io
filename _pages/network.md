---
title: "🌐 Network"
permalink: /network/
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
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2">🌐 Network</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400 px-2">Explore network vulnerabilities, protocols exploitation and infrastructure attacks</p>
        </header>

        <!-- Catégories Network -->
        <section class="py-8 md:py-12 px-4">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6 max-w-6xl mx-auto">
            
            <a href="#protocols" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">📡</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Protocols</h2>
                <p class="text-gray-400 text-sm md:text-base">TCP/IP, DNS, DHCP, SMB, FTP, and protocol vulnerabilities</p>
              </div>
            </a>

            <a href="#reconnaissance" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔭</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Reconnaissance</h2>
                <p class="text-gray-400 text-sm md:text-base">Network scanning, enumeration, and information gathering</p>
              </div>
            </a>

            <a href="#mitm" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🎭</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Man-in-the-Middle</h2>
                <p class="text-gray-400 text-sm md:text-base">ARP spoofing, LLMNR/NBT-NS poisoning, relay attacks</p>
              </div>
            </a>

            <a href="#wireless" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">📶</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Wireless</h2>
                <p class="text-gray-400 text-sm md:text-base">WiFi attacks, WPA/WEP cracking, rogue AP, evil twin</p>
              </div>
            </a>

            <a href="#pivoting" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔀</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Pivoting & Tunneling</h2>
                <p class="text-gray-400 text-sm md:text-base">Port forwarding, SSH tunnels, proxy chains, lateral movement</p>
              </div>
            </a>

            <a href="#infrastructure" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🏗️</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Infrastructure</h2>
                <p class="text-gray-400 text-sm md:text-base">Network devices, routers, switches, firewalls exploitation</p>
              </div>
            </a>

          </div>
        </section>

        <!-- Articles Protocols -->
        <section id="protocols" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-blue-600 pl-4">📡 Protocols</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign protocol_posts = site.categories.network | where_exp: "post", "post.subcategory == 'protocols'" %}
            {% if protocol_posts.size > 0 %}
              {% for post in protocol_posts %}
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
                <p class="text-lg">No protocol articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Reconnaissance -->
        <section id="reconnaissance" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-green-600 pl-4">🔭 Reconnaissance</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign recon_posts = site.categories.network | where_exp: "post", "post.subcategory == 'reconnaissance'" %}
            {% if recon_posts.size > 0 %}
              {% for post in recon_posts %}
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
                <p class="text-lg">No reconnaissance articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles MITM -->
        <section id="mitm" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-purple-600 pl-4">🎭 Man-in-the-Middle</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign mitm_posts = site.categories.network | where_exp: "post", "post.subcategory == 'mitm'" %}
            {% if mitm_posts.size > 0 %}
              {% for post in mitm_posts %}
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
                <p class="text-lg">No MITM articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Wireless -->
        <section id="wireless" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-yellow-600 pl-4">📶 Wireless</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign wireless_posts = site.categories.network | where_exp: "post", "post.subcategory == 'wireless'" %}
            {% if wireless_posts.size > 0 %}
              {% for post in wireless_posts %}
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
                <p class="text-lg">No wireless articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Pivoting -->
        <section id="pivoting" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-red-600 pl-4">🔀 Pivoting & Tunneling</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign pivoting_posts = site.categories.network | where_exp: "post", "post.subcategory == 'pivoting'" %}
            {% if pivoting_posts.size > 0 %}
              {% for post in pivoting_posts %}
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
                <p class="text-lg">No pivoting articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Infrastructure -->
        <section id="infrastructure" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-orange-600 pl-4">🏗️ Infrastructure</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign infra_posts = site.categories.network | where_exp: "post", "post.subcategory == 'infrastructure'" %}
            {% if infra_posts.size > 0 %}
              {% for post in infra_posts %}
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
                <p class="text-lg">No infrastructure articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tous les articles (si pas de catégorisation) -->
        {% assign uncategorized_posts = site.categories.network | where_exp: "post", "post.subcategory == nil" %}
        {% if uncategorized_posts.size > 0 %}
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-gray-600 pl-4">📚 All Network Articles</h2>
          
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
