---
title: "💣 Crackme"
permalink: /ctf/crackme/
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
        <header class="bg-gradient-to-r from-red-900 to-orange-900 py-12 md:py-16 text-center px-4 rounded-lg mt-4 lg:mt-0">
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2 mb-4">💣 Crackme</h1>
          <p class="mt-4 text-base md:text-lg text-gray-200 px-2">Bypass protection mechanisms in homemade binaries</p>
          <div class="mt-6 inline-block bg-orange-600 text-white px-6 py-3 rounded-full font-semibold">
            Test your cracking skills
          </div>
        </header>

        <!-- Introduction -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">🔓 What is a Crackme?</h2>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              A <strong class="text-red-400">Crackme</strong> is a small program designed specifically to test your reverse engineering and software cracking abilities. The goal is simple: bypass the protection mechanism, find the correct password/serial, or patch the binary to unlock functionality.
            </p>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              Unlike CTF challenges, crackmes are often:
            </p>
            <ul class="space-y-2 mb-4">
              <li class="flex items-start">
                <span class="text-red-400 mr-3">•</span>
                <span class="text-gray-300"><strong>Educational:</strong> Designed to teach specific RE concepts</span>
              </li>
              <li class="flex items-start">
                <span class="text-red-400 mr-3">•</span>
                <span class="text-gray-300"><strong>Progressive:</strong> Start simple, gradually increase in complexity</span>
              </li>
              <li class="flex items-start">
                <span class="text-red-400 mr-3">•</span>
                <span class="text-gray-300"><strong>Focused:</strong> Each crackme usually highlights one or two techniques</span>
              </li>
              <li class="flex items-start">
                <span class="text-red-400 mr-3">•</span>
                <span class="text-gray-300"><strong>Custom-made:</strong> Unique binaries with creative protection schemes</span>
              </li>
            </ul>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed">
              My collection includes both classic crackmes and custom challenges I've created to help you master specific reverse engineering techniques.
            </p>
          </div>
        </section>

        <!-- Crackme Types -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">🎨 Crackme Categories</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-blue-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🔑</div>
              <h3 class="text-lg font-semibold mb-2 text-blue-400">Serial/KeyGen</h3>
              <p class="text-gray-400 text-sm">Find the algorithm to generate valid serial numbers or registration keys</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-purple-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🔒</div>
              <h3 class="text-lg font-semibold mb-2 text-purple-400">Password Verification</h3>
              <p class="text-gray-400 text-sm">Reverse engineer the password checking mechanism to find the correct password</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-green-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🩹</div>
              <h3 class="text-lg font-semibold mb-2 text-green-400">Binary Patching</h3>
              <p class="text-gray-400 text-sm">Modify the executable to bypass checks or unlock hidden features</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-yellow-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🛡️</div>
              <h3 class="text-lg font-semibold mb-2 text-yellow-400">Anti-Tampering</h3>
              <p class="text-gray-400 text-sm">Bypass integrity checks, debugger detection, and anti-modification protections</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-red-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🧮</div>
              <h3 class="text-lg font-semibold mb-2 text-red-400">Algorithm Reverse</h3>
              <p class="text-gray-400 text-sm">Understand and replicate complex validation algorithms</p>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl border-l-4 border-orange-600 hover:shadow-xl transition">
              <div class="text-4xl mb-3">🎭</div>
              <h3 class="text-lg font-semibold mb-2 text-orange-400">Obfuscated</h3>
              <p class="text-gray-400 text-sm">Deal with code obfuscation, string encryption, and control flow flattening</p>
            </div>
          </div>
        </section>

        <!-- Difficulty Levels -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center">📊 Difficulty Progression</h2>
          
          <div class="space-y-4">
            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">⭐</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-green-400">Level 1 - Newbie</h3>
                <p class="text-gray-400">Simple password comparison, basic string checks. Perfect for learning your first RE tools.</p>
                <div class="mt-2 text-sm text-gray-500">Tools: strings, ltrace, basic debugger</div>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">⭐⭐</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-blue-400">Level 2 - Beginner</h3>
                <p class="text-gray-400">Simple encoding/decoding, XOR operations, basic mathematical checks.</p>
                <div class="mt-2 text-sm text-gray-500">Tools: IDA/Ghidra, GDB/x64dbg</div>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">⭐⭐⭐</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-yellow-400">Level 3 - Intermediate</h3>
                <p class="text-gray-400">Custom algorithms, serial validation, basic anti-debugging tricks.</p>
                <div class="mt-2 text-sm text-gray-500">Tools: Advanced disassembler features, scripting</div>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">⭐⭐⭐⭐</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-orange-400">Level 4 - Advanced</h3>
                <p class="text-gray-400">Strong obfuscation, VM protection, sophisticated anti-tampering mechanisms.</p>
                <div class="mt-2 text-sm text-gray-500">Tools: Symbolic execution, custom scripts, patience</div>
              </div>
            </div>

            <div class="bg-gray-800 p-6 rounded-xl flex items-start">
              <div class="text-3xl mr-4">⭐⭐⭐⭐⭐</div>
              <div class="flex-1">
                <h3 class="text-xl font-semibold mb-2 text-red-400">Level 5 - Expert</h3>
                <p class="text-gray-400">Multiple protection layers, custom packers, hardcore anti-analysis. For experienced reversers only.</p>
                <div class="mt-2 text-sm text-gray-500">Tools: Everything in your arsenal + creativity</div>
              </div>
            </div>
          </div>
        </section>

        <!-- Available Crackmes -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-red-600 pl-4">🎮 Available Crackmes</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            {% assign crackmes = site.categories.crackme %}
            {% if crackmes.size > 0 %}
              {% for post in crackmes %}
              <article class="bg-gray-800 p-6 rounded-xl shadow hover:shadow-xl transition border-l-4 
                {% if post.level == '1' or post.level == 1 %}border-green-600
                {% elsif post.level == '2' or post.level == 2 %}border-blue-600
                {% elsif post.level == '3' or post.level == 3 %}border-yellow-600
                {% elsif post.level == '4' or post.level == 4 %}border-orange-600
                {% else %}border-red-600{% endif %}">
                
                <div class="flex items-center justify-between mb-3 flex-wrap gap-2">
                  <h3 class="text-xl md:text-2xl font-semibold">
                    <a href="{{ post.url | relative_url }}" class="hover:text-red-400 transition">{{ post.title }}</a>
                  </h3>
                  {% if post.level %}
                  <span class="
                    {% if post.level == '1' or post.level == 1 %}bg-green-600
                    {% elsif post.level == '2' or post.level == 2 %}bg-blue-600
                    {% elsif post.level == '3' or post.level == 3 %}bg-yellow-600
                    {% elsif post.level == '4' or post.level == 4 %}bg-orange-600
                    {% else %}bg-red-600{% endif %}
                    text-white px-3 py-1 rounded-full text-xs font-semibold">
                    Level {{ post.level }}
                  </span>
                  {% endif %}
                </div>

                {% if post.crackme_type %}
                <div class="mb-3">
                  <span class="bg-gray-700 text-gray-300 px-2 py-1 rounded text-xs mr-2">{{ post.crackme_type }}</span>
                  {% if post.platform %}
                  <span class="bg-gray-700 text-gray-300 px-2 py-1 rounded text-xs">{{ post.platform }}</span>
                  {% endif %}
                </div>
                {% endif %}

                {% if post.techniques %}
                <div class="mb-3">
                  <span class="text-gray-400 text-sm">Techniques: </span>
                  <span class="text-blue-400 text-sm">{{ post.techniques }}</span>
                </div>
                {% endif %}

                {% if post.excerpt %}
                <p class="text-gray-400 mb-4 text-sm">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
                {% endif %}

                <div class="flex items-center justify-between">
                  <div class="flex gap-3">
                    <a href="{{ post.url | relative_url }}" class="text-red-400 hover:text-red-300 text-sm font-semibold">
                      Download →
                    </a>
                    {% if post.solution %}
                    <a href="{{ post.solution }}" class="text-green-400 hover:text-green-300 text-sm font-semibold">
                      Solution →
                    </a>
                    {% endif %}
                  </div>
                  <span class="text-sm text-gray-500">📅 {{ post.date | date: "%b %Y" }}</span>
                </div>
              </article>
              {% endfor %}
            {% else %}
              <div class="col-span-2 bg-gray-800 p-8 rounded-xl text-center">
                <div class="text-6xl mb-4">💣</div>
                <p class="text-xl text-gray-400 mb-4">No crackmes available yet</p>
                <p class="text-gray-500">Custom crackmes are coming soon. Stay tuned!</p>
              </div>
            {% endif %}
          </div>
        </section>

        <!-- Solving Approach -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-8 border-l-4 border-orange-600 pl-4">🎯 Cracking Methodology</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <!-- Reconnaissance -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <div class="flex items-center mb-4">
                <span class="text-3xl mr-3">1️⃣</span>
                <h3 class="text-xl font-semibold text-blue-400">Reconnaissance</h3>
              </div>
              <ul class="space-y-2 text-sm text-gray-300">
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <span>Run <code class="bg-gray-900 px-2 py-1 rounded">file</code> to identify binary type</span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <span>Check for protections with <code class="bg-gray-900 px-2 py-1 rounded">checksec</code></span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <span>Look for interesting strings</span>
                </li>
                <li class="flex items-start">
                  <span class="text-blue-400 mr-2">▸</span>
                  <span>Run the binary to understand behavior</span>
                </li>
              </ul>
            </div>

            <!-- Static Analysis -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <div class="flex items-center mb-4">
                <span class="text-3xl mr-3">2️⃣</span>
                <h3 class="text-xl font-semibold text-purple-400">Static Analysis</h3>
              </div>
              <ul class="space-y-2 text-sm text-gray-300">
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <span>Load in IDA Pro or Ghidra</span>
                </li>
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <span>Locate main/entry point</span>
                </li>
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <span>Identify validation functions</span>
                </li>
                <li class="flex items-start">
                  <span class="text-purple-400 mr-2">▸</span>
                  <span>Analyze algorithm logic</span>
                </li>
              </ul>
            </div>

            <!-- Dynamic Analysis -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <div class="flex items-center mb-4">
                <span class="text-3xl mr-3">3️⃣</span>
                <h3 class="text-xl font-semibold text-green-400">Dynamic Analysis</h3>
              </div>
              <ul class="space-y-2 text-sm text-gray-300">
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <span>Set breakpoints on key functions</span>
                </li>
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <span>Trace execution with debugger</span>
                </li>
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <span>Monitor memory changes</span>
                </li>
                <li class="flex items-start">
                  <span class="text-green-400 mr-2">▸</span>
                  <span>Use ltrace/strace for syscalls</span>
                </li>
              </ul>
            </div>

            <!-- Solution -->
            <div class="bg-gray-800 p-6 rounded-xl">
              <div class="flex items-center mb-4">
                <span class="text-3xl mr-3">4️⃣</span>
                <h3 class="text-xl font-semibold text-yellow-400">Solution</h3>
              </div>
              <ul class="space-y-2 text-sm text-gray-300">
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <span>Write a keygen if needed</span>
                </li>
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <span>Create a patch if required</span>
                </li>
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <span>Extract the valid password</span>
                </li>
                <li class="flex items-start">
                  <span class="text-yellow-400 mr-2">▸</span>
                  <span>Document your solution</span>
                </li>
              </ul>
            </div>
          </div>
        </section>

        <!-- Tools -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">🔧 Essential Cracking Tools</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <h3 class="text-lg font-semibold mb-3 text-blue-400">Disassemblers</h3>
                <ul class="space-y-1 text-sm text-gray-300">
                  <li>• IDA Pro / Ghidra / Binary Ninja</li>
                  <li>• radare2 / Cutter</li>
                  <li>• objdump / Hopper</li>
                </ul>
              </div>

              <div>
                <h3 class="text-lg font-semibold mb-3 text-green-400">Debuggers</h3>
                <ul class="space-y-1 text-sm text-gray-300">
                  <li>• GDB (with GEF/pwndbg)</li>
                  <li>• x64dbg / OllyDbg</li>
                  <li>• WinDbg / LLDB</li>
                </ul>
              </div>

              <div>
                <h3 class="text-lg font-semibold mb-3 text-purple-400">Hex Editors</h3>
                <ul class="space-y-1 text-sm text-gray-300">
                  <li>• ImHex / 010 Editor</li>
                  <li>• HxD / Hex Fiend</li>
                  <li>• xxd / hexdump</li>
                </ul>
              </div>

              <div>
                <h3 class="text-lg font-semibold mb-3 text-yellow-400">Utilities</h3>
                <ul class="space-y-1 text-sm text-gray-300">
                  <li>• strings / file / checksec</li>
                  <li>• ltrace / strace</li>
                  <li>• angr / Z3 solver</li>
                </ul>
              </div>
            </div>
          </div>
        </section>

        <!-- Rules -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <h2 class="text-2xl md:text-3xl font-bold mb-6">📋 Crackme Rules</h2>
            
            <div class="space-y-4">
              <div class="flex items-start">
                <span class="text-green-400 text-2xl mr-4">✓</span>
                <div>
                  <h3 class="font-semibold text-green-400 mb-1">Multiple solutions welcome</h3>
                  <p class="text-gray-400 text-sm">Patch it, keygen it, or brute-force it - any working solution counts!</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-green-400 text-2xl mr-4">✓</span>
                <div>
                  <h3 class="font-semibold text-green-400 mb-1">Learn and share</h3>
                  <p class="text-gray-400 text-sm">Share your approach, tools, and techniques with the community.</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-blue-400 text-2xl mr-4">ℹ️</span>
                <div>
                  <h3 class="font-semibold text-blue-400 mb-1">Check solutions after solving</h3>
                  <p class="text-gray-400 text-sm">Try to solve it yourself first, then compare with the official solution.</p>
                </div>
              </div>

              <div class="flex items-start">
                <span class="text-yellow-400 text-2xl mr-4">⚠️</span>
                <div>
                  <h3 class="font-semibold text-yellow-400 mb-1">For educational purposes only</h3>
                  <p class="text-gray-400 text-sm">These skills are for learning. Never use them illegally on real software.</p>
                </div>
              </div>
            </div>
          </div>
        </section>

        <!-- Call to Action -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto mb-8">
          <div class="bg-gradient-to-r from-red-900 to-orange-900 p-6 md:p-8 rounded-xl text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">💥 Ready to crack some code?</h2>
            <p class="text-base md:text-lg text-gray-200 mb-6">
              Pick a crackme, fire up your tools, and show those protections who's boss!
            </p>
            <a href="#available-crackmes" class="inline-block bg-white text-red-900 px-8 py-3 rounded-lg font-semibold hover:bg-gray-200 transition">
              Browse Crackmes
            </a>
          </div>
        </section>
  
      </main>
    </div>
  </div>
</body>
</html>
