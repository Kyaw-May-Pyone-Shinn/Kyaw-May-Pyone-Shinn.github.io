---
layout: default
---

{% assign profile = site.data.profile %}

<!-- HERO -->
<section id="home" class="py-20">

  <div class="max-w-6xl mx-auto px-6 grid lg:grid-cols-2 gap-12 items-center">

    <!-- LEFT -->
    <div class="max-w-xl">

      <p class="section-label mb-5">
        Hello There
      </p>

      <h1 class="text-4xl md:text-5xl font-black leading-tight mb-5">

        Hi, I’m <br>

        <span class="text-accent">
          Kyaw May
        </span>

        Pyone Shinn

      </h1>

      <div class="text-2xl font-bold mb-5">

        I’m a

        <span id="rotating-role"
              class="text-accent role-transition">
          Data Analyst
        </span>

      </div>

      <p class="text-muted leading-relaxed mb-7">

        I build analytics, dashboards, CRM reporting,
        and decision-support solutions that transform
        operational data into actionable business insights.

      </p>

      <div class="flex flex-wrap gap-3 mb-7">

        <a href="#projects"
           class="px-5 py-2.5 rounded-full bg-accent text-white text-sm font-bold hover:bg-accentDark transition">

          Explore Projects

        </a>

        <a href="#contact"
           class="px-5 py-2.5 rounded-full border border-border bg-white text-sm font-bold hover:border-accent hover:text-accent transition">

          Contact Me

        </a>

      </div>

      <div class="flex flex-wrap gap-3 text-sm">

        <a href="{{ profile.linkedin }}"
           target="_blank"
           class="px-4 py-2 rounded-full bg-white border border-border hover:border-accent hover:text-accent transition">

          LinkedIn

        </a>

        <a href="{{ profile.github }}"
           target="_blank"
           class="px-4 py-2 rounded-full bg-white border border-border hover:border-accent hover:text-accent transition">

          GitHub

        </a>

        <a href="mailto:{{ profile.email }}"
           class="px-4 py-2 rounded-full bg-white border border-border hover:border-accent hover:text-accent transition">

          Email

        </a>

      </div>

    </div>

    <!-- RIGHT -->
    <div class="grid gap-4">

      <!-- PROFILE SUMMARY -->
      <div class="card rounded-3xl p-7">

        <div class="flex items-start gap-5">

          <div class="w-14 h-14 rounded-2xl bg-accentSoft flex items-center justify-center text-accent font-black text-xl shrink-0">
            K
          </div>

          <div>

            <h2 class="text-xl font-black mb-1">
              MSc Data Analytics Candidate
            </h2>

            <p class="text-accent text-sm font-semibold mb-4">
              Business Intelligence • CRM Analytics • Consulting
            </p>

            <p class="text-muted text-sm leading-relaxed">

              Focused on building structured analytics,
              business intelligence dashboards, CRM reporting,
              and decision-support solutions that align data
              with operational and strategic business goals.

            </p>

          </div>

        </div>

      </div>

      <!-- KPI -->
      <div class="grid grid-cols-2 gap-4">

        {% for item in profile.highlights %}

        <div class="card rounded-2xl p-5">

          <p class="text-3xl font-black">
            {{ item.value }}
          </p>

          <p class="text-sm text-muted mt-2 leading-relaxed">
            {{ item.label }}
          </p>

        </div>

        {% endfor %}

      </div>

    </div>

  </div>

</section>

<!-- ABOUT -->
<section id="about" class="py-16 border-t border-border">

  <div class="max-w-6xl mx-auto px-6">

    <p class="section-label mb-4">
      About
    </p>

    <h2 class="text-3xl font-black mb-8">
      Professional Profile
    </h2>

    <div class="grid md:grid-cols-2 gap-5">

      {% for paragraph in profile.summary %}

      <div class="card rounded-2xl p-6">

        <p class="text-muted leading-relaxed">
          {{ paragraph }}
        </p>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- SKILLS -->
<section id="skills" class="py-16 border-t border-border">

  <div class="max-w-6xl mx-auto px-6">

    <p class="section-label mb-4">
      Skills
    </p>

    <h2 class="text-3xl font-black mb-8">
      Technical & Business Capabilities
    </h2>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-5">

      {% for skill in profile.technical_skills %}

      <div class="card rounded-2xl p-6">

        <h3 class="font-black text-accent mb-3">
          {{ skill.category }}
        </h3>

        <p class="text-muted text-sm leading-relaxed">
          {{ skill.items }}
        </p>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- EXPERIENCE -->
