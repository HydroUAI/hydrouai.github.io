---
layout: default
title: Projetos
---

# Projetos

<div class="grid">
{% for p in site.data.projects %}
  <article class="card">
    <h3>{{ p.title }}</h3>
    <p><em>Status:</em> {{ p.status }}</p>
    <p>{{ p.summary }}</p>
  </article>
{% endfor %}
</div>
