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
  • A dataset containing titles of journal issues, and article titles from the journal Architectural Design (2005-2024) and the titles and abstracts of winning projects and honourable mentions of the eVolo skyscraper competition (2006-2024). This can be used in promt engineering or in training AI models with language that is specific to the field of architecture:

  ComPara: A Corpus Linguistics Dataset of Computation in Architecture. 2022. Anca-Simona Horvath. Mendeley Data <a href="https://doi.org/10.17632/7ktscvmxvg.5" target="_blank">DOI</a>

---
• A dataset containing 2.904 geometries of single-family houses in the form of annotated Point Clouds, and was developed in order to train 3D Generative Adversarial Networks. The geometries are segmented within 3 classes: wall, roof, floor. The points of the point clouds are saved in .pts files while their labels are saved in .seg files.

The creation of the dataset was done in a semi-automated way that consists of two stages:
a) creation of module geometries representing building components (done in Rhino3D)
b) the conversion of the geometries into Point Clouds with the Cockroach plug-in.

25 wall modules and 35 roof modules were created. Each wall module was combined with each roof module. Data augmentation methods were applied to maximize the size of the dataset: the modules were scaled in 3 ranges, and rotated 90 degrees for a wider feature space. 

  Annotated point clouds of buildings: a segmented dataset of single-family houses. 2022. Panagiota Pouliou, Anca-Simona Horvath, George Palamas. Mendeley Data. <a href="https://doi.org/10.17632/3thtp7mc6z.1" target="_blank">DOI</a>

---
  
  
- Software packages
- Technical reports


