---
layout: default
title: The Rom(AI)nians
exhibition_id: rom-ai-nians
images:
  - /at-a/assets/images/exhibitions/romainians/04-poster.jpg
  - /at-a/assets/images/exhibitions/romainians/01-exterior-entrance.jpg
  - /at-a/assets/images/exhibitions/romainians/02-exterior-cutout.jpg
  - /at-a/assets/images/exhibitions/romainians/05-interior-wide.jpg
  - /at-a/assets/images/exhibitions/romainians/06-laptop-printer.jpg
  - /at-a/assets/images/exhibitions/romainians/07-facebook-profile.jpg
  - /at-a/assets/images/exhibitions/romainians/08-banana.jpg
---

{% assign ex = site.data.exhibitions | where: "id", page.exhibition_id | first %}

<p><a href="/at-a/outputs#exhibitions" class="exhibition-back">&larr; Back to Outputs</a></p>

<h1>{{ ex.title }}</h1>
<p class="exhibition-page-meta">{% if ex.venue_url %}<a href="{{ ex.venue_url }}" target="_blank" rel="noopener">{{ ex.venue }}</a>{% else %}{{ ex.venue }}{% endif %}{% if ex.location %}, {{ ex.location }}{% endif %} &middot; {{ ex.year }}</p>
{% if ex.credits %}<p class="exhibition-page-credits">{{ ex.credits }}</p>{% endif %}

{% if ex.description_long %}
  {% for para in ex.description_long %}<p>{{ para }}</p>
  {% endfor %}
{% elsif ex.description %}<p>{{ ex.description }}</p>
{% endif %}

{% if ex.press or ex.instagram %}<p class="pub-actions">
  {% if ex.press %}<a class="pub-btn" href="{{ ex.press }}" target="_blank" rel="noopener">Press coverage</a>{% endif %}
  {% if ex.instagram %}<a class="pub-btn" href="{{ ex.instagram }}" target="_blank" rel="noopener">Instagram</a>{% endif %}
</p>{% endif %}

<div class="exhibition-video">
  <video controls preload="metadata">
    <source src="/at-a/assets/videos/the-romainians-reel.mp4" type="video/mp4">
  </video>
</div>

<div class="exhibition-gallery">
{% if page.images and page.images.size > 0 %}
  {% for img in page.images %}
  <img src="{{ img }}" alt="{{ ex.title | escape }} &mdash; installation view">
  {% endfor %}
{% else %}
  <p class="exhibition-placeholder">Installation images coming soon.</p>
{% endif %}
</div>
