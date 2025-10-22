---
permalink: /about/
title: "$ whoami"
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
          <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold px-2">$ whoami</h1>
          <p class="mt-4 text-base md:text-lg text-gray-400 px-2">Offensive security enthusiast, vulnerability researcher, and malware analyst</p>
        </header>

        <!-- Introduction -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              Hi there, curious hacker.
            </p>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-4">
              I'm passionate about <strong class="text-blue-400">offensive cyber security</strong>. I explore vulnerabilities, unexpected behaviors, obscure corners of Windows, Linux, networks, web apps and even malicious binaries we'd rather ignore.
            </p>
            <p class="text-base md:text-lg text-gray-300 leading-relaxed">
              I launched this blog to <strong class="text-blue-400">document my research</strong>, <strong class="text-blue-400">share techniques</strong>, and also <strong class="text-blue-400">create a trace</strong> of what fascinates me on a daily basis: the art of understanding a system to better exploit it.
            </p>
          </div>
        </section>

        <!-- My Playgrounds -->
        <section class="py-8 md:py-12 px-4 max-w-6xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 text-center">🎯 My playgrounds</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 md:gap-8">
            
            <!-- Pentest Web & Network -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🌐</span>
                <h3 class="text-xl md:text-2xl font-semibold">Pentest Web & Network</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                I spend time looking for SQL injections, XSS, RCE, privilege escalations or pivot techniques. Understanding how network and web stacks work is essential to better circumvent them.
              </p>
            </div>

            <!-- Reverse Engineering & Binary Exploitation -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">⚔️</span>
                <h3 class="text-xl md:text-2xl font-semibold">Reverse Engineering & Binary Exploitation</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                I like to disassemble executables, read assembler, understand the internal logic of a program and write my own exploits, sometimes starting from a simple memory bug.
              </p>
            </div>

            <!-- Malware Analysis -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🧪</span>
                <h3 class="text-xl md:text-2xl font-semibold">Malware Analysis</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                Static or dynamic analysis, I like to track down malicious behavior, understand persistence mechanisms, spot C2s and extract payloads from an obscure binary.
              </p>
            </div>

            <!-- Active Directory & Windows Internals -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🗂️</span>
                <h3 class="text-xl md:text-2xl font-semibold">Active Directory & Windows Internals</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                I delve into the bowels of Windows, its security mechanisms, from UAC to protocol abuse in Active Directory environments. Microsoft systems are a rich and complex terrain.
              </p>
            </div>

            <!-- Applied cryptography & CTF -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🧠</span>
                <h3 class="text-xl md:text-2xl font-semibold">Applied cryptography & CTF</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                Without being a crypto-math, I like to play with implementation errors, misused modes and faulty PRNGs. Especially in CTF challenges, where nothing is really what it seems.
              </p>
            </div>

            <!-- Linux & scripting -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🐧</span>
                <h3 class="text-xl md:text-2xl font-semibold">Linux & scripting</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                Bash, Python or custom tools, I automate, monitor and bypass. A good script is sometimes better than a big tool.
              </p>
            </div>

            <!-- Fun & Crackmes -->
            <div class="bg-gray-800 p-6 rounded-xl shadow">
              <div class="flex items-start mb-4">
                <span class="text-3xl mr-4">🎮</span>
                <h3 class="text-xl md:text-2xl font-semibold">Fun & Crackmes</h3>
              </div>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed">
                I like to code or solve small protected binaries. It's fun, cerebral, and it muscles the analysis.
              </p>
            </div>

          </div>
        </section>

        <!-- Why this blog -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto">
          <h2 class="text-2xl md:text-3xl font-bold mb-6 md:mb-8 text-center">👨‍💻 Why this blog?</h2>
          
          <div class="bg-gray-800 p-6 md:p-8 rounded-xl">
            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-6">
              Because I believe in <strong class="text-blue-400">making visible</strong> what is often hidden:
            </p>
            
            <ul class="space-y-3 mb-6">
              <li class="flex items-start">
                <span class="text-blue-400 mr-3 text-xl">•</span>
                <span class="text-gray-300">The methods behind the tools.</span>
              </li>
              <li class="flex items-start">
                <span class="text-blue-400 mr-3 text-xl">•</span>
                <span class="text-gray-300">The ideas behind the feats.</span>
              </li>
              <li class="flex items-start">
                <span class="text-blue-400 mr-3 text-xl">•</span>
                <span class="text-gray-300">And the mistakes behind the successes.</span>
              </li>
            </ul>

            <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-6">
              It's also a way of sharing with the community. If you find a loophole, a useful write-up, or want to propose a twisted challenge: <strong class="text-blue-400">let me know</strong>.
            </p>

            <div class="bg-gray-900 border-l-4 border-blue-600 p-4 rounded">
              <p class="text-base md:text-lg text-gray-300 leading-relaxed mb-2">
                💬 Whether you're a beginner or a seasoned red teamer, this blog is for you.
              </p>
              <p class="text-base md:text-lg text-gray-300 leading-relaxed">
                If you like to understand things in depth, you've come to the right place.
              </p>
            </div>
          </div>
        </section>

        <!-- Contact/Social (optionnel) -->
        <section class="py-8 md:py-12 px-4 max-w-4xl mx-auto mb-8">
          <div class="bg-gradient-to-r from-blue-900 to-purple-900 p-6 md:p-8 rounded-xl text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-4">📬 Get in touch</h2>
            <p class="text-base md:text-lg text-gray-300 mb-6">
              Want to collaborate, share ideas, or just chat about security?
            </p>
            <div class="flex justify-center gap-4 flex-wrap">
              <a href="https://github.com/s3d1p0x" target="_blank" class="bg-gray-800 hover:bg-gray-700 px-6 py-3 rounded-lg transition">
                <i class="fab fa-github"></i> GitHub
              </a>
              <a href="https://www.linkedin.com/in/quentin-auspitz-cybersecurity-pentest" target="_blank" class="bg-gray-800 hover:bg-gray-700 px-6 py-3 rounded-lg transition">
                <i class="fab fa-linkedin"></i> LinkedIn
              </a>
            </div>
          </div>
        </section>
  
      </main>
    </div>
  </div>
</body>
</html>
