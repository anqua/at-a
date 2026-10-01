---
layout: default
title: The Blooming Archive
exhibition_id: blooming-archive
images: []
---

{% assign ex = site.data.exhibitions | where: "id", page.exhibition_id | first %}

<p><a href="/at-a/outputs/#exhibitions" class="exhibition-back">&larr; Back to Outputs</a></p>

<h1>{{ ex.title }}</h1>
<p class="exhibition-page-meta">{{ ex.venue }}{% if ex.location %}, {{ ex.location }}{% endif %} &middot; {{ ex.year }}</p>

{% if ex.description %}<p>{{ ex.description }}</p>{% endif %}

<div class="exhibition-gallery">
{% if page.images and page.images.size > 0 %}
  {% for img in page.images %}
  <img src="{{ img }}" alt="{{ ex.title | escape }} &mdash; installation view">
  {% endfor %}
{% else %}
  <p class="exhibition-placeholder">Installation images coming soon.</p>
{% endif %}
</div>
