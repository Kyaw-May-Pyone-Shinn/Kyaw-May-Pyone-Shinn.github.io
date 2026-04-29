---
layout: default
---

<!-- HERO -->
<section class="min-h-screen flex items-center">
  <div class="max-w-6xl mx-auto px-4">

    <h1 class="text-5xl font-extrabold mb-4">
      Kyaw May Pyone Shinn
    </h1>

    <div class="text-2xl mb-4">
      I'm looking for:
      <span id="rotating-role" class="text-brand">Data Analyst</span>
    </div>

    <p class="text-muted">
      MSc Data Analytics candidate focused on Business Intelligence and consulting-driven analytics.
    </p>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="min-h-screen flex items-center border-t border-border">
  <div class="max-w-4xl mx-auto px-4">
    <h2 class="text-3xl font-bold mb-6">About</h2>

    <p class="text-muted">
      MSc Data Analytics candidate with strong focus on BI, analytics, and consulting problem solving.
      Experienced in translating data into insights using Tableau, Python, SQL, and Salesforce.
    </p>
  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="min-h-screen flex items-center border-t border-border">
  <div class="max-w-6xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Skills</h2>

    <div class="grid md:grid-cols-2 gap-6">

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3">Technical</h3>
        <p>Python, R, SQL, Tableau, Power BI</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3">Languages</h3>
        <p>English, Burmese, Korean, Chinese</p>
      </div>

    </div>

  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="min-h-screen flex items-center border-t border-border">
  <div class="max-w-5xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Experience</h2>

    <div class="space-y-6">

      <div class="bg-panel p-6 rounded-xl border border-border">
        Lab Assistant – NCI
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        Peer Mentor – NCI
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        Data Intern – City Holdings
      </div>

    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="min-h-screen flex items-center border-t border-border">
  <div class="max-w-6xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Projects</h2>

    <div class="grid md:grid-cols-2 gap-6">
      {% for project in site.data.projects %}
      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold">{{ project.title }}</h3>
        <p class="text-muted">{{ project.description }}</p>
      </div>
      {% endfor %}
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="min-h-screen flex items-center border-t border-border">
  <div class="max-w-xl mx-auto text-center">

    <h2 class="text-3xl font-bold mb-6">Contact</h2>

    <p class="text-muted">kmpshinn@gmail.com</p>

    <div class="flex justify-center gap-6 mt-4">
      <a href="#" class="text-accent">LinkedIn</a>
      <a href="#" class="text-accent">GitHub</a>
    </div>

  </div>
</section>
