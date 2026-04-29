---
layout: default
---

<section class="py-20">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-10 items-center">

    <!-- LEFT -->
    <div>

      <p class="text-accent font-bold uppercase mb-4">
        DATA • INSIGHTS • IMPACT
      </p>

      <h1 class="text-5xl font-extrabold mb-4">
        Hi, I'm
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand to-accent">
          Kyaw May Pyone Shinn
        </span>
      </h1>

      <!-- 🔥 ROTATING ROLE -->
      <div class="text-2xl font-semibold mb-4">
        I'm looking for:
        <span id="rotating-role" class="text-brand transition duration-300">
          Data Analyst
        </span>
      </div>

      <p class="text-muted mb-6">
        I transform data into actionable insights, build intelligent systems,
        and help businesses make confident, data-driven decisions.
      </p>

      <a href="#projects" class="px-6 py-3 bg-gradient-to-r from-brand to-accent rounded-full font-bold">
        View My Work
      </a>

    </div>

    <!-- RIGHT -->
    <div class="flex justify-center">
      <div class="w-72 h-72 rounded-full bg-gradient-to-r from-brand to-accent flex items-center justify-center text-6xl">
        👨‍💻
      </div>
    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="py-20">
  <div class="max-w-6xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Projects</h2>

    <div class="grid md:grid-cols-2 gap-6">

      {% for project in site.data.projects %}
      <div class="bg-panel border border-border p-6 rounded-xl shadow-glass">

        <div class="flex justify-between text-xs text-accent mb-2">
          <span>{{ project.type }}</span>
          <span>{{ project.period }}</span>
        </div>

        <h3 class="text-xl font-bold mb-2">{{ project.title }}</h3>
        <p class="text-muted mb-4">{{ project.description }}</p>

        <ul class="text-sm text-muted mb-4">
          {% for item in project.impact %}
          <li>• {{ item }}</li>
          {% endfor %}
        </ul>

      </div>
      {% endfor %}

    </div>
  </div>
</section>
