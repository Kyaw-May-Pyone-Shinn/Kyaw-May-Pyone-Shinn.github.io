---
layout: default
---

{% assign profile = site.data.profile %}

<!-- HERO -->
<section id="home" class="min-h-screen flex items-center">
  <div class="max-w-7xl mx-auto px-5 grid lg:grid-cols-2 gap-12 items-center">

    <!-- LEFT -->
    <div>

      <p class="section-label mb-6">Hello there</p>

      <h1 class="text-5xl md:text-7xl font-black leading-tight mb-4">
        Hi, I’m <br>
        <span class="gradient-text">Kyaw May</span><br>
        Pyone Shinn
      </h1>

      <div class="text-xl md:text-2xl mb-6 font-semibold">
        I’m a
        <span id="rotating-role" class="text-primary">Data Analyst</span>
      </div>

      <p class="text-muted max-w-xl mb-6">
        I build analytics, dashboards, and CRM-driven business solutions
        that help organisations make data-driven decisions.
      </p>

      <div class="flex flex-wrap gap-4 mb-6">
        <a href="#projects" class="px-6 py-3 bg-gradient-to-r from-primary to-secondary rounded-full font-bold shadow-glow">
          Explore Projects
        </a>

        <a href="#contact" class="px-6 py-3 border border-border rounded-full font-bold">
          Contact Me
        </a>
      </div>

      <div class="flex gap-4 text-sm">
        <a href="https://www.linkedin.com/in/kyaw-may-pyone-shinn/" class="px-4 py-2 border border-border rounded-full hover:border-primary">
          LinkedIn
        </a>

        <a href="https://github.com/Kyaw-May-Pyone-Shinn" class="px-4 py-2 border border-border rounded-full hover:border-primary">
          GitHub
        </a>
      </div>

    </div>

    <!-- RIGHT -->
    <div class="relative">
      <div class="glass rounded-3xl p-8">

        <div class="w-40 h-40 mx-auto rounded-full bg-gradient-to-br from-primary to-secondary flex items-center justify-center text-5xl mb-8">
          📊
        </div>

        <div class="grid grid-cols-2 gap-4">

          <div class="bg-white/5 p-4 rounded-xl">
            <p class="text-2xl font-bold text-primary">100+</p>
            <p class="text-xs text-muted">students mentored</p>
          </div>

          <div class="bg-white/5 p-4 rounded-xl">
            <p class="text-2xl font-bold text-primary">70+</p>
            <p class="text-xs text-muted">weekly lab support</p>
          </div>

          <div class="bg-white/5 p-4 rounded-xl">
            <p class="text-2xl font-bold text-primary">R² 0.85</p>
            <p class="text-xs text-muted">forecasting model</p>
          </div>

          <div class="bg-white/5 p-4 rounded-xl">
            <p class="text-2xl font-bold text-primary">30–45s</p>
            <p class="text-xs text-muted">process improvement</p>
          </div>

        </div>

      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="min-h-screen border-t border-border py-24">
  <div class="max-w-5xl mx-auto px-5">

    <h2 class="text-4xl font-black mb-6">About Me</h2>

    <p class="text-muted mb-4">
      I am an MSc Data Analytics candidate specialising in Business Intelligence,
      Business Analytics, and consulting-driven problem solving. I combine technical
      expertise with stakeholder-oriented thinking to translate complex data into
      actionable business insights.
    </p>

    <p class="text-muted">
      My experience spans analytics, dashboards, CRM systems, and process improvement
      across retail and financial services environments using Tableau, Power BI,
      Python, SQL, and Salesforce.
    </p>

  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="min-h-screen border-t border-border py-24">
  <div class="max-w-6xl mx-auto px-5">

    <h2 class="text-4xl font-black mb-10">Skills</h2>

    <div class="grid md:grid-cols-3 gap-6">

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">Programming</h3>
        <p class="text-muted">Python, R, Pandas, NumPy</p>
      </div>

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">BI & Visualisation</h3>
        <p class="text-muted">Tableau, Power BI, Dashboards</p>
      </div>

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">Database</h3>
        <p class="text-muted">MySQL, PostgreSQL, ETL</p>
      </div>

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">CRM</h3>
        <p class="text-muted">Salesforce, Reporting</p>
      </div>

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">Cloud</h3>
        <p class="text-muted">Azure Fundamentals</p>
      </div>

      <div class="glass p-6 rounded-xl">
        <h3 class="text-primary font-bold mb-2">Languages</h3>
        <p class="text-muted">English, Burmese, Korean, Chinese</p>
      </div>

    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="min-h-screen border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5">

    <h2 class="text-4xl font-black mb-12">Projects</h2>

    <div class="grid lg:grid-cols-2 gap-6">

      {% for project in site.data.projects %}
      <div class="glass rounded-3xl p-6 hover:-translate-y-1 transition">

        <h3 class="text-xl font-extrabold mb-2">
          {{ project.title }}
        </h3>

        <p class="text-primary text-sm mb-3">
          {{ project.type }}
        </p>

        <p class="text-sm text-muted mb-2">
          <strong>What:</strong> {{ project.summary }}
        </p>

        <p class="text-sm text-muted mb-2">
          <strong>How:</strong> {{ project.approach }}
        </p>

        <p class="text-sm text-muted mb-4">
          <strong>Impact:</strong> {{ project.outcome }}
        </p>

        <div class="flex flex-wrap gap-2 mb-4">
          {% for tech in project.tech %}
          <span class="px-3 py-1 bg-primary/10 border border-primary/20 rounded-full text-xs">
            {{ tech }}
          </span>
          {% endfor %}
        </div>

        <a href="{{ project.link }}" class="text-primary font-bold text-sm">
          View Project →
        </a>

      </div>
      {% endfor %}

    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="min-h-screen flex items-center border-t border-border py-24">
  <div class="max-w-xl mx-auto text-center">

    <h2 class="text-4xl font-black mb-6">Contact</h2>

    <p class="text-muted mb-4">kmpshinn@gmail.com</p>

    <div class="flex justify-center gap-6">
      <a href="https://www.linkedin.com/in/kyaw-may-pyone-shinn/" class="text-primary font-bold">
        LinkedIn
      </a>

      <a href="https://github.com/Kyaw-May-Pyone-Shinn" class="text-primary font-bold">
        GitHub
      </a>
    </div>

  </div>
</section>
