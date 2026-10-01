---
layout: default
title: The Blooming Archive
exhibition_id: blooming-archive
images:
  - /at-a/assets/images/exhibitions/blooming-archive/01-overview.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/02-orchid-detail.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/03-visitors.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/04-visitor-interacting.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/05-visitor-photographing.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/06-tablet-closeup.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/07-visitor-tablet.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/08-installation-wide.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/11-installation.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/12-installation.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/13-setup.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/14-setup.jpg
  - /at-a/assets/images/exhibitions/blooming-archive/15-setup.jpg
---

{% assign ex = site.data.exhibitions | where: "id", page.exhibition_id | first %}

<p><a href="/at-a/outputs#exhibitions" class="exhibition-back">&larr; Back to Outputs</a></p>

<h1>{{ ex.title }}</h1>
<p class="exhibition-page-meta">{{ ex.venue }}{% if ex.location %}, {{ ex.location }}{% endif %} &middot; {{ ex.year }}</p>
{% if ex.event %}<p class="exhibition-page-event">{{ ex.event }}</p>{% endif %}
{% if ex.credits %}<p class="exhibition-page-credits">{{ ex.credits }}</p>{% endif %}

{% if ex.description %}<p>{{ ex.description }}</p>{% endif %}

{% include exhibition-gallery.html images=page.images title=ex.title %}
