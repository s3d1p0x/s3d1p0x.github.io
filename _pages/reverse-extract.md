---
title: "🧬 Reverse Extract"
permalink: /ctf/reverse-extract/
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
        <header class="bg-gradient-to-r from-purple-900 to-pink-900 py-12 md:py-16 text-center px-4 rounded-lg mt-4 lg:mt-0">
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2 mb-4">🧬 Reverse Extract</h1>
          <p class="mt-4 text-base md:text-lg text-gray-200 px-2">Dismantle obscure CTF binaries and extract hidden secrets</p>
          <div class="mt-6 inline-block bg-pink-600 text-white px-6 py-3 rounded-full font-semibold">
            Master reverse engineering techniques
          </div>
        </header>

        <!-- Introduction -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">🔬 What is Reverse Extract?</h2>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              <strong class="text-purple-400">Reverse Extract</strong> is a collection of carefully selected obscure binaries from various CTF competitions. Each binary presents unique challenges in reverse engineering, from anti-debugging techniques to complex obfuscation methods.
            </p>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              Unlike typical crackmes, these challenges come from real CTF competitions and require a deep understanding of:
            </p>
            <ul class="space-y-2 mb-4">
              <li class="flex items-start">
                <span class="text-purple-400 mr-3">•</span>
                <span class="text-gray-300">Static and dynamic analysis techniques</span>
              </li>
              <li class="flex items-start">
                <span class="text-purple-400 mr-3">•</span>
                <span class="text-gray-300">Assembly language (x86, x64, ARM)</span>
              </li>
              <li class="flex items-start">
                <span class="text-purple-400 mr-3">•</span>
                <span class="text-gray-300">Anti-debugging and anti-analysis methods</span>
              </li>
              <li class="flex items-start">
                <span class="text-purple-400 mr-3">•</span>
                <span class="text-gray-300">Cryptographic algorithms and custom encoding</span>
              </li>
              <li class="flex items-start">
                <span class="text-purple-400 mr-3">•</span>
                <span class="text-gray-300">Tools like IDA Pro, Ghidra, radare2, and GDB</span>
              </li>
            </ul>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed">
              Each binary comes with a detailed write-up explaining the analysis process, tools used, and key insights to master reverse engineering.
            </p>
          </div>
        </section>

        <!-- Challenge Types -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">🎯 Challenge Types</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-blue-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🛡️</div>
              <h3 class="text-lg font-semibold mb-2 text-blue-400">Anti-Debugging</h3>
              <p class="text-gray-400 text-sm">Binaries with sophisticated anti-debugging techniques, debugger detection, and process monitoring</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-purple-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🌀</div>
              <h3 class="text-lg font-semibold mb-2 text-purple-400">Obfuscation</h3>
              <p class="text-gray-400 text-sm">Heavily obfuscated code with control flow flattening, string encryption, and code virtualization</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-green-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">📦</div>
              <h3 class="text-lg font-semibold mb-2 text-green-400">Packers</h3>
              <p class="text-gray-400 text-sm">Custom packers and crypters requiring unpacking techniques and memory analysis</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-yellow-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🔐</div>
              <h3 class="text-lg font-semibold mb-2 text-yellow-400">Crypto Algorithms</h3>
              <p class="text-gray-400 text-sm">Custom cryptographic implementations and algorithm identification challenges</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-red-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🤖</div>
              <h3 class="text-lg font-semibold mb-2 text-red-400">VM Challenges</h3>
              <p class="text-gray-400 text-sm">Custom virtual machines requiring bytecode analysis and instruction set understanding</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-orange-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🔧</div>
              <h3 class="text-lg font-semibold mb-2 text-orange-400">Exotic Platforms</h3>
              <p class="text-gray-400 text-sm">Binaries for unusual architectures: MIPS, ARM, PowerPC, and embedded systems</p>
            </div>
          </div>
        </section>

        <!-- Difficulty Levels -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">📊 Difficulty Levels</h2>
          
          <div class="space-y-4">
            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">🟢</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-green-400">Beginner</h3>
                <p class="text-gray-400">Basic reverse engineering techniques, simple obfuscation, straightforward logic. Good starting point for learning fundamentals.</p>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">🟡</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-yellow-400">Intermediate</h3>
                <p class="text-gray-400">Moderate obfuscation, anti-debugging techniques, requires understanding of assembly and debugging tools.</p>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">🟠</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-orange-400">Advanced</h3>
                <p class="text-gray-400">Heavy obfuscation, custom packers, requires advanced RE skills and multiple tool combinations.</p>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">🔴</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-red-400">Expert</h3>
                <p class="text-gray-400">Extremely challenging binaries with multiple protection layers, custom VMs, and sophisticated anti-analysis techniques.</p>
              </div>
            </div>
          </div>
        </section>

        <!-- Available Challenges -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-purple-600 pl-4">🎮 Available Challenges</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            {% assign reverse_challenges = site.categories.reverse-extract %}
            {% if reverse_challenges.size > 0 %}
              {% for post in reverse_challenges %}
              <article class="bg-gray-800 p-6 rounded-xl shadow hover:shadow-xl transition border-l-4 
                {% if post.difficulty == 'Beginner' %}border-green-600
                {% elsif post.difficulty == 'Intermediate' %}border-yellow-600
                {% elsif post.difficulty == 'Advanced' %}border-orange-600
                {% else %}border-red-600{% endif %}">
                
                <div class="flex items-center justify-between mb-3 flex-wrap gap-2">
                  <h3 class="text-xl md:text-2xl font-semibold">
                    <a href="{{ post.url | relative_url }}" class="hover:text-purple-400 transition">{{ post.title }}</a>
                  </h3>
                  {% if post.difficulty %}
                  <span class="
                    {% if post.difficulty == 'Beginner' %}bg-green-600
                    {% elsif post.difficulty == 'Intermediate' %}bg-yellow-600
                    {% elsif post.difficulty == 'Advanced' %}bg-orange-600
                    {% else %}bg-red-600{% endif %}
                    text-white px-3 py-1 rounded-full text-xs font-semibold">
                    {{ post.difficulty }}
                  </span>
                  {% endif %}
                </div>

                {% if post.ctf_name %}
                <div class="mb-3">
                  <span class="text-gray-400 text-sm">From: </span>
                  <span class="text-purple-400 text-sm font-semibold">{{ post.ctf_name }}</span>
                </div>
                {% endif %}

                {% if post.architecture %}
                <div class="mb-3">
                  <span class="bg-gray-700 text-gray-300 px-2 py-1 rounded text-xs mr-2">{{ post.architecture }}</span>
                  {% if post.challenge_type %}
                  <span class="bg-gray-700 text-gray-300 px-2 py-1 rounded text-xs">{{ post.challenge_type }}</span>
                  {% endif %}
                </div>
                {% endif %}

                {% if post.excerpt %}
                <p class="text-gray-400 mb-4 text-sm">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
                {% endif %}

                <div class="flex items-center justify-between">
                  <span class="text-sm text-gray-500">📅 {{ post.date | date: "%B %d, %Y" }}</span>
                  <a href="{{ post.url | relative_url }}" class="text-purple-400 hover:text-purple-300 text-sm font-semibold">
                    Read Analysis →
                  </a>
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 bg-gray-800 p-8 rounded-xl text-center">
                <div class="text-6xl mb-4">🧬</div>
                <p class="text-xl text-gray-400 mb-4">No challenges available yet</p>
                <p class="text-gray-500">Check back soon for exciting reverse engineering challenges!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Tools & Resources -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-blue-600 pl-4">🔧 Essential Tools</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <!-- Static Analysis -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <h3 class="text-xl font-semibold mb-4 text-blue-400">Static Analysis</h3>
              <ul class="space-y-2">
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">IDA Pro / Ghidra</span>
                    <p class="text-gray-400 text-sm">Disassembly and decompilation</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">radare2 / Cutter</span>
                    <p class="text-gray-400 text-sm">Open-source reverse engineering</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">Binary Ninja</span>
                    <p class="text-gray-400 text-sm">Modern RE platform</p>
                  </div>
                </li>
              </ul>
            </div>

            <!-- Dynamic Analysis -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <h3 class="text-xl font-semibold mb-4 text-green-400">Dynamic Analysis</h3>
              <ul class="space-y-2">
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">GDB / x64dbg</span>
                    <p class="text-gray-400 text-sm">Debugging and runtime analysis</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">ltrace / strace</span>
                    <p class="text-gray-400 text-sm">System and library call tracing</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">Frida / QBDI</span>
                    <p class="text-gray-400 text-sm">Dynamic instrumentation</p>
                  </div>
                </li>
              </ul>
            </div>

            <!-- Additional Tools -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <h3 class="text-xl font-semibold mb-4 text-purple-400">Utilities</h3>
              <ul class="space-y-2">
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">strings / binwalk</span>
                    <p class="text-gray-400 text-sm">Binary analysis utilities</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">objdump / readelf</span>
                    <p class="text-gray-400 text-sm">Binary file inspection</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">angr / Z3</span>
                    <p class="text-gray-400 text-sm">Symbolic execution and SMT solving</p>
                  </div>
                </li>
              </ul>
            </div>

            <!-- Hex Editors -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <h3 class="text-xl font-semibold mb-4 text-yellow-400">Hex Editors</h3>
              <ul class="space-y-2">
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">ImHex / 010 Editor</span>
                    <p class="text-gray-400 text-sm">Advanced hex editing</p>
                  </div>
                </li>
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <div>
                    <span class="text-gray-200 font-semibold">hexdump / xxd</span>
                    <p class="text-gray-400 text-sm">Command-line hex viewing</p>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <!-- Tips & Methodology -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">💡 Reverse Engineering Tips</h2>
            
            <div class="space-y-4">
              <div class="bg-gray-900 p-4 rounded-lg border-l-4 border-blue-600">
                <h3 class="font-semibold text-blue-400 mb-2">1. Start with static analysis</h3>
                <p class="text-gray-300 text-sm">Use tools like strings, file, and checksec to gather initial information before diving into disassembly.</p>
              </div>

              <div class="bg-gray-900 p-4 rounded-lg border-l-4 border-green-600">
                <h3 class="font-semibold text-green-400 mb-2">2. Understand the big picture</h3>
                <p class="text-gray-300 text-sm">Don't get lost in assembly details immediately. Map out the program flow, identify key functions, and understand the overall logic first.</p>
              </div>

              <div class="bg-gray-900 p-4 rounded-lg border-l-4 border-purple-600">
                <h3 class="font-semibold text-purple-400 mb-2">3. Use dynamic analysis wisely</h3>
                <p class="text-gray-300 text-sm">Debuggers are powerful, but use them strategically. Set breakpoints on interesting functions and watch how data flows through the program.</p>
              </div>

              <div class="bg-gray-900 p-4 rounded-lg border-l-4 border-yellow-600">
                <h3 class="font-semibold text-yellow-400 mb-2">4. Take notes and document</h3>
                <p class="text-gray-300 text-sm">Reverse engineering is complex. Keep detailed notes, rename functions/variables, and comment your findings as you progress.</p>
              </div>

              <div class="bg-gray-900 p-4 rounded-lg border-l-4 border-red-600">
                <h3 class="font-semibold text-red-400 mb-2">5. Don't fear anti-analysis</h3>
                <p class="text-gray-300 text-sm">Anti-debugging and obfuscation are meant to intimidate. Learn to recognize and bypass these techniques methodically.</p>
              </div>
            </div>
          </div>
        </section>

        <!-- Call to Action -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto mb-8">
          <div class="bg-gradient-to-r from-purple-900 to-pink-900 p-6 md:p-8 rounded-xl text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">🚀 Ready to extract some secrets?</h2>
            <p class="text-base md:text-lg text-gray-200 mb-6">
              Pick a challenge, fire up your favorite RE tools, and start dissecting!
            </p>
            <a href="#available-challenges" class="inline-block bg-white text-purple-900 px-8 py-3 rounded-lg font-semibold hover:bg-gray-200 transition">
              Browse Challenges
            </a>
          </div>
        </section>
  
      </main>
    </div>
  </div>
</body>
</html>
