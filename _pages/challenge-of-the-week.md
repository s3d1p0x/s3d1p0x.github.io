---
title: "🎯 Challenge of the Week"
permalink: /ctf/challenge-of-the-week/
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
        <header class="bg-gradient-to-r from-blue-900 to-purple-900 py-12 md:py-16 text-center px-4 rounded-lg mt-4 lg:mt-0">
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2 mb-4">🎯 Challenge of the Week</h1>
          <p class="mt-4 text-base md:text-lg text-gray-200 px-2">Test your skills with a unique challenge every week</p>
          <div class="mt-6 inline-block bg-yellow-600 text-white px-6 py-3 rounded-full font-semibold">
            New challenge every Monday!
          </div>
        </header>

        <!-- Introduction -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">📖 About the Challenge</h2>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              Every week, I publish a new cybersecurity challenge designed to test and improve your skills across different domains: web exploitation, binary analysis, cryptography, reverse engineering, and more.
            </p>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed">
              Each challenge comes with a detailed write-up after a week, explaining the solution, techniques used, and key takeaways. Whether you're a beginner or an experienced hacker, there's always something to learn!
            </p>
          </div>
        </section>

        <!-- How it works -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">🚀 How it works</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="bg-gray-800 p-6 rounded-xl text-center">
              <div class="text-5xl mb-4">1️⃣</div>
              <h3 class="text-xl font-semibold mb-3 text-blue-400">New Challenge</h3>
              <p class="text-gray-400">Every Monday, a new challenge is published with instructions and files to download.</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl text-center">
              <div class="text-5xl mb-4">2️⃣</div>
              <h3 class="text-xl font-semibold mb-3 text-purple-400">Solve It</h3>
              <p class="text-gray-400">You have one week to solve the challenge. Take your time, research, and learn new techniques!</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl text-center">
              <div class="text-5xl mb-4">3️⃣</div>
              <h3 class="text-xl font-semibold mb-3 text-green-400">Read Write-up</h3>
              <p class="text-gray-400">The following Monday, a detailed write-up is published with the solution and explanations.</p>
            </div>
          </div>
        </section>

        <!-- Challenge Categories -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">🎨 Challenge Categories</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-blue-600">
              <h3 class="text-lg font-semibold mb-2 text-blue-400">🌐 Web Exploitation</h3>
              <p class="text-gray-400 text-sm">SQLi, XSS, SSRF, authentication bypass</p>
            </div>

            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-purple-600">
              <h3 class="text-lg font-semibold mb-2 text-purple-400">👾 Binary Exploitation</h3>
              <p class="text-gray-400 text-sm">Buffer overflows, ROP, heap exploitation</p>
            </div>

            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-green-600">
              <h3 class="text-lg font-semibold mb-2 text-green-400">⚔️ Reverse Engineering</h3>
              <p class="text-gray-400 text-sm">Binary analysis, crackmes, obfuscation</p>
            </div>

            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-yellow-600">
              <h3 class="text-lg font-semibold mb-2 text-yellow-400">🧠 Cryptography</h3>
              <p class="text-gray-400 text-sm">Crypto attacks, implementation flaws</p>
            </div>

            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-red-600">
              <h3 class="text-lg font-semibold mb-2 text-red-400">🕵 Forensics</h3>
              <p class="text-gray-400 text-sm">Memory analysis, file carving, PCAP</p>
            </div>

            <div class="bg-gray-800 p-4 rounded-xl border-l-4 border-orange-600">
              <h3 class="text-lg font-semibold mb-2 text-orange-400">🔐 Miscellaneous</h3>
              <p class="text-gray-400 text-sm">Mixed challenges, OSINT, steganography</p>
            </div>
          </div>
        </section>

        <!-- Current Challenge -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-yellow-600 pl-4">⚡ Current Challenge</h2>
          
          {% assign current_challenges = site.categories.challenge-of-the-week | where_exp: "post", "post.status == 'active'" %}
          {% if current_challenges.size > 0 %}
            <div class="grid grid-cols-1 gap-6">
              {% for post in current_challenges limit:1 %}
              <article class="bg-gradient-to-br from-gray-800 to-gray-900 p-6 md:p-8 rounded-xl shadow-lg border-2 border-yellow-600">
                <div class="flex items-center justify-between mb-4 flex-wrap gap-2">
                  <h3 class="text-2xl md:text-3xl font-bold text-yellow-400">{{ post.title }}</h3>
                  <span class="bg-yellow-600 text-white px-4 py-2 rounded-full text-sm font-semibold">🔥 ACTIVE</span>
                </div>
                
                {% if post.difficulty %}
                <div class="mb-4">
                  <span class="text-gray-400">Difficulty: </span>
                  <span class="{% if post.difficulty == 'Easy' %}text-green-400{% elsif post.difficulty == 'Medium' %}text-yellow-400{% else %}text-red-400{% endif %} font-semibold">
                    {{ post.difficulty }}
                  </span>
                </div>
                {% endif %}

                {% if post.category %}
                <div class="mb-4">
                  <span class="bg-blue-600 text-white px-3 py-1 rounded-full text-sm">{{ post.category }}</span>
                </div>
                {% endif %}

                {% if post.excerpt %}
                <p class="text-gray-300 mb-4 text-base md:text-lg">{{ post.excerpt | strip_html }}</p>
                {% endif %}

                <div class="flex gap-4 flex-wrap">
                  <a href="{{ post.url | relative_url }}" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold transition">
                    View Challenge
                  </a>
                  {% if post.download_link %}
                  <a href="{{ post.download_link }}" class="bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-lg font-semibold transition">
                    Download Files
                  </a>
                  {% endif %}
                </div>

                {% if post.deadline %}
                <div class="mt-6 bg-gray-900 p-4 rounded-lg border-l-4 border-red-600">
                  <p class="text-gray-300">
                    <strong class="text-red-400">⏰ Deadline:</strong> {{ post.deadline | date: "%B %d, %Y" }}
                  </p>
                </div>
                {% endif %}
              </article>
              {% endfor %}
            </div>
          {% else %}
            <div class="bg-gray-800 p-8 rounded-xl text-center">
              <p class="text-xl text-gray-400 mb-4">⏳ New challenge coming soon...</p>
              <p class="text-gray-500">Check back every Monday for a new challenge!</p>
            </div>
          {% endif %}
        </section>

        <!-- Past Challenges -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-purple-600 pl-4">📚 Past Challenges</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            {% assign past_challenges = site.categories.challenge-of-the-week | where_exp: "post", "post.status == 'solved'" %}
            {% if past_challenges.size > 0 %}
              {% for post in past_challenges %}
              <article class="bg-gray-800 p-6 rounded-xl shadow hover:shadow-xl transition">
                <div class="flex items-center justify-between mb-3">
                  <h3 class="text-xl md:text-2xl font-semibold">
                    <a href="{{ post.url | relative_url }}" class="hover:text-blue-500 transition">{{ post.title }}</a>
                  </h3>
                  <span class="bg-green-600 text-white px-3 py-1 rounded-full text-xs">✓ Solved</span>
                </div>

                {% if post.difficulty %}
                <div class="mb-2">
                  <span class="text-gray-400 text-sm">Difficulty: </span>
                  <span class="{% if post.difficulty == 'Easy' %}text-green-400{% elsif post.difficulty == 'Medium' %}text-yellow-400{% else %}text-red-400{% endif %} text-sm font-semibold">
                    {{ post.difficulty }}
                  </span>
                </div>
                {% endif %}

                {% if post.category %}
                <div class="mb-3">
                  <span class="bg-gray-700 text-gray-300 px-2 py-1 rounded text-xs">{{ post.category }}</span>
                </div>
                {% endif %}

                {% if post.excerpt %}
                <p class="text-gray-400 mb-4 text-sm">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
                {% endif %}

                <div class="flex items-center justify-between text-sm text-gray-500">
                  <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  <a href="{{ post.url | relative_url }}" class="text-blue-400 hover:text-blue-300">Read Write-up →</a>
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 bg-gray-800 p-8 rounded-xl text-center">
                <p class="text-gray-400">No past challenges yet. Be the first to solve the current one!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Rules & Guidelines -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">📋 Rules & Guidelines</h2>
            
            <div class="space-y-4">
              <div class="flex items-start">
                <span class="text-green-400 text-2xl mr-4">✓</span>
                <div>
                  <h3 class="font-semibold text-green-400 mb-1">Do your own research</h3>
                  <p class="text-gray-400 text-sm">Use Google, read documentation, learn new tools - that's the whole point!</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-green-400 text-2xl mr-4">✓</span>
                <div>
                  <h3 class="font-semibold text-green-400 mb-1">Share your approach</h3>
                  <p class="text-gray-400 text-sm">Feel free to discuss techniques and share your learning process (but not the flag!).</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-red-400 text-2xl mr-4">✗</span>
                <div>
                  <h3 class="font-semibold text-red-400 mb-1">No spoilers</h3>
                  <p class="text-gray-400 text-sm">Don't post solutions or flags publicly before the write-up is released.</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-blue-400 text-2xl mr-4">💡</span>
                <div>
                  <h3 class="font-semibold text-blue-400 mb-1">Ask for hints</h3>
                  <p class="text-gray-400 text-sm">Stuck? Reach out on social media or comments - I'm happy to provide hints!</p>
                </div>
              </div>
            </div>
          </div>
        </section>

        <!-- Call to Action -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto mb-8">
          <div class="bg-gradient-to-r from-blue-900 to-purple-900 p-6 md:p-8 rounded-xl text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">🎉 Ready to challenge yourself?</h2>
            <p class="text-base md:text-lg text-gray-200 mb-6">
              Subscribe to get notified when new challenges are released!
            </p>
            <div class="flex justify-center gap-4 flex-wrap">
              <a href="https://github.com/s3d1p0x" target="_blank" class="bg-gray-800 hover:bg-gray-700 px-6 py-3 rounded-lg transition font-semibold">
                Follow on GitHub
              </a>
              <a href="https://www.linkedin.com/in/quentin-auspitz-cybersecurity-pentest" target="_blank" class="bg-gray-800 hover:bg-gray-700 px-6 py-3 rounded-lg transition font-semibold">
                Connect on LinkedIn
              </a>
            </div>
          </div>
        </section>
  
      </main>
    </div>
  </div>
</body>
</html>
