---
layout: default
title: People
---

<div id="people">

<h2>Active Members</h2>

{% assign active_people = site.data.people | where: "status", "active" %}

{% for person in active_people %}
  <div class="person-card">

    {% if person.photo %}
      <img src="{{ site.baseurl }}{{ person.photo }}" alt="{{ person.name }}">
    {% endif %}

    <h3>{{ person.name }}</h3>
    <p>{{ person.role }}</p>

    {% if person.research %}
      <p>{{ person.research }}</p>
    {% endif %}

    {% if person.email %}
      <a href="mailto:{{ person.email }}">Email</a>
    {% endif %}

    {% if person.website %}
      <a href="{{ person.website }}" target="_blank" rel="noopener">Website</a>
    {% endif %}

    {% if person.scholar %}
      <a href="{{ person.scholar }}" target="_blank" rel="noopener">Google Scholar</a>
    {% endif %}

    {% if person.linkedin %}
      <a href="{{ person.linkedin }}" target="_blank" rel="noopener">LinkedIn</a>
    {% endif %}

  </div>
{% endfor %}


<h2>Graduates</h2>

{% assign graduates = site.data.people | where: "status", "graduate" %}

{% for person in graduates %}
  <div class="person-card">

    {% if person.photo %}
      <img src="{{ site.baseurl }}{{ person.photo }}" alt="{{ person.name }}">
    {% endif %}

    <h3>{{ person.name }}</h3>
    <p>{{ person.role }}</p>

    {% if person.research %}
      <p>{{ person.research }}</p>
    {% endif %}

    {% if person.email %}
      <a href="mailto:{{ person.email }}">Email</a>
    {% endif %}

    {% if person.website %}
      <a href="{{ person.website }}" target="_blank" rel="noopener">Website</a>
    {% endif %}

    {% if person.scholar %}
      <a href="{{ person.scholar }}" target="_blank" rel="noopener">Google Scholar</a>
    {% endif %}

    {% if person.linkedin %}
      <a href="{{ person.linkedin }}" target="_blank" rel="noopener">LinkedIn</a>
    {% endif %}

  </div>
{% endfor %}

</div>

## Collaborators
