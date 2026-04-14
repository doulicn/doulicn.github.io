---
permalink: /
title: "Dou Li"
layout: splash
author_profile: false
classes: wide
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<section class="home-hero">
  <div class="home-hero__copy">
    <p class="home-eyebrow">Academic Website</p>
    <h1>Dou Li</h1>
    <p class="home-lead">Researcher at Boston University. This site highlights current work, publications, professional materials, and ways to get in touch.</p>
    <div class="home-actions">
      <a class="btn btn--primary" href="#publications">View Publications</a>
      <a class="btn btn--inverse" href="#contact">Contact</a>
    </div>
    <ul class="home-links">
      {% if site.author.googlescholar %}<li><a href="{{ site.author.googlescholar }}">Google Scholar</a></li>{% endif %}
      {% if site.author.orcid %}<li><a href="{{ site.author.orcid }}">ORCID</a></li>{% endif %}
      {% if site.author.researchgate %}<li><a href="{{ site.author.researchgate }}">ResearchGate</a></li>{% endif %}
    </ul>
  </div>
  <div class="home-hero__image">
    <img src="{{ base_path }}/images/profile.png" alt="Portrait of Dou Li">
  </div>
</section>

<section class="home-section" id="bio">
  <div class="home-section__header">
    <p class="home-section__eyebrow">Bio</p>
    <h2>About</h2>
  </div>
  <div class="home-card">
    <p>Dou Li is affiliated with Boston University. This website is structured as a clean academic profile with space for research highlights, publications, a concise curriculum vitae, and professional contact information.</p>
    <p>The current content uses the existing repository data and can be expanded by updating the markdown files for publications, talks, teaching, and CV materials.</p>
  </div>
</section>

<section class="home-section" id="research">
  <div class="home-section__header">
    <p class="home-section__eyebrow">Research</p>
    <h2>Research Overview</h2>
  </div>
  <div class="home-grid home-grid--two">
    <div class="home-card">
      <h3>Current Focus</h3>
      <p>Use this section to summarize core research questions, methods, and ongoing projects in a few clear sentences. The layout is already configured for a compact overview that works well on desktop and mobile.</p>
    </div>
    <div class="home-card">
      <h3>Areas of Interest</h3>
      <p>Add a short list of themes, application domains, or interdisciplinary interests here. Keeping this section brief makes the homepage scan quickly for collaborators, students, and recruiters.</p>
    </div>
  </div>
</section>

<section class="home-section" id="publications">
  <div class="home-section__header">
    <p class="home-section__eyebrow">Publications</p>
    <h2>Selected Work</h2>
  </div>
  <div class="home-card home-card--spaced">
    {% assign selected_publications = site.publications | sort: "date" | reverse %}
    {% for post in selected_publications limit:3 %}
      <article class="publication-preview">
        <p class="publication-preview__meta">{{ post.date | date: "%Y" }}{% if post.venue %} · {{ post.venue }}{% endif %}</p>
        <h3><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h3>
        {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
      </article>
    {% endfor %}
    <p class="home-section__link"><a href="{{ base_path }}/publications/">Browse the full publications list</a></p>
  </div>
</section>

<section class="home-section" id="cv">
  <div class="home-section__header">
    <p class="home-section__eyebrow">CV</p>
    <h2>Curriculum Vitae</h2>
  </div>
  <div class="home-grid home-grid--two">
    <div class="home-card">
      <h3>At a Glance</h3>
      <ul class="home-list">
        <li>Affiliation: Boston University</li>
        <li>Email: <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a></li>
        <li>Profiles: Google Scholar, ORCID, and ResearchGate</li>
      </ul>
    </div>
    <div class="home-card">
      <h3>Full CV</h3>
      <p>The full CV page is set up for a more detailed academic record, including affiliations, professional links, and publications.</p>
      <p><a class="btn btn--primary" href="{{ base_path }}/cv/">Open CV Page</a></p>
    </div>
  </div>
</section>

<section class="home-section" id="contact">
  <div class="home-section__header">
    <p class="home-section__eyebrow">Contact</p>
    <h2>Get In Touch</h2>
  </div>
  <div class="home-card">
    <p>The most direct way to reach Dou Li is by email at <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>.</p>
    <p>Academic profiles:
      {% if site.author.googlescholar %}<a href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
      {% if site.author.orcid %} · <a href="{{ site.author.orcid }}">ORCID</a>{% endif %}
      {% if site.author.researchgate %} · <a href="{{ site.author.researchgate }}">ResearchGate</a>{% endif %}
    </p>
  </div>
</section>
