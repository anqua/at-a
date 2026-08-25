---
layout: default
title: People
---

<div id="people">
{% for person in site.data.people %}
  <div class="person-card">
    {% if person.photo %}
      <img src="{{ person.photo }}" alt="{{ person.name }}">
    {% endif %}
    <h3>{{ person.name }}</h3>
    <p class="role">{{ person.role }}</p>
    {% if person.research %}
      <p class="research">{{ person.research }}</p>
    {% endif %}
    <p class="contact">
      {% assign has_prev = false %}
      {% if person.email %}<a href="mailto:{{ person.email }}">Email</a>{% assign has_prev = true %}{% endif %}
      {% if person.website %}{% if has_prev %} | {% endif %}<a href="{{ person.website }}" target="_blank" rel="noopener">Website</a>{% assign has_prev = true %}{% endif %}
      {% if person.linkedin %}{% if has_prev %} | {% endif %}<a href="{{ person.linkedin }}" target="_blank" rel="noopener">{% include icon-linkedin.html %}LinkedIn</a>{% assign has_prev = true %}{% endif %}
      {% if person.scholar %}{% if has_prev %} | {% endif %}<a href="{{ person.scholar }}" target="_blank" rel="noopener">{% include icon-scholar.html %}Google Scholar</a>{% assign has_prev = true %}{% endif %}
    </p>
  </div>
{% endfor %}
</div>

## Graduates:
Simai (Stella) Huang | 黄思迈 (role: Research Assistant / current role: PhD student Beijing Normal Hong Kong Baptist University)

## Collaborators
