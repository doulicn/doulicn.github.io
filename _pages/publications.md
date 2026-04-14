---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
---

{% if site.author.googlescholar %}
  <div class="wordwrap">A full list can also be maintained on <a href="{{site.author.googlescholar}}">Google Scholar</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
