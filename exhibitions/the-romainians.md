---
layout: default
title: The Rom(AI)nians
exhibition_id: rom-ai-nians
images:
  - /at-a/assets/images/exhibitions/romainians/04-poster.jpg
  - type: video
    src: /at-a/assets/videos/the-romainians-reel.mp4
  - /at-a/assets/images/exhibitions/romainians/01-exterior-entrance.jpg
  - /at-a/assets/images/exhibitions/romainians/02-exterior-cutout.jpg
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

{% if ex.press %}<p class="pub-actions">
  <a class="pub-btn" href="{{ ex.press }}" target="_blank" rel="noopener">Press coverage</a>
</p>{% endif %}

{% include exhibition-gallery.html images=page.images title=ex.title %}
