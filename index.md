---
layout: default
---

{% assign profile = site.data.profile %}

<!-- HOME -->
<section id="home" class="min-h-[82vh] flex items-center">
  <div class="max-w-6xl mx-auto px-5 grid lg:grid-cols-2 gap-10 items-center">

    <div>
      <p class="section-kicker mb-5">Hello there</p>

      <h1 class="text-4xl md:text-5xl font-black leading-tight mb-4 text-ink">
        Hi, I’m <br>
        <span class="text-rose">Kyaw May</span> Pyone Shinn
      </h1>

      <p class="text-xl md:text-2xl font-bold mb-4 text-navy">
        I’m a <span id="rotating-role" class="text-rose role-fade">Data Analyst</span>
      </p>

      <p class="text-muted max-w-xl leading-relaxed mb-6">
        I build analytics, dashboards, CRM reporting, and decision-support solutions that help organisations make clear, confident, data-driven decisions.
      </p>

      <div class="flex flex-wrap gap-3 mb-5">
        <a href="#projects" class="px-5 py-2.5 rounded-full bg-rose text-white font-bold text-sm hover:bg-roseDark transition">
          Explore Projects
        </a>
        <a href="#contact" class="px-5 py-2.5 rounded-full border border-line bg-white font-bold text-sm hover:border-rose hover:text-rose transition">
          Contact Me
        </a>
      </div>

      <div class="flex flex-wrap gap-3 text-sm">
        <a href="{{ profile.linkedin }}" target="_blank" class="px-4 py-2 rounded-full bg-white border border-line text-muted hover:text-rose hover:border-rose transition">
          LinkedIn
        </a>
        <a href="{{ profile.github }}" target="_blank" class="px-4 py-2 rounded-full bg-white border border-line text-muted hover:text-rose hover:border-rose transition">
          GitHub
        </a>
        <a href="mailto:{{ profile.email }}" class="px-4 py-2 rounded-full bg-white border border-line text-muted hover:text-rose hover:border-rose transition">
          Email
        </a>
      </div>
    </div>

    <div class="card rounded-3xl p-7">
      <div class="flex items-center gap-5 mb-7">
        <div class="w-24 h-24 rounded-3xl bg-blush flex items-center justify-center text-4xl">
          📊
        </div>
        <div>
          <p class="text-sm section-kicker mb-1">Portfolio Focus</p>
          <h2 class="text-2xl font-black text-ink">BI, Analytics & Consulting</h2>
          <p class="text-muted text-sm mt-1">Turning data into practical business action.</p>
        </div>
      </div>

      <div class="grid grid-cols-2 gap-4">
        {% for item in profile.highlights %}
        <div class="rounded-2xl bg-slate-50 border border-line p-4">
          <p class="text-2xl font-black text-rose">{{ item.value }}</p>
          <p class="text-xs text-muted mt-1">{{ item.label }}</p>
        </div>
        {% endfor %}
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="border-t border-line py-16">
  <div class="max-w-6xl mx-auto px-5 grid lg:grid-cols-3 gap-8">

    <div>
      <p class="section-kicker mb-4">About</p>
      <h2 class="text-3xl md:text-4xl font-black leading-tight text-ink">
        Analytical, business-focused, and impact-driven.
      </h2>
    </div>

    <div class="lg:col-span-2 grid gap-4">
      {% for paragraph in profile.summary %}
      <div class="card rounded-2xl p-5">
        <p class="text-muted leading-relaxed">{{ paragraph }}</p>
      </div>
      {% endfor %}

      <div class="grid md:grid-cols-2 gap-4">
        <div class="card rounded-2xl p-5">
          <h3 class="font-black text-ink mb-2">What I focus on</h3>
          <p class="text-muted text-sm leading-relaxed">
            BI dashboards, CRM reporting, KPI design, forecasting, stakeholder communication, and process improvement.
          </p>
        </div>

        <div class="card rounded-2xl p-5">
          <h3 class="font-black text-ink mb-2">How I work</h3>
          <p class="text-muted text-sm leading-relaxed">
            I start with the business question, structure the data, build the analysis, and communicate insights clearly.
          </p>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="border-t border-line py-16">
  <div class="max-w-6xl mx-auto px-5">

    <p class="section-kicker mb-4">Skills</p>
    <h2 class="text-3xl md:text-4xl font-black mb-8 text-ink">Tools and capabilities</h2>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-4 mb-6">
      {% for skill in profile.technical_skills %}
      <div class="card rounded-2xl p-5 hover:-translate-y-1 transition">
        <h3 class="font-black text-rose mb-2">{{ skill.category }}</h3>
        <p class="text-muted text-sm leading-relaxed">{{ skill.items }}</p>
      </div>
      {% endfor %}
    </div>

    <div class="grid lg:grid-cols-2 gap-4">
      <div class="card rounded-2xl p-5">
        <h3 class="text-xl font-black mb-4">Languages</h3>
        <div class="flex flex-wrap gap-2">
          {% for language in profile.languages %}
          <span class="px-3 py-1.5 rounded-full bg-blush text-roseDark text-sm font-semibold">
            {{ language }}
          </span>
          {% endfor %}
        </div>
      </div>

      <div class="card rounded-2xl p-5">
        <h3 class="text-xl font-black mb-4">Certificates</h3>
        <div class="grid gap-2">
          {% for cert in profile.certificates %}
          <p class="text-muted text-sm">• {{ cert }}</p>
          {% endfor %}
        </div>
      </div>
    </div>

  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="border-t border-line py-16">
  <div class="max-w-6xl mx-auto px-5">

    <p class="section-kicker mb-4">Experience</p>
    <h2 class="text-3xl md:text-4xl font-black mb-8 text-ink">Work experience</h2>

    <div class="grid gap-5">
      {% for job in site.data.experience %}
      <article class="card rounded-2xl p-6">
        <div class="flex flex-wrap justify-between gap-4 mb-3">
          <div>
            <h3 class="text-xl font-black text-ink">{{ job.role }}</h3>
            <p class="text-rose font-bold">{{ job.company }}</p>
          </div>
          <div class="text-left md:text-right">
            <p class="text-muted text-sm">{{ job.location }}</p>
            <p class="text-soft text-sm">{{ job.period }}</p>
          </div>
        </div>

        <p class="text-muted text-sm leading-relaxed mb-4">{{ job.description }}</p>

        <ul class="grid gap-2">
          {% for bullet in job.bullets %}
          <li class="flex gap-3 text-sm text-muted">
            <span class="text-rose">◆</span>
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
<section id="leadership" class="border-t border-line py-16">
  <div class="max-w-6xl mx-auto px-5">

    <p class="section-kicker mb-4">Leadership</p>
    <h2 class="text-3xl md:text-4xl font-black mb-8 text-ink">Leadership & activities</h2>

    <div class="grid md:grid-cols-2 gap-5">
      {% for item in site.data.leadership %}
      <article class="card rounded-2xl p-6">
        <div class="flex justify-between gap-4 mb-3">
          <div>
            <h3 class="font-black text-ink">{{ item.role }}</h3>
            <p class="text-rose font-bold">{{ item.organisation }}</p>
          </div>
          <p class="text-sm text-soft text-right">{{ item.period }}</p>
        </div>

        <p class="text-muted text-sm leading-relaxed mb-3">{{ item.description }}</p>

        <ul class="grid gap-1">
          {% for bullet in item.bullets %}
          <li class="text-sm text-muted">• {{ bullet }}</li>
          {% endfor %}
        </ul>
      </article>
      {% endfor %}
    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="border-t border-line py-16">
  <div class="max-w-6xl mx-auto px-5">

    <p class="section-kicker mb-4">Projects</p>
    <h2 class="text-3xl md:text-4xl font-black mb-8 text-ink">Selected portfolio projects</h2>

    <div class="grid lg:grid-cols-2 gap-5">
      {% for project in site.data.projects %}
      <article class="card rounded-2xl p-6 hover:-translate-y-1 transition">
        <div class="flex flex-wrap justify-between gap-3 mb-3">
          <div>
            <p class="text-rose font-bold text-sm">{{ project.type }}</p>
            <h3 class="text-xl font-black text-ink mt-1">{{ project.title }}</h3>
          </div>
        </div>

        <p class="text-muted text-sm leading-relaxed mb-4">{{ project.summary }}</p>

        <div class="grid gap-3 mb-4">
          <p class="text-sm text-muted"><strong class="text-ink">What I did:</strong> {{ project.what }}</p>
          <p class="text-sm text-muted"><strong class="text-ink">How I did it:</strong> {{ project.how }}</p>
          <p class="text-sm text-muted"><strong class="text-ink">Impact:</strong> {{ project.outcome }}</p>
        </div>

        <div class="flex flex-wrap gap-2 mb-4">
          {% for tech in project.tech %}
          <span class="px-3 py-1 rounded-full bg-blush text-roseDark text-xs font-bold">
            {{ tech }}
          </span>
          {% endfor %}
        </div>

        <a href="{{ project.link }}" target="_blank" class="text-rose font-black text-sm">
          View Project →
        </a>
      </article>
      {% endfor %}
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="border-t border-line py-16">
  <div class="max-w-3xl mx-auto px-5 text-center">

    <p class="section-kicker mb-4">Contact</p>
    <h2 class="text-3xl md:text-4xl font-black mb-4 text-ink">Let’s connect.</h2>

    <p class="text-muted max-w-2xl mx-auto mb-6 leading-relaxed">
      I am open to Data Analyst, Business Analyst, Business Intelligence, CRM analytics, and consulting-oriented graduate roles.
    </p>

    <div class="card rounded-2xl p-6">
      <p class="text-xl font-black text-ink mb-1">{{ profile.email }}</p>
      <p class="text-muted mb-5">{{ profile.location }}</p>

      <div class="flex justify-center flex-wrap gap-3">
        <a href="{{ profile.linkedin }}" target="_blank" class="px-5 py-2.5 rounded-full bg-rose text-white font-bold text-sm hover:bg-roseDark transition">
          LinkedIn
        </a>
        <a href="{{ profile.github }}" target="_blank" class="px-5 py-2.5 rounded-full border border-line font-bold text-sm hover:border-rose hover:text-rose transition">
          GitHub
        </a>
        <a href="mailto:{{ profile.email }}" class="px-5 py-2.5 rounded-full border border-line font-bold text-sm hover:border-rose hover:text-rose transition">
          Email Me
        </a>
      </div>
    </div>

  </div>
</section>
