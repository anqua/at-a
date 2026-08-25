---
layout: default
title: Outputs
---

<div id="outputs">

<h3>JOURNAL ARTICLES</h3>
<div class="pubs-grid">
{% assign sorted_journals = site.data.publications | where: "type", "article" | sort: "year" | reverse %}
{% for pub in sorted_journals %}
  {% include pub-card.html pub=pub %}
{% endfor %}
</div>

<h3>CONFERENCE PAPERS</h3>
<div class="pubs-grid">
{% assign sorted_confs = site.data.publications | where: "type", "conference" | sort: "year" | reverse %}
{% for pub in sorted_confs %}
  {% include pub-card.html pub=pub %}
{% endfor %}
</div>

<h3>BOOK CHAPTERS</h3>
<div class="pubs-grid">
{% assign sorted_chapters = site.data.publications | where: "type", "bookchapter" | sort: "year" | reverse %}
{% for pub in sorted_chapters %}
  {% include pub-card.html pub=pub %}
{% endfor %}
</div>

<h3>PREPRINTS</h3>
<div class="pubs-grid">
{% assign sorted_preprints = site.data.publications | where: "type", "preprint" | sort: "year" | reverse %}
{% for pub in sorted_preprints %}
  {% include pub-card.html pub=pub %}
{% endfor %}
</div>

<h3>Art and Design Exhibitions</h3>

<p>2 art exhibitions in the making!</p>

<h3>DATASETS</h3>
<div class="pubs-grid">
{% assign sorted_datasets = site.data.publications | where: "type", "dataset" | sort: "year" | reverse %}
{% for pub in sorted_datasets %}
  {% include pub-card.html pub=pub %}
{% endfor %}
</div>

</div>

<script>
document.addEventListener('click', function (e) {
  var toggleBtn = e.target.closest('.pub-bibtex-toggle');
  if (toggleBtn) {
    var target = document.getElementById(toggleBtn.dataset.target);
    if (!target) return;
    if (target.hasAttribute('hidden')) {
      target.removeAttribute('hidden');
      toggleBtn.textContent = 'Hide BibTeX';
    } else {
      target.setAttribute('hidden', '');
      toggleBtn.textContent = 'BibTeX';
    }
    return;
  }

  var copyBtn = e.target.closest('.pub-copy');
  if (copyBtn) {
    var pre = document.getElementById(copyBtn.dataset.target);
    if (pre && navigator.clipboard) {
      navigator.clipboard.writeText(pre.textContent.trim()).then(function () {
        var original = copyBtn.textContent;
        copyBtn.textContent = 'Copied!';
        setTimeout(function () { copyBtn.textContent = original; }, 1500);
      });
    }
  }
});
</script>
