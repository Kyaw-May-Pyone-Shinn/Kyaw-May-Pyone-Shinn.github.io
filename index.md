---
layout: default
---

{% assign profile = site.data.profile %}

<!-- HERO -->
<section id="home" class="min-h-screen flex items-center">
  <div class="max-w-7xl mx-auto px-5 grid lg:grid-cols-2 gap-12 items-center">

    <div>
      <p class="section-label mb-6">Data • Insights • Impact</p>

      <h1 class="text-5xl md:text-7xl font-black leading-tight mb-6">
        Hi, I’m <br>
        <span class="gradient-text">{{ profile.name }}</span>
      </h1>

      <div class="glass rounded-3xl p-5 mb-7 max-w-2xl">
        <p class="text-lg md:text-2xl font-bold">
          I’m looking for a
          <span id="rotating-role" class="text-primary transition-opacity duration-300">Data Analyst</span>
          role.
        </p>
        <p class="text-muted mt-3">
          I build analytics, dashboards, CRM reporting, and decision-support solutions that connect data with business action.
        </p>
      </div>

      <div class="flex flex-wrap gap-4">
        <a href="#projects" class="px-7 py-3 rounded-full bg-gradient-to-r from-primary via-secondary to-accent font-extrabold shadow-glow">
          Explore Projects
        </a>
        <a href="#contact" class="px-7 py-3 rounded-full border border-border hover:border-primary transition font-bold">
          Contact Me
        </a>
        <a href="{{ profile.linkedin }}" target="_blank" class="px-7 py-3 rounded-full border border-border hover:border-primary transition font-bold">
          LinkedIn
        </a>
      </div>
    </div>

    <div class="relative">
      <div class="absolute inset-0 bg-gradient-to-br from-primary/30 to-secondary/20 blur-3xl rounded-full"></div>

      <div class="relative glass rounded-[2rem] p-8">
        <div class="w-44 h-44 mx-auto rounded-full bg-gradient-to-br from-primary via-secondary to-accent flex items-center justify-center text-6xl shadow-glow mb-8">
          📊
        </div>

        <div class="grid grid-cols-2 gap-4">
          {% for item in profile.highlights %}
          <div class="rounded-2xl bg-white/5 border border-border p-4">
            <p class="text-2xl font-black text-primary">{{ item.value }}</p>
            <p class="text-xs text-muted mt-1">{{ item.label }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="min-h-screen flex items-center border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5 grid lg:grid-cols-3 gap-8">

    <div>
      <p class="section-label mb-5">About</p>
      <h2 class="text-4xl md:text-5xl font-black mb-6">Business-minded analyst with technical depth.</h2>
      <p class="text-muted">
        My portfolio is built around one idea: analytics should not stop at charts. It should help people make better decisions.
      </p>
    </div>

    <div class="lg:col-span-2 space-y-5">
      {% for paragraph in profile.summary %}
      <div class="glass rounded-3xl p-6">
        <p class="text-muted leading-relaxed">{{ paragraph }}</p>
      </div>
      {% endfor %}

      <div class="grid md:grid-cols-2 gap-5">
        <div class="glass rounded-3xl p-6">
          <h3 class="font-extrabold text-primary mb-3">What I focus on</h3>
          <p class="text-muted">
            Business Intelligence, dashboard design, KPI tracking, CRM reporting, forecasting, stakeholder communication, and process improvement.
          </p>
        </div>

        <div class="glass rounded-3xl p-6">
          <h3 class="font-extrabold text-primary mb-3">How I work</h3>
          <p class="text-muted">
            I start with business questions, understand the stakeholder need, structure the data, build the analysis, and communicate insights clearly.
          </p>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="min-h-screen border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5">

    <p class="section-label mb-5">Skills</p>
    <h2 class="text-4xl md:text-5xl font-black mb-12">Technical, analytical, and consulting capability.</h2>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
      {% for skill in profile.technical_skills %}
      <div class="glass rounded-3xl p-6 hover:-translate-y-1 transition">
        <h3 class="text-primary font-extrabold mb-3">{{ skill.category }}</h3>
        <p class="text-muted leading-relaxed">{{ skill.items }}</p>
      </div>
      {% endfor %}
    </div>

    <div class="grid lg:grid-cols-2 gap-6">
      <div class="glass rounded-3xl p-6">
        <h3 class="text-2xl font-extrabold mb-5">Languages</h3>
        <div class="flex flex-wrap gap-3">
          {% for language in profile.languages %}
          <span class="px-4 py-2 rounded-full bg-primary/10 border border-primary/25 text-soft text-sm">
            {{ language }}
          </span>
          {% endfor %}
        </div>
      </div>

      <div class="glass rounded-3xl p-6">
        <h3 class="text-2xl font-extrabold mb-5">Education</h3>
        <div class="space-y-4">
          {% for edu in profile.education %}
          <div class="border-l-2 border-primary pl-4">
            <p class="font-bold">{{ edu.school }}</p>
            <p class="text-muted text-sm">{{ edu.degree }}</p>
            <p class="text-primary text-sm font-semibold">{{ edu.result }} {{ edu.year }}</p>
          </div>
          {% endfor %}
        </div>
      </div>
    </div>

    <div class="glass rounded-3xl p-6 mt-6">
      <h3 class="text-2xl font-extrabold mb-5">Certificates</h3>
      <div class="grid md:grid-cols-2 gap-3">
        {% for cert in profile.certificates %}
        <p class="text-muted">• {{ cert }}</p>
        {% endfor %}
      </div>
    </div>

  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="min-h-screen border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5">

    <p class="section-label mb-5">Experience</p>
    <h2 class="text-4xl md:text-5xl font-black mb-12">Practical experience across education, retail, and banking.</h2>

    <div class="relative space-y-8">
      {% for job in site.data.experience %}
      <article class="glass rounded-3xl p-7">
        <div class="flex flex-wrap justify-between gap-4 mb-4">
          <div>
            <h3 class="text-2xl font-extrabold">{{ job.role }}</h3>
            <p class="text-primary font-bold">{{ job.company }}</p>
          </div>
          <div class="text-right">
            <p class="text-muted">{{ job.location }}</p>
            <p class="text-sm text-soft">{{ job.period }}</p>
          </div>
        </div>

        <p class="text-muted leading-relaxed mb-5">{{ job.description }}</p>

        <ul class="space-y-2 text-muted">
          {% for bullet in job.bullets %}
          <li class="flex gap-3">
            <span class="text-primary">◆</span>
            <span>{{ bullet }}</span>
          </li>
          {% endfor %}
        </ul>
      </article>
      {% endfor %}
    </div>

  </div>
</section>

<!-- LEADERSHIP -->
<section id="leadership" class="min-h-screen border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5">

    <p class="section-label mb-5">Leadership</p>
    <h2 class="text-4xl md:text-5xl font-black mb-12">Leadership, mentoring, and community impact.</h2>

    <div class="grid lg:grid-cols-2 gap-6">
      {% for item in site.data.leadership %}
      <article class="glass rounded-3xl p-7 hover:-translate-y-1 transition">
        <div class="flex justify-between gap-5 mb-4">
          <div>
            <h3 class="text-xl font-extrabold">{{ item.role }}</h3>
            <p class="text-primary font-bold">{{ item.organisation }}</p>
          </div>
          <p class="text-sm text-muted text-right">{{ item.period }}</p>
        </div>

        <p class="text-muted mb-5">{{ item.description }}</p>

        <ul class="space-y-2 text-muted text-sm">
          {% for bullet in item.bullets %}
          <li>• {{ bullet }}</li>
          {% endfor %}
        </ul>
      </article>
      {% endfor %}
    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="min-h-screen border-t border-border py-24">
  <div class="max-w-7xl mx-auto px-5">

    <p class="section-label mb-5">Projects</p>
    <h2 class="text-4xl md:text-5xl font-black mb-12">Portfolio projects with business value.</h2>

    <div class="grid lg:grid-cols-2 gap-8">
      {% for project in site.data.projects %}
      <article class="glass rounded-3xl p-7 hover:-translate-y-1 transition">
        <div class="flex flex-wrap justify-between gap-4 mb-4">
          <div>
            <p class="text-primary font-bold text-sm">{{ project.type }}</p>
            <h3 class="text-2xl font-extrabold mt-1">{{ project.title }}</h3>
          </div>
          <p class="text-sm text-muted">{{ project.period }}</p>
        </div>

        <p class="text-muted leading-relaxed mb-5">{{ project.summary }}</p>

        <div class="space-y-4 mb-6">
          <div>
            <h4 class="font-extrabold text-soft mb-1">Business Problem</h4>
            <p class="text-muted text-sm leading-relaxed">{{ project.problem }}</p>
          </div>

          <div>
            <h4 class="font-extrabold text-soft mb-1">Approach</h4>
            <p class="text-muted text-sm leading-relaxed">{{ project.approach }}</p>
          </div>

          <div>
            <h4 class="font-extrabold text-soft mb-1">Outcome</h4>
            <p class="text-muted text-sm leading-relaxed">{{ project.outcome }}</p>
          </div>
        </div>

        <div class="flex flex-wrap gap-2 mb-6">
          {% for tech in project.tech %}
          <span class="px-3 py-1 rounded-full bg-primary/10 border border-primary/25 text-xs text-soft">
            {{ tech }}
          </span>
          {% endfor %}
        </div>

        <a href="{{ project.link }}" target="_blank" class="text-primary font-extrabold">
          View Project →
        </a>
      </article>
      {% endfor %}
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="min-h-screen flex items-center border-t border-border py-24">
  <div class="max-w-4xl mx-auto px-5 text-center">

    <p class="section-label mb-5 justify-center">Contact</p>
    <h2 class="text-4xl md:text-5xl font-black mb-6">Let’s connect.</h2>

    <p class="text-muted max-w-2xl mx-auto mb-8">
      I am open to Data Analyst, Business Analyst, Business Intelligence, CRM analytics, and consulting-oriented graduate roles. I am especially interested in work that combines analytics, stakeholder communication, dashboards, and practical business impact.
    </p>

    <div class="glass rounded-3xl p-8">
      <p class="text-xl font-extrabold mb-2">{{ profile.email }}</p>
      <p class="text-muted mb-6">{{ profile.location }}</p>

      <div class="flex justify-center flex-wrap gap-4">
        <a href="{{ profile.linkedin }}" target="_blank" class="px-6 py-3 rounded-full bg-gradient-to-r from-primary to-secondary font-bold shadow-glow">
          LinkedIn
        </a>

        <a href="{{ profile.github }}" target="_blank" class="px-6 py-3 rounded-full border border-border hover:border-primary font-bold transition">
          GitHub
        </a>

        <a href="mailto:{{ profile.email }}" class="px-6 py-3 rounded-full border border-border hover:border-primary font-bold transition">
          Email Me
        </a>
      </div>
    </div>

  </div>
</section>
