---
layout: default
title: Equipe
---

# Equipe HydroUAI

<div class="grid">
{% for member in site.data.team %}
  <article class="card">
    {% if member.headshot %}
      <img src="{{ member.headshot | relative_url }}" alt="Foto de {{ member.name }}" class="avatar" />
    {% else %}
      <div class="avatar">
        {% assign parts = member.name | split: ' ' %}
        {{ parts[0] | slice: 0,1 }}{{ parts | last | slice: 0,1 }}
      </div>
    {% endif %}
    <h3>{{ member.name }}</h3>
    <p>{{ member.role }}</p>
    <p>{{ member.research_focus }}</p>
  </article>
{% endfor %}
</div>
