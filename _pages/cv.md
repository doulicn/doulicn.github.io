---
layout: archive
title: "CV"
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% include base_path %}

This page provides a concise academic CV built from the current repository content.

Professional Profile
======

* **Name:** Dou Li
* **Affiliation:** Boston University
* **Email:** [{{ site.author.email }}](mailto:{{ site.author.email }})
* **Google Scholar:** [Profile]({{ site.author.googlescholar }})
* **ORCID:** [Profile]({{ site.author.orcid }})
* **ResearchGate:** [Profile]({{ site.author.researchgate }})

Research Summary
======

Add a concise summary of research interests, methods, and academic contributions here. The current site structure is ready for a fuller CV once position history, education, awards, service, and advising details are added.

Publications
======

<ul>
{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}
</ul>
