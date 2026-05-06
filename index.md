---
layout: default
---

{% assign profile = site.data.profile %}

<!-- HERO -->
<section id="home" class="py-14">

  <div class="max-w-5xl mx-auto px-6">

    <div class="max-w-3xl">

      <p class="section-label mb-4">
        Data Analytics • Business Intelligence • Consulting
      </p>

      <h1 class="text-3xl md:text-4xl font-black leading-tight mb-5 text-text">
        Kyaw May Pyone Shinn
      </h1>

      <div class="text-xl font-semibold mb-5 text-text">

        <span id="rotating-role"
              class="text-accent role-transition">

          Data Analyst

        </span>

      </div>

      <p class="text-muted leading-relaxed mb-7 max-w-2xl">

        MSc Data Analytics candidate with a strong focus on Business Intelligence,
        CRM analytics, dashboard development, and consulting-oriented problem solving.
        Experienced in transforming operational and business data into structured,
        actionable insights using Tableau, Salesforce, Python, SQL, and Power BI.

      </p>

      <!-- BUTTONS -->
      <div class="flex flex-wrap gap-3 mb-6">

        <a href="#projects"
           class="px-5 py-2.5 rounded-full bg-accent text-white text-sm font-semibold hover:bg-accentDark transition">

          View Projects

        </a>

        <a href="#contact"
           class="px-5 py-2.5 rounded-full border border-border bg-white text-sm font-semibold hover:border-accent hover:text-accent transition">

          Contact

        </a>

      </div>

      <!-- SOCIAL -->
      <div class="flex flex-wrap gap-3 text-sm">

        <a href="{{ profile.linkedin }}"
           target="_blank"
           class="text-muted hover:text-accent transition">

          LinkedIn

        </a>

        <span class="text-border">•</span>

        <a href="{{ profile.github }}"
           target="_blank"
           class="text-muted hover:text-accent transition">

          GitHub

        </a>

        <span class="text-border">•</span>

        <a href="mailto:{{ profile.email }}"
           class="text-muted hover:text-accent transition">

          Email

        </a>

      </div>

    </div>

  </div>

</section>

<!-- ABOUT -->
<section id="about" class="py-12 border-t border-border">

  <div class="max-w-5xl mx-auto px-6">

    <p class="section-label mb-3">
      About
    </p>

    <h2 class="text-2xl font-black mb-6">
      Professional Profile
    </h2>

    <div class="grid gap-4">

      {% for paragraph in profile.summary %}

      <div class="card rounded-2xl p-5">

        <p class="text-sm text-muted leading-relaxed">
          {{ paragraph }}
        </p>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- SKILLS -->
<section id="skills" class="py-12 border-t border-border">

  <div class="max-w-5xl mx-auto px-6">

    <p class="section-label mb-3">
      Skills
    </p>

    <h2 class="text-2xl font-black mb-6">
      Technical & Business Capabilities
    </h2>

    <div class="grid md:grid-cols-2 gap-4">

      {% for skill in profile.technical_skills %}

      <div class="card rounded-2xl p-5">

        <h3 class="font-bold text-accent mb-2 text-sm">
          {{ skill.category }}
        </h3>

        <p class="text-sm text-muted leading-relaxed">
          {{ skill.items }}
        </p>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- EXPERIENCE -->
<section id="experience" class="py-12 border-t border-border">

  <div class="max-w-5xl mx-auto px-6">

    <p class="section-label mb-3">
      Experience
    </p>

    <h2 class="text-2xl font-black mb-6">
      Professional Experience
    </h2>

    <div class="grid gap-4">

      {% for job in site.data.experience %}

      <div class="card rounded-2xl p-5">

        <div class="flex flex-wrap justify-between gap-3 mb-4">

          <div>

            <h3 class="text-lg font-black">
              {{ job.role }}
            </h3>

            <p class="text-accent text-sm font-semibold">
              {{ job.company }}
            </p>

          </div>

          <div class="text-sm text-muted text-left md:text-right">

            <p>{{ job.location }}</p>
            <p>{{ job.period }}</p>

          </div>

        </div>

        <p class="text-sm text-muted leading-relaxed mb-4">
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
<section id="leadership" class="py-12 border-t border-border">

  <div class="max-w-5xl mx-auto px-6">

    <p class="section-label mb-3">
      Leadership
    </p>

    <h2 class="text-2xl font-black mb-6">
      Leadership & Activities
    </h2>

    <div class="grid gap-4">

      {% for item in site.data.leadership %}

      <div class="card rounded-2xl p-5">

        <div class="flex flex-wrap justify-between gap-3 mb-4">

          <div>

            <h3 class="font-black">
              {{ item.role }}
            </h3>

            <p class="text-accent text-sm font-semibold">
              {{ item.organisation }}
            </p>

          </div>

          <p class="text-sm text-muted">
            {{ item.period }}
          </p>

        </div>

        <p class="text-sm text-muted leading-relaxed mb-4">
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
<section id="projects" class="py-12 border-t border-border">

  <div class="max-w-5xl mx-auto px-6">

    <p class="section-label mb-3">
      Projects
    </p>

    <h2 class="text-2xl font-black mb-6">
      Selected Portfolio Projects
    </h2>

    <div class="grid gap-4">

      {% for project in site.data.projects %}

      <div class="card rounded-2xl p-5">

        <div class="mb-4">

          <p class="text-sm text-accent font-semibold mb-2">
            {{ project.type }}
          </p>

          <h3 class="text-lg font-black">
            {{ project.title }}
          </h3>

        </div>

        <p class="text-sm text-muted leading-relaxed mb-4">
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

        <div class="flex flex-wrap gap-2 mb-4">

          {% for tech in project.tech %}

          <span class="px-3 py-1 rounded-full bg-accentSoft text-accentDark text-xs font-semibold">
            {{ tech }}
          </span>

          {% endfor %}

        </div>

        <a href="{{ project.link }}"
           target="_blank"
           class="text-accent text-sm font-bold">

          View Project →

        </a>

      </div>

      {% endfor %}

    </div>

  </div>

</section>

<!-- CONTACT -->
<section id="contact" class="py-12 border-t border-border">

  <div class="max-w-3xl mx-auto px-6">

    <p class="section-label mb-3">
      Contact
    </p>

    <h2 class="text-2xl font-black mb-5">
      Let’s Connect
    </h2>

    <p class="text-sm text-muted leading-relaxed mb-7">

      I am currently open to graduate and early-career opportunities
      in Data Analytics, Business Intelligence, Business Analysis,
      CRM Analytics, and consulting-oriented roles.

    </p>

    <div class="card rounded-2xl p-6">

      <p class="font-black mb-1">
        {{ profile.email }}
      </p>

      <p class="text-sm text-muted mb-5">
        Dublin, Ireland
      </p>

      <div class="flex flex-wrap gap-3">

        <a href="{{ profile.linkedin }}"
           target="_blank"
           class="px-4 py-2 rounded-full bg-accent text-white text-sm font-semibold hover:bg-accentDark transition">

          LinkedIn

        </a>

        <a href="{{ profile.github }}"
           target="_blank"
           class="px-4 py-2 rounded-full border border-border text-sm font-semibold hover:border-accent hover:text-accent transition">

          GitHub

        </a>

        <a href="mailto:{{ profile.email }}"
           class="px-4 py-2 rounded-full border border-border text-sm font-semibold hover:border-accent hover:text-accent transition">

          Email

        </a>

      </div>

    </div>

  </div>

</section>
