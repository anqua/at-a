---
layout: default
title: The Rom(AI)nians
exhibition_id: rom-ai-nians
images: []
---

{% assign ex = site.data.exhibitions | where: "id", page.exhibition_id | first %}

<p><a href="/at-a/outputs/#exhibitions" class="exhibition-back">&larr; Back to Outputs</a></p>

<h1>{{ ex.title }}</h1>
<p class="exhibition-page-meta">{{ ex.venue }}{% if ex.location %}, {{ ex.location }}{% endif %} &middot; {{ ex.year }}</p>
{% if ex.credits %}<p class="exhibition-page-credits">{{ ex.credits }}</p>{% endif %}

{% if ex.description %}<p>{{ ex.description }}</p>{% endif %}

{% if ex.press %}<p><a class="pub-btn" href="{{ ex.press }}" target="_blank" rel="noopener">Press coverage</a></p>{% endif %}

<div class="exhibition-gallery">
{% if page.images and page.images.size > 0 %}
  {% for img in page.images %}
  <img src="{{ img }}" alt="{{ ex.title | escape }} &mdash; installation view">
  {% endfor %}
{% else %}
  <p class="exhibition-placeholder">Installation images coming soon.</p>
{% endif %}
</div>
