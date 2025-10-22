---
title: "🎓 Certifications"
permalink: /certifications/
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
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2">🎓 Certifications</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400 px-2">Reviews, tips and feedback on cybersecurity certifications and ProLabs</p>
        </header>

        <!-- Catégories Certifications -->
        <section class="py-8 md:py-12 px-4">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6 max-w-4xl mx-auto">
            
            <a href="#cpts" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🎯</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">CPTS</h2>
                <p class="text-gray-400 text-sm md:text-base">Certified Penetration Testing Specialist - HackTheBox</p>
              </div>
            </a>

            <a href="#zephyr" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">💨</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">ProLab: Zephyr</h2>
                <p class="text-gray-400 text-sm md:text-base">HackTheBox ProLab - Advanced Active Directory</p>
              </div>
            </a>

            <a href="#dante" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🔥</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">ProLab: Dante</h2>
                <p class="text-gray-400 text-sm md:text-base">HackTheBox ProLab - Network Penetration Testing</p>
              </div>
            </a>

            <a href="#ejpt" class="block bg-gray-800 p-6 md:p-8 rounded-xl shadow-lg hover:bg-gray-700 transition transform hover:scale-105">
              <div class="text-center">
                <span class="text-4xl md:text-5xl mb-4 block">🎓</span>
                <h2 class="text-xl md:text-2xl font-bold mb-2">eJPT</h2>
                <p class="text-gray-400 text-sm md:text-base">eLearnSecurity Junior Penetration Tester</p>
              </div>
            </a>

          </div>
        </section>

        <!-- Articles CPTS -->
        <section id="cpts" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-blue-600 pl-4">🎯 CPTS</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign cpts_posts = site.categories.certifications | where_exp: "post", "post.subcategory == 'cpts'" %}
            {% if cpts_posts.size > 0 %}
              {% for post in cpts_posts %}
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
              <!-- Article CPTS existant hardcodé -->
              <article class="bg-gray-800 p-4 md:p-6 rounded-xl shadow">
                <h3 class="text-xl md:text-2xl font-semibold">
                  <a href="/certifications/CPTS/" class="hover:text-blue-500 transition">CPTS Review</a>
                </h3>
                <p class="text-gray-400 mt-2 text-sm md:text-base">Feedback on my experience with HackTheBox CPTS certification - complete review of the Penetration Tester path and exam tips.</p>
                <div class="mt-4 flex items-center text-sm text-gray-500">
                  <span>📅 August 31, 2024</span>
                </div>
              </article>
            {% endif %}
          </div>
        </section>

        <!-- Articles ProLab: Zephyr -->
        <section id="zephyr" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-green-600 pl-4">💨 ProLab: Zephyr</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign zephyr_posts = site.categories.certifications | where_exp: "post", "post.subcategory == 'zephyr'" %}
            {% if zephyr_posts.size > 0 %}
              {% for post in zephyr_posts %}
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
                <p class="text-lg">No ProLab Zephyr articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles ProLab: Dante -->
        <section id="dante" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-purple-600 pl-4">🔥 ProLab: Dante</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign dante_posts = site.categories.certifications | where_exp: "post", "post.subcategory == 'dante'" %}
            {% if dante_posts.size > 0 %}
              {% for post in dante_posts %}
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
                <p class="text-lg">No ProLab Dante articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Articles eJPT -->
        <section id="ejpt" class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-yellow-600 pl-4">🎓 eJPT</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            {% assign ejpt_posts = site.categories.certifications | where_exp: "post", "post.subcategory == 'ejpt'" %}
            {% if ejpt_posts.size > 0 %}
              {% for post in ejpt_posts %}
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
                <p class="text-lg">No eJPT articles yet. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tous les articles (si pas de catégorisation) -->
        {% assign uncategorized_posts = site.categories.certifications | where_exp: "post", "post.subcategory == nil" %}
        {% if uncategorized_posts.size > 0 %}
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 border-l-4 border-gray-600 pl-4">📚 All Certifications Articles</h2>
          
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
