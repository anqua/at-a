---
layout: default
title: People
---

<h2 class="people-heading">Group members ({{ site.data.people.size }})</h2>

<div id="people">
{% for person in site.data.people %}
  <div class="person-card">
    {% if person.photo %}
      <img src="{{ person.photo }}" alt="{{ person.name }}">
    {% endif %}
    <h3>{{ person.name }}</h3>
    <p class="role">{{ person.role }}{% if person.since %}<span class="since">{{ person.since }}</span>{% endif %}</p>
    {% if person.research %}
      <p class="research">{{ person.research }}</p>
    {% endif %}
    <p class="contact">
      {% assign has_prev = false %}
      {% if person.email %}<a href="mailto:{{ person.email }}" aria-label="Email">{% include icon-email.html %}</a>{% assign has_prev = true %}{% endif %}
      {% if person.cv %}{% if has_prev %} | {% endif %}<a href="{{ person.cv }}" target="_blank" rel="noopener" aria-label="CV">{% include icon-cv.html %}</a>{% assign has_prev = true %}{% endif %}
      {% if person.website %}{% if has_prev %} | {% endif %}<a href="{{ person.website }}" target="_blank" rel="noopener" aria-label="Website">{% include icon-website.html %}</a>{% assign has_prev = true %}{% endif %}
      {% if person.linkedin %}{% if has_prev %} | {% endif %}<a href="{{ person.linkedin }}" target="_blank" rel="noopener" aria-label="LinkedIn">{% include icon-linkedin.html %}</a>{% assign has_prev = true %}{% endif %}
      {% if person.scholar %}{% if has_prev %} | {% endif %}<a href="{{ person.scholar }}" target="_blank" rel="noopener" aria-label="Google Scholar">{% include icon-scholar.html %}</a>{% assign has_prev = true %}{% endif %}
    </p>
  </div>
{% endfor %}
</div>

<div id="visiting">
  <h2 class="visiting-heading">Visiting researchers ({{ site.data.visiting.size }})</h2>
{% for v in site.data.visiting %}
  <div class="visiting-card visiting-card--{{ v.area }}">
    <img src="{% if v.photo %}{{ v.photo }}{% else %}/at-a/assets/images/Logo_AtA.png{% endif %}" alt="{{ v.name | escape }}" class="visiting-photo{% unless v.photo %} visiting-photo--logo{% endunless %}">
    <div class="visiting-body">
      <p class="visiting-area">{% if v.area == "ah-tech" %}Arts &amp; Humanities &times; Technology{% elsif v.area == "ah-arch" %}Arts &amp; Humanities &times; Architecture{% elsif v.area == "tech-arch" %}Technology &times; Architecture{% endif %}</p>
      <h3>{{ v.name }}</h3>
      <p class="visiting-role">{{ v.role }}{% if v.affiliation %} &middot; {{ v.affiliation }}{% endif %}</p>
      <p class="visiting-bio">{{ v.bio }}</p>
    </div>
  </div>
{% endfor %}
</div>

<div id="graduates" markdown="1">

## Graduates

Simai (Stella) Huang \| 黄思迈 (role: Research Assistant / current role: PhD student Beijing Normal Hong Kong Baptist University)

</div>

## Academic and industry friends and collaborators
{: .section-heading-center }

<div id="collaborators">
{% for collab in site.data.collaborators %}
  <div class="collab-item">
    {% if collab.logo %}<img src="{{ collab.logo }}" alt="{{ collab.name }}" class="collab-logo">{% else %}<span class="collab-name">{{ collab.name }}</span>{% endif %}
  </div>
{% endfor %}
</div>
