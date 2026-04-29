---
layout: default
---

<!-- HERO -->
<section class="py-20">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-10 items-center">

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

      <!-- ROTATING ROLE -->
      <div class="text-2xl font-semibold mb-4">
        I'm looking for:
        <span id="rotating-role" class="text-brand transition duration-300">
          Data Analyst
        </span>
      </div>

      <p class="text-muted mb-6">
        MSc Data Analytics candidate focused on Business Intelligence,
        analytics, and consulting-driven problem solving. I translate
        complex data into actionable business insights.
      </p>

      <a href="#projects" class="px-6 py-3 bg-gradient-to-r from-brand to-accent rounded-full font-bold">
        View My Work
      </a>
    </div>

    <div class="flex justify-center">
      <div class="w-72 h-72 rounded-full bg-gradient-to-r from-brand to-accent flex items-center justify-center text-6xl">
        👨‍💻
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="py-20 border-t border-border">
  <div class="max-w-5xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-6">About Me</h2>

    <p class="text-muted leading-relaxed">
      I am an MSc Data Analytics student with a strong focus on Business Intelligence,
      Business Analytics, and consulting-driven problem solving. I combine technical
      expertise with business understanding to deliver data-driven insights that
      support decision-making.
    </p>

    <p class="text-muted mt-4 leading-relaxed">
      My experience includes working with tools such as Tableau, Power BI, Python,
      SQL, and Salesforce, with practical exposure to analytics, CRM systems,
      and process improvement in real-world environments including retail and
      financial services.
    </p>

  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="py-20 border-t border-border">
  <div class="max-w-6xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Skills</h2>

    <div class="grid md:grid-cols-3 gap-6">

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">Programming & Data</h3>
        <p class="text-muted">Python, Pandas, NumPy, Scikit-learn, R</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">BI & Visualisation</h3>
        <p class="text-muted">Tableau, Power BI, KPI dashboards, storytelling</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">Databases</h3>
        <p class="text-muted">MySQL, PostgreSQL, ETL, data cleaning</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">CRM & Tools</h3>
        <p class="text-muted">Salesforce, Jupyter, VS Code, GitHub</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">Cloud</h3>
        <p class="text-muted">Microsoft Azure fundamentals, pipelines</p>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold mb-3 text-accent">Business Skills</h3>
        <p class="text-muted">Stakeholder engagement, requirements, process optimisation</p>
      </div>

    </div>

  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="py-20 border-t border-border">
  <div class="max-w-5xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Experience</h2>

    <div class="space-y-6">

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold">Lab Assistant – National College of Ireland</h3>
        <p class="text-sm text-muted mb-2">2026 – Present</p>
        <ul class="text-muted text-sm">
          <li>• Supported 70+ students in AI/ML, BI, and data analysis modules</li>
          <li>• Guided machine learning workflows using Python</li>
          <li>• Assisted Tableau dashboard development</li>
        </ul>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold">International Peer Mentor – NCI</h3>
        <p class="text-sm text-muted mb-2">2025 – Present</p>
        <ul class="text-muted text-sm">
          <li>• Facilitated onboarding for 100+ students</li>
          <li>• Improved engagement and communication flow</li>
        </ul>
      </div>

      <div class="bg-panel p-6 rounded-xl border border-border">
        <h3 class="font-bold">Data Assistant Intern – City Holdings</h3>
        <p class="text-sm text-muted mb-2">2024</p>
        <ul class="text-muted text-sm">
          <li>• Analysed operational data using SQL and Excel</li>
          <li>• Produced reports supporting decision-making</li>
        </ul>
      </div>

    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="py-20 border-t border-border">
  <div class="max-w-6xl mx-auto px-4">

    <h2 class="text-3xl font-bold mb-10">Projects</h2>

    <div class="grid md:grid-cols-2 gap-6">

      {% for project in site.data.projects %}
      <div class="bg-panel border border-border p-6 rounded-xl">

        <h3 class="text-xl font-bold mb-2">{{ project.title }}</h3>
        <p class="text-muted mb-4">{{ project.description }}</p>

      </div>
      {% endfor %}

    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="py-20 border-t border-border">
  <div class="max-w-xl mx-auto text-center px-4">

    <h2 class="text-3xl font-bold mb-6">Contact</h2>

    <p class="text-muted mb-4">
      Email: kmpshinn@gmail.com
    </p>

    <a href="#" class="text-accent">
      LinkedIn
    </a>

  </div>
</section>
