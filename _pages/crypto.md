---
title: "🧠 Cryptography"
permalink: /cryptography/
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
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2">🧠 Cryptography</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400 px-2">Master cryptographic concepts and learn to break weak implementations</p>
        </header>

        <!-- Catégories Cryptography -->
        <section class="py-8 md:py-12 px-4">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6 max-w-6xl mx-auto">
            
            <a href="#symmetric" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔐</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Symmetric Cryptography</h2>
                <p class="text-gray-400 text-sm md:text-base">AES, DES, block ciphers, stream ciphers, modes of operation</p>
              </div>
            </a>

            <a href="#asymmetric" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔑</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Asymmetric Cryptography</h2>
                <p class="text-gray-400 text-sm md:text-base">RSA, ECC, Diffie-Hellman, public key infrastructure</p>
              </div>
            </a>

            <a href="#hash" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔨</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Hash Functions</h2>
                <p class="text-gray-400 text-sm md:text-base">MD5, SHA family, collision attacks, password hashing</p>
              </div>
            </a>

            <a href="#attacks" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">⚔️</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Cryptographic Attacks</h2>
                <p class="text-gray-400 text-sm md:text-base">Padding oracle, timing attacks, side-channel attacks</p>
              </div>
            </a>

            <a href="#protocols" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">📡</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Cryptographic Protocols</h2>
                <p class="text-gray-400 text-sm md:text-base">TLS/SSL, IPsec, PGP, certificate pinning</p>
              </div>
            </a>

            <a href="#quantum" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">⚛️</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">Post-Quantum Crypto</h2>
                <p class="text-gray-400 text-sm md:text-base">Quantum-resistant algorithms, lattice-based cryptography</p>
              </div>
            </a>

          </div>
        </section>

        <!-- Articles Symmetric Cryptography -->
        <section id="symmetric" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-blue-600 pl-4">🔐 Symmetric Cryptography</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign symmetric_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'symmetric'" %}
            {% if symmetric_posts.size > 0 %}
              {% for post in symmetric_posts %}
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
                <p class="text-lg">No symmetric cryptography articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Asymmetric Cryptography -->
        <section id="asymmetric" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-green-600 pl-4">🔑 Asymmetric Cryptography</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign asymmetric_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'asymmetric'" %}
            {% if asymmetric_posts.size > 0 %}
              {% for post in asymmetric_posts %}
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
                <p class="text-lg">No asymmetric cryptography articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Hash Functions -->
        <section id="hash" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-purple-600 pl-4">🔨 Hash Functions</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign hash_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'hash'" %}
            {% if hash_posts.size > 0 %}
              {% for post in hash_posts %}
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
                <p class="text-lg">No hash functions articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Cryptographic Attacks -->
        <section id="attacks" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-yellow-600 pl-4">⚔️ Cryptographic Attacks</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign attacks_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'attacks'" %}
            {% if attacks_posts.size > 0 %}
              {% for post in attacks_posts %}
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
                <p class="text-lg">No cryptographic attacks articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Cryptographic Protocols -->
        <section id="protocols" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-red-600 pl-4">📡 Cryptographic Protocols</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign protocols_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'protocols'" %}
            {% if protocols_posts.size > 0 %}
              {% for post in protocols_posts %}
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
                <p class="text-lg">No cryptographic protocols articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles Post-Quantum Crypto -->
        <section id="quantum" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-orange-600 pl-4">⚛️ Post-Quantum Crypto</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign quantum_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == 'quantum'" %}
            {% if quantum_posts.size > 0 %}
              {% for post in quantum_posts %}
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
                <p class="text-lg">No post-quantum cryptography articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tous les articles (si pas de catégorisation) -->
        {% assign uncategorized_posts = site.categories.cryptography | where_exp: "post", "post.subcategory == nil" %}
        {% if uncategorized_posts.size > 0 %}
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-gray-600 pl-4">📚 All Cryptography Articles</h2>
          
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
