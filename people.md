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
      {% if person.email %}<a href="mailto:{{ person.email }}">Email</a>{% endif %}
      {% if person.website %} | <a href="{{ person.website }}" target="_blank">Website</a>{% endif %}
    </p>
  </div>
{% endfor %}
</div>

## Faculty

**Name Surname**  
Role, affiliation  
Research interests

## Researchers

**Name Surname**  
Position  
Research interests

## Students

- Name Surname (PhD)
- Name Surname (MSc)

