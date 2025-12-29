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
  <dt>{{ pub.title }}</dt> | {{ pub.year }}
  <dd>
    {{ pub.authors }}. <em>{{ pub.journal }}</em>{% if pub.volume %}, vol. {{ pub.volume }}{% endif %}{% if pub.pages %}, pp. {{ pub.pages }}{% endif %}.
    {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
  </dd>
{% endfor %}
</dl>

<h3>Conference Papers</h3>
<dl>
{% assign sorted_confs = site.data.publications | where: "type", "conference" | sort: "year" | reverse %}
{% for pub in sorted_confs %}
  <dt>{{ pub.title }}</dt> | {{ pub.year }}
  <dd>
    {{ pub.authors }}. In <em>{{ pub.conference }}</em>.
    {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>{% endif %}
  </dd>
{% endfor %}
</dl>

</div>


## Other Outputs
<h3>Datasets</h3>

---
- <dt>ComPara: A Corpus Linguistics Dataset of Computation in Architecture.</dt> | 2022 
| Anca-Simona Horvath. Mendeley Data <a href="https://doi.org/10.17632/7ktscvmxvg.5" target="_blank">DOI</a>
  
  A dataset containing titles of journal issues, and article titles from the journal Architectural Design (2005-2024) and the titles and abstracts of winning projects and honourable mentions of the eVolo skyscraper competition (2006-2024). This can be used in promt engineering or in training AI models with language that is specific to the field of architecture:


---
- <dt>Annotated point clouds of buildings: a segmented dataset of single-family houses.</dt> | 2022 
| Panagiota Pouliou, Anca-Simona Horvath, George Palamas. Mendeley Data. <a href="https://doi.org/10.17632/3thtp7mc6z.1" target="_blank">DOI</a>

  A dataset containing 2.904 geometries of single-family houses in the form of annotated Point Clouds. The geometries are segmented in 3 classes: wall, roof, floor. The points of the point clouds are saved in .pts files while their labels are saved in .seg files. The dataset can be used to train 3D Generative Adversarial Neural Networks (GANs) for architectural applications, with architecturally relevant data.

---

<h3>Software packages</h3>
<h3>Technical reports</h3>


