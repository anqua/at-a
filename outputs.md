---
layout: default
title: Outputs
---

## Publications

<ul>
{% for pub in site.data.publications %}
  <li>
    {% if pub.type == "article" %}
      {{ pub.authors }}. <strong>{{ pub.title }}</strong>. {{ pub.journal }}, {{ pub.year }}{% if pub.volume %}, vol. {{ pub.volume }}{% endif %}{% if pub.pages %}, pp. {{ pub.pages }}{% endif %}. {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}">DOI</a>{% endif %}
    {% elsif pub.type == "conference" %}
      {{ pub.authors }}. <strong>{{ pub.title }}</strong>. In {{ pub.conference }}, {{ pub.year }}.
    {% endif %}
  </li>
{% endfor %}
</ul>



## Journal Articles

- **Author, A.; Author, B.**  
  *Title of the paper.* Journal Name, Year.

## Conference Papers

- **Author, A.; Author, B.**  
  *Title of the paper.* Conference Name, Year.

## Other Outputs

- Software packages
- Technical reports
- Datasets

