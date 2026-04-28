---
layout: default
---

<section class="py-20">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-10 items-center">

    <div>
      <p class="text-brand-2 uppercase text-sm font-bold mb-4">
        AVAILABLE FOR ANALYST ROLES
      </p>

      <h1 class="text-5xl font-extrabold mb-4">
        Kyaw May Pyone Shinn
      </h1>

      <p class="text-xl text-muted mb-4 font-semibold">
        Data Analyst • Business Analyst • BI Specialist
      </p>

      <p class="text-muted mb-6">
        I transform raw data into actionable business insights using analytics,
        machine learning, and business intelligence tools.
      </p>

      <div class="flex gap-4">
        <a href="#projects" class="px-6 py-3 rounded-full bg-gradient-to-r from-brand to-accent text-white font-bold">
          View Projects
        </a>
      </div>
    </div>

    <div class="bg-panel border border-border rounded-xl2 p-6 shadow-glass">
      <p class="text-brand-2 text-xs uppercase">Core Stack</p>
      <p>SQL • Power BI • Python</p>
    </div>

  </div>
</section>

<section id="skills" class="py-20">
  <div class="max-w-6xl mx-auto px-4">
    <h2 class="text-3xl font-bold mb-6">Skills</h2>

    <div class="flex flex-wrap gap-3">
      {% for skill in site.data.profile.skills %}
      <span class="px-4 py-2 bg-brand/10 border border-brand/20 rounded-full">
        {{ skill }}
      </span>
      {% endfor %}
    </div>
  </div>
</section>

<section id="projects" class="py-20">
  <div class="max-w-6xl mx-auto px-4">
    <h2 class="text-3xl font-bold mb-10">Projects</h2>

    <div class="grid md:grid-cols-2 gap-6">
      {% for project in site.data.projects %}
      <div class="bg-panel border border-border p-6 rounded-xl2 shadow-glass">

        <div class="flex justify-between text-xs text-brand-2 mb-2">
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