<section id="experience" class="py-16 border-t border-border">

  <div class="max-w-6xl mx-auto px-6">

    <p class="section-label mb-4">
      Experience
    </p>

    <h2 class="text-3xl font-black mb-8">
      Professional Experience
    </h2>

    <div class="grid gap-5">

      {% for job in site.data.experience %}

      <div class="card rounded-2xl p-7">

        <div class="flex flex-wrap justify-between gap-4 mb-5">

          <div>

            <h3 class="text-xl font-black">
              {{ job.role }}
            </h3>

            <p class="text-accent font-semibold">
              {{ job.company }}
            </p>

          </div>

          <div class="text-sm text-muted text-left md:text-right">

            <p>{{ job.location }}</p>
            <p>{{ job.period }}</p>

          </div>

        </div>

        <p class="text-muted text-sm leading-relaxed mb-5">
          {{ job.description }}
        </p>

        <ul class="grid gap-2">

          {% for bullet in job.bullets %}

          <li class="text-sm text-muted leading-relaxed">
            • {{ bullet }}
          </li>

          {% endfor %}

        </ul>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- LEADERSHIP -->
<section id="leadership" class="py-16 border-t border-border">

  <div class="max-w-6xl mx-auto px-6">

    <p class="section-label mb-4">
      Leadership
    </p>

    <h2 class="text-3xl font-black mb-8">
      Leadership & Activities
    </h2>

    <div class="grid md:grid-cols-2 gap-5">

      {% for item in site.data.leadership %}

      <div class="card rounded-2xl p-7">

        <div class="flex justify-between gap-4 mb-4">

          <div>

            <h3 class="font-black">
              {{ item.role }}
            </h3>

            <p class="text-accent font-semibold">
              {{ item.organisation }}
            </p>

          </div>

          <p class="text-sm text-muted">
            {{ item.period }}
          </p>

        </div>

        <p class="text-sm text-muted leading-relaxed mb-5">
          {{ item.description }}
        </p>

        <ul class="grid gap-2">

          {% for bullet in item.bullets %}

          <li class="text-sm text-muted leading-relaxed">
            • {{ bullet }}
          </li>

          {% endfor %}

        </ul>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- PROJECTS -->
<section id="projects" class="py-16 border-t border-border">

  <div class="max-w-6xl mx-auto px-6">

    <p class="section-label mb-4">
      Projects
    </p>

    <h2 class="text-3xl font-black mb-8">
      Selected Portfolio Projects
    </h2>

    <div class="grid lg:grid-cols-2 gap-5">

      {% for project in site.data.projects %}

      <div class="card rounded-2xl p-7">

        <div class="mb-5">

          <p class="text-sm text-accent font-semibold mb-2">
            {{ project.type }}
          </p>

          <h3 class="text-xl font-black">
            {{ project.title }}
          </h3>

        </div>

        <p class="text-sm text-muted leading-relaxed mb-5">
          {{ project.summary }}
        </p>

        <div class="grid gap-4 mb-5">

          <div>
            <p class="text-sm font-bold mb-1">
              What I did
            </p>

            <p class="text-sm text-muted leading-relaxed">
              {{ project.what }}
            </p>
          </div>

          <div>
            <p class="text-sm font-bold mb-1">
              How I did it
            </p>

            <p class="text-sm text-muted leading-relaxed">
              {{ project.how }}
            </p>
          </div>

          <div>
            <p class="text-sm font-bold mb-1">
              Outcome
            </p>

            <p class="text-sm text-muted leading-relaxed">
              {{ project.outcome }}
            </p>
          </div>

        </div>

        <div class="flex flex-wrap gap-2 mb-5">

          {% for tech in project.tech %}

          <span class="px-3 py-1 rounded-full bg-accentSoft text-accentDark text-xs font-semibold">
            {{ tech }}
          </span>

          {% endfor %}

        </div>

        <a href="{{ project.link }}"
           target="_blank"
           class="text-accent font-bold text-sm">

          View Project →

        </a>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- CONTACT -->
<section id="contact" class="py-16 border-t border-border">

  <div class="max-w-3xl mx-auto px-6 text-center">

    <p class="section-label mb-4">
      Contact
    </p>

    <h2 class="text-3xl font-black mb-5">
      Let’s Connect
    </h2>

    <p class="text-muted leading-relaxed mb-8">

      I am currently open to graduate and early-career opportunities
      in Data Analytics, Business Intelligence, Business Analysis,
      CRM Analytics, and consulting-oriented roles.

    </p>

    <div class="card rounded-3xl p-8">

      <p class="text-xl font-black mb-2">
        {{ profile.email }}
      </p>

      <p class="text-muted mb-6">
        Dublin, Ireland
      </p>

      <div class="flex flex-wrap justify-center gap-3">

        <a href="{{ profile.linkedin }}"
           target="_blank"
           class="px-5 py-2.5 rounded-full bg-accent text-white text-sm font-bold hover:bg-accentDark transition">

          LinkedIn

        </a>

        <a href="{{ profile.github }}"
           target="_blank"
           class="px-5 py-2.5 rounded-full border border-border text-sm font-bold hover:border-accent hover:text-accent transition">

          GitHub

        </a>

        <a href="mailto:{{ profile.email }}"
           class="px-5 py-2.5 rounded-full border border-border text-sm font-bold hover:border-accent hover:text-accent transition">

          Email Me

        </a>

      </div>

    </div>

  </div>

</section>
