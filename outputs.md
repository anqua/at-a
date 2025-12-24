---
layout: default
title: Outputs
---

## Publications

<div id="outputs">

<h3>Journal Articles</h3>
<dl>
{% assign sorted_journals = site.data.publications | where: "type", "article" | sort: "year" | reverse %}
{% for pub in sorted_journals %}
  <dt>{{ pub.authors }} ({{ pub.year }})</dt>
  <dd>
    <em>{{ pub.title }}</em>. {{ pub.journal }}{% if pub.volume %}, vol. {{ pub.volume }}{% endif %}{% if pub.pages %}, pp. {{ pub.pages }}{% endif %}.
    {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
  </dd>
{% endfor %}
</dl>

<h3>Conference Papers</h3>
<dl>
{% assign sorted_confs = site.data.publications | where: "type", "conference" | sort: "year" | reverse %}
{% for pub in sorted_confs %}
  <dt>{{ pub.authors }} ({{ pub.year }})</dt>
  <dd>
    <em>{{ pub.title }}</em>. In {{ pub.conference }}.
    {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
  </dd>
{% endfor %}
</dl>

</div>


## Other Outputs
- Datasets
- Software packages
- Technical reports


