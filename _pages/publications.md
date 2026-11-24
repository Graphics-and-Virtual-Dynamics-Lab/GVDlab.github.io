---
title: "GVD Lab - Publications"
layout: gridlay
excerpt: "GVD Lab - Research Publications and Patents."
sitemap: false
permalink: /publications/
---

<div class="gvd-publications" markdown="0">

<style>
/* =========================================
   GVD LAB - PUBLICATIONS REDESIGN
   ========================================= */

.gvd-publications {
  --ink: #0d1930;
  --navy: #102441;
  --teal: #61e3dc;
  --muted: #5f728a;
  --border: #dfe8f0;
  width: 100%;
  min-width: 0;
  color: #192c46;
  box-sizing: border-box;
}

.gvd-publications * {
  box-sizing: border-box;
}

/* HERO */

.gvd-publications .pub-hero {
  position: relative;
  overflow: hidden;
  background:
    radial-gradient(circle at 85% 20%,rgba(57,212,205,.18),transparent 40%),
    linear-gradient(135deg,#0b1529,#102441,#142f4c);
  color: #fff;
  padding: 48px 42px;
  margin: 18px 0 36px;
  border-radius: 24px;
  box-shadow: 0 18px 45px rgba(15,35,64,.13);
}

.gvd-publications .pub-eyebrow {
  color: #89ebe5;
  text-transform: uppercase;
  letter-spacing: .16em;
  font-size: 11px;
  font-weight: 800;
  margin-bottom: 14px;
}

.gvd-publications .pub-hero h1 {
  font-size: clamp(35px,5vw,55px);
  line-height: 1.1;
  letter-spacing: -.04em;
  font-weight: 800;
  color: #fff;
  margin: 0 0 18px;
}

.gvd-publications .pub-hero h1 span {
  color: #75e8e0;
}

.gvd-publications .pub-hero p {
  color: #d5e3f0;
  font-size: 16px;
  line-height: 1.8;
  max-width: 700px;
  margin: 0 0 24px;
}

/* BUTTONS */

.gvd-publications .pub-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.gvd-publications .pub-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 18px;
  border-radius: 10px;
  background: #61e3dc;
  color: #071c27;
  font-size: 14px;
  font-weight: 750;
  text-decoration: none;
  border: 1px solid transparent;
  transition: transform .2s ease,background .2s ease;
}

.gvd-publications .pub-button:hover {
  transform: translateY(-2px);
  background: #89eee8;
  color: #071c27;
  text-decoration: none;
}

.gvd-publications .pub-button-secondary {
  color: #fff;
  background: rgba(255,255,255,.07);
  border-color: rgba(255,255,255,.25);
}

.gvd-publications .pub-button-secondary:hover {
  background: rgba(255,255,255,.15);
  color: #fff;
}

/* SECTIONS */

.gvd-publications .pub-section {
  margin: 38px 0 45px;
  scroll-margin-top: 90px;
}

.gvd-publications .pub-kicker {
  color: #007e88;
  text-transform: uppercase;
  letter-spacing: .14em;
  font-size: 11px;
  font-weight: 800;
  margin: 0 0 8px;
}

.gvd-publications .pub-section h2 {
  color: #0d1930;
  font-size: clamp(25px,3vw,34px);
  font-weight: 800;
  letter-spacing: -.025em;
  line-height: 1.25;
  margin: 0 0 15px;
}

.gvd-publications .pub-section-lead {
  font-size: 15px;
  color: #5f728a;
  line-height: 1.75;
  margin-bottom: 24px;
}

/* FEATURED RESEARCH GRID */

.gvd-publications .pub-grid {
  display: grid;
  grid-template-columns: repeat(2,minmax(0,1fr));
  gap: 22px;
}

.gvd-publications .pub-card {
  display: flex;
  flex-direction: column;
  min-width: 0;
  height: 100%;
  overflow: hidden;
  border-radius: 17px;
  border: 1px solid #dfe8f0;
  background: #fff;
  box-shadow: 0 6px 20px rgba(15,35,64,.045);
  transition: transform .25s ease,box-shadow .25s ease;
}

.gvd-publications .pub-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 15px 32px rgba(15,35,64,.10);
}

.gvd-publications .pub-image {
  position: relative;
  height: 210px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  background: #f1f5f9;
  border-bottom: 1px solid #e4ebf2;
}

.gvd-publications .pub-image img {
  width: 100%;
  height: 100%;
  max-width: 100%;
  object-fit: contain;
  padding: 12px;
  margin: 0;
  border-radius: 0;
  box-shadow: none;
}

.gvd-publications .pub-image-fallback {
  display: none;
  color: #75e8e0;
  font-size: 13px;
  font-weight: 800;
  letter-spacing: .13em;
  text-transform: uppercase;
  text-align: center;
}

.gvd-publications .pub-image.no-image {
  background:
    radial-gradient(circle at 80% 20%,rgba(57,212,205,.18),transparent 40%),
    linear-gradient(135deg,#0b1529,#173652);
}

.gvd-publications .pub-image.no-image .pub-image-fallback {
  display: block;
}

/* CARD CONTENT */

.gvd-publications .pub-card-body {
  padding: 23px;
  display: flex;
  flex-direction: column;
  flex: 1;
}

.gvd-publications .pub-tag {
  align-self: flex-start;
  background: #e0f7f4;
  color: #087a80;
  border-radius: 6px;
  padding: 5px 9px;
  font-size: 10px;
  font-weight: 800;
  letter-spacing: .08em;
  text-transform: uppercase;
  margin-bottom: 13px;
}

.gvd-publications .pub-tag-award {
  background: #fff3d7;
  color: #94640c;
}

.gvd-publications .pub-card h3 {
  color: #102441;
  font-weight: 800;
  font-size: 17px;
  line-height: 1.5;
  margin: 0 0 12px;
}

.gvd-publications .pub-description {
  color: #40566c;
  font-size: 14px;
  line-height: 1.7;
  margin-bottom: 12px;
}

.gvd-publications .pub-authors {
  color: #5f728a;
  font-size: 13px;
  line-height: 1.7;
  margin: 0 0 15px;
  overflow-wrap: anywhere;
}

.gvd-publications .pub-venue {
  color: #263f56;
  font-size: 13px;
  line-height: 1.7;
  margin: 0 0 20px;
}

.gvd-publications .pub-read {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  align-self: flex-start;
  margin-top: auto;
  background: #102441;
  color: #fff;
  border-radius: 8px;
  padding: 10px 15px;
  font-size: 12px;
  font-weight: 700;
  text-decoration: none;
}

.gvd-publications .pub-read:hover {
  color: #fff;
  background: #146173;
  text-decoration: none;
}

/* PATENTS */

.gvd-publications .pub-patent {
  padding: 24px 26px;
  border: 1px solid #dfe8f0;
  border-left: 4px solid #159b98;
  border-radius: 14px;
  background: linear-gradient(135deg,#f0faf9,#f8fbfd);
  margin-bottom: 16px;
}

.gvd-publications .pub-patent h3 {
  margin: 8px 0 12px;
  font-size: 18px;
  line-height: 1.5;
  font-weight: 800;
  color: #102441;
}

.gvd-publications .pub-patent p {
  font-size: 14px;
  line-height: 1.7;
  color: #40566c;
}

.gvd-publications .pub-patent a {
  color: #087e88;
  font-weight: 700;
}

/* SEARCH AND FILTER CONTROLS */

.gvd-publications .pub-controls {
  display: grid;
  grid-template-columns: minmax(0,1fr) 160px;
  gap: 12px;
  padding: 18px;
  border: 1px solid #dfe8f0;
  background: #f6f9fc;
  border-radius: 14px;
  margin-bottom: 18px;
}

.gvd-publications .pub-control label {
  display: block;
  font-size: 12px;
  color: #40566c;
  font-weight: 700;
  margin-bottom: 7px;
}

.gvd-publications .pub-control input,
.gvd-publications .pub-control select {
  width: 100%;
  height: 44px;
  padding: 10px 13px;
  border: 1px solid #cddce7;
  background: #fff;
  border-radius: 8px;
  color: #192c46;
  font-family: inherit;
  font-size: 14px;
  outline-offset: 2px;
}

.gvd-publications .pub-control input:focus,
.gvd-publications .pub-control select:focus {
  border-color: #159b98;
  outline: 2px solid #b5e8e4;
}

.gvd-publications .pub-result-count {
  color: #5f728a;
  font-size: 13px;
  margin: 0 0 16px;
}

/* FULL PUBLICATION LIST */

.gvd-publications .pub-list {
  display: grid;
  gap: 12px;
}

.gvd-publications .pub-list-item {
  border: 1px solid #dfe8f0;
  border-radius: 12px;
  background: #fff;
  padding: 20px 22px;
  min-width: 0;
  overflow-wrap: anywhere;
  transition: border-color .2s ease,background .2s ease;
}

.gvd-publications .pub-list-item:hover {
  background: #f8fcfc;
  border-color: #a7dcd9;
}

.gvd-publications .pub-list-item[hidden] {
  display: none !important;
}

.gvd-publications .pub-list-title {
  color: #102441;
  font-size: 16px;
  font-weight: 750;
  line-height: 1.5;
  margin: 0 0 8px;
}

.gvd-publications .pub-list-authors {
  color: #5f728a;
  font-size: 13px;
  line-height: 1.7;
  margin: 0 0 8px;
}

.gvd-publications .pub-list-link {
  color: #087e88;
  font-size: 13px;
  font-weight: 700;
  line-height: 1.6;
}

.gvd-publications .pub-list-link:hover {
  color: #075a62;
  text-decoration: underline;
}

.gvd-publications .pub-empty {
  padding: 30px;
  text-align: center;
  border: 1px dashed #cddce7;
  color: #5f728a;
  border-radius: 12px;
}

.gvd-publications .pub-empty[hidden] {
  display: none !important;
}

/* FOOTER CTA */

.gvd-publications .pub-footer {
  padding: 25px 28px;
  margin: 35px 0;
  border-radius: 17px;
  background: linear-gradient(105deg,#103451,#146173);
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.gvd-publications .pub-footer h3 {
  font-size: 21px;
  color: #fff;
  font-weight: 800;
  margin: 0 0 8px;
}

.gvd-publications .pub-footer p {
  color: #d5e7ea;
  font-size: 14px;
  margin: 0;
}

/* MOBILE RESPONSIVENESS */

@media (max-width:767px) {

  .gvd-publications {
    padding-left: 16px;
    padding-right: 16px;
    max-width: 100%;
  }

  .gvd-publications .pub-hero {
    padding: 28px 22px;
    border-radius: 18px;
  }

  .gvd-publications .pub-hero h1 {
    font-size: 36px;
  }

  .gvd-publications .pub-hero p {
    font-size: 14px;
  }

  .gvd-publications .pub-section {
    margin-top: 32px;
    margin-bottom: 36px;
  }

  .gvd-publications .pub-section h2 {
    font-size: 26px;
  }

  .gvd-publications .pub-grid {
    grid-template-columns: minmax(0,1fr);
    gap: 17px;
  }

  .gvd-publications .pub-image {
    height: 190px;
  }

  .gvd-publications .pub-card-body {
    padding: 19px;
  }

  .gvd-publications .pub-controls {
    grid-template-columns: minmax(0,1fr);
    padding: 15px;
  }

  .gvd-publications .pub-list-item {
    padding: 17px;
  }

  .gvd-publications .pub-patent {
    padding: 20px;
  }

  .gvd-publications .pub-footer {
    flex-direction: column;
    align-items: flex-start;
    padding: 22px;
  }
}

@media (max-width:480px) {

  .gvd-publications .pub-actions {
    flex-direction: column;
  }

  .gvd-publications .pub-actions .pub-button {
    width: 100%;
  }

  .gvd-publications .pub-image {
    height: 170px;
  }
}

@media (prefers-reduced-motion:reduce) {

  .gvd-publications .pub-card,
  .gvd-publications .pub-button,
  .gvd-publications .pub-list-item {
    transition: none !important;
  }

  .gvd-publications .pub-card:hover,
  .gvd-publications .pub-button:hover {
    transform: none !important;
  }
}
</style>

<!-- ======================================
     PUBLICATION DATABASE
     Prefer updated records while retaining
     unique entries from both databases.
     ====================================== -->

{% assign publications = site.data.publist | concat: site.data.publist_2026 %}

<!-- HERO -->

<section class="pub-hero">

<p class="pub-eyebrow">GVD Lab · Scientific Contributions</p>

<h1>Research &amp; <span>Publications.</span></h1>

<p>
Explore our contributions to computer graphics, crowd simulation,
virtual reality, artificial intelligence, digital twins, and
human-centered virtual environments.
</p>

<div class="pub-actions">

<a class="pub-button" href="#full-list-of-publications">
Browse all publications &darr;
</a>

<a class="pub-button pub-button-secondary"
href="https://scholar.google.ca/citations?hl=en&amp;user=cTTXR50AAAAJ&amp;view_op=list_works&amp;sortby=pubdate"
target="_blank"
rel="noopener noreferrer">
Google Scholar &#8599;
</a>

</div>

</section>

<!-- ======================================
     FEATURED RESEARCH
     ====================================== -->

<section class="pub-section" id="research-highlights">

<p class="pub-kicker">Selected research</p>

<h2>Group highlights.</h2>

<p class="pub-section-lead">
Explore selected publications and award-winning contributions
from the Graphics and Virtual Dynamics Lab.
</p>

<div class="pub-grid">

{% assign seen_highlights = "|" %}

{% for publi in publications %}

{% assign title_key = publi.title | downcase | strip %}
{% assign publication_key = title_key | prepend: "|" | append: "|" %}

{% if seen_highlights contains publication_key %}
{% continue %}
{% endif %}

{% assign seen_highlights = seen_highlights | append: title_key | append: "|" %}

{% assign is_highlight = publi.highlight %}
{% assign image_name = publi.image %}

{% for original in site.data.publist_2026 %}

{% assign original_title = original.title | downcase | strip %}

{% if original_title == title_key %}

{% if original.highlight == 1 %}
{% assign is_highlight = 1 %}
{% endif %}

{% if image_name == "image.png" or image_name == blank %}
{% if original.image != blank and original.image != "image.png" %}
{% assign image_name = original.image %}
{% endif %}
{% endif %}

{% endif %}

{% endfor %}

{% assign venue_lower = publi.link.display | downcase %}
{% assign url_lower = publi.link.url | downcase %}

{% if venue_lower contains "patent application" or url_lower contains "/patent/" %}
{% continue %}
{% endif %}

{% if is_highlight == 1 %}

<article class="pub-card">

{% if image_name and image_name != empty and image_name != "image.png" %}

<div class="pub-image">

<img
src="{{ site.baseurl }}/images/pubpic/{{ image_name }}"
alt="{{ publi.title | escape }}"
loading="lazy"
onerror="this.style.display='none'; this.parentElement.classList.add('no-image');">

<span class="pub-image-fallback">
GVD Lab Research
</span>

</div>

{% else %}

<div class="pub-image no-image">

<span class="pub-image-fallback">
GVD Lab Research
</span>

</div>

{% endif %}

<div class="pub-card-body">

{% if publi.description contains "Best Paper Award" %}

<span class="pub-tag pub-tag-award">
&#9733; Best Paper Award
</span>

{% elsif publi.description contains "SAC Highlight Award" %}

<span class="pub-tag pub-tag-award">
&#9733; SAC Highlight Award
</span>

{% else %}

<span class="pub-tag">
Featured research
</span>

{% endif %}

<h3>{{ publi.title | escape }}</h3>

{% if publi.description and publi.description != empty %}

<p class="pub-description">
{{ publi.description }}
</p>

{% endif %}

<p class="pub-authors">
<em>{{ publi.authors | escape }}</em>
</p>

<p class="pub-venue">
{{ publi.link.display }}
</p>

{% if publi.news1 and publi.news1 != empty %}

<p class="pub-description">
<strong>{{ publi.news1 }}</strong>
</p>

{% endif %}

<a class="pub-read"
href="{{ publi.link.url | escape }}"
target="_blank"
rel="noopener noreferrer">
Read publication &#8599;
</a>

</div>

</article>

{% endif %}

{% endfor %}

</div>

</section>

<!-- ======================================
     PATENTS
     ====================================== -->

<section class="pub-section" id="patents">

<p class="pub-kicker">Innovation</p>

<h2>Patents.</h2>

<p class="pub-section-lead">
Research contributions to intellectual property and
emerging technologies.
</p>

{% assign seen_patents = "|" %}
{% assign patent_count = 0 %}

{% for publi in publications %}

{% assign venue_lower = publi.link.display | downcase %}
{% assign url_lower = publi.link.url | downcase %}

{% if venue_lower contains "patent application" or url_lower contains "/patent/" %}

{% assign patent_title = publi.title | downcase | strip %}
{% assign patent_key = patent_title | prepend: "|" | append: "|" %}

{% if seen_patents contains patent_key %}
{% continue %}
{% endif %}

{% assign seen_patents = seen_patents | append: patent_title | append: "|" %}
{% assign patent_count = patent_count | plus: 1 %}

<article class="pub-patent">

<span class="pub-tag">Patent application</span>

<h3>{{ publi.title | escape }}</h3>

<p>
<em>{{ publi.authors | escape }}</em>
</p>

{% if publi.link.display contains "18/891,586" %}

<p>Application filed in 2024.</p>

{% endif %}

<p>
{{ publi.link.display }}
</p>

<a href="{{ publi.link.url | escape }}"
target="_blank"
rel="noopener noreferrer">
View patent record &#8599;
</a>

</article>

{% endif %}

{% endfor %}

{% if patent_count == 0 %}

<article class="pub-patent">

<span class="pub-tag">Patent application</span>

<h3>
Selective Multi-View Deep Model for 3D Object Classification
</h3>

<p>
<em>
Mona Alzahrani, Muhammad Usman, Saeed Anwar, Tarek Helmy
</em>
</p>

<p>US Patent Application 18/891,586 — filed in 2024.</p>

</article>

{% endif %}

</section>

<!-- ======================================
     FULL PUBLICATION LIST
     ====================================== -->

<section class="pub-section" id="full-list-of-publications">

<p class="pub-kicker">Publication archive</p>

<h2>Full list of publications.</h2>

<p class="pub-section-lead">
Browse the lab's research contributions, search for a paper,
or filter publications by year.
</p>

<div class="pub-controls">

<div class="pub-control">

<label for="gvd-pub-search">
Search publications
</label>

<input
type="search"
id="gvd-pub-search"
placeholder="Search titles, authors, journals..."
autocomplete="off">

</div>

<div class="pub-control">

<label for="gvd-pub-year">
Publication year
</label>

<select id="gvd-pub-year">
<option value="all">All years</option>
</select>

</div>

</div>

<p class="pub-result-count"
id="gvd-pub-count"
aria-live="polite">
Showing all publications
</p>

<div class="pub-list" id="gvd-publication-list">

{% assign seen_publications = "|" %}

{% for publi in publications %}

{% assign venue_lower = publi.link.display | downcase %}
{% assign url_lower = publi.link.url | downcase %}

{% if venue_lower contains "patent application" or url_lower contains "/patent/" %}
{% continue %}
{% endif %}

{% assign title_key = publi.title | downcase | strip %}
{% assign publication_key = title_key | prepend: "|" | append: "|" %}

{% if seen_publications contains publication_key %}
{% continue %}
{% endif %}

{% assign seen_publications = seen_publications | append: title_key | append: "|" %}

<article class="pub-list-item"
data-venue="{{ publi.link.display | escape }}">

<h3 class="pub-list-title">
{{ publi.title | escape }}
</h3>

<p class="pub-list-authors">
<em>{{ publi.authors | escape }}</em>
</p>

<a class="pub-list-link"
href="{{ publi.link.url | escape }}"
target="_blank"
rel="noopener noreferrer">
{{ publi.link.display }} &#8599;
</a>

</article>

{% endfor %}

</div>

<div class="pub-empty" id="gvd-pub-empty" hidden>

No publications match your search. Try another keyword or year.

</div>

</section>

<!-- ======================================
     GOOGLE SCHOLAR CTA
     ====================================== -->

<section class="pub-footer">

<div>

<h3>Explore our scholarly contributions.</h3>

<p>
Visit Dr. Muhammad Usman's Google Scholar profile
for publication records and citation information.
</p>

</div>

<a class="pub-button"
href="https://scholar.google.ca/citations?hl=en&amp;user=cTTXR50AAAAJ&amp;view_op=list_works&amp;sortby=pubdate"
target="_blank"
rel="noopener noreferrer">
Google Scholar &#8599;
</a>

</section>

</div>

<!-- ======================================
     PUBLICATION SEARCH AND YEAR FILTER
     ====================================== -->

<script>
(function () {
  'use strict';

  var search = document.getElementById('gvd-pub-search');
  var yearFilter = document.getElementById('gvd-pub-year');
  var count = document.getElementById('gvd-pub-count');
  var empty = document.getElementById('gvd-pub-empty');
  var list = document.getElementById('gvd-publication-list');

  if (!search || !yearFilter || !count || !empty || !list) {
    return;
  }

  var items = Array.prototype.slice.call(
    list.querySelectorAll('.pub-list-item')
  );

  var years = [];

  items.forEach(function (item) {

    var venue = item.getAttribute('data-venue') || '';

    var matches = venue.match(
      /\b(?:19\d{2}|20\d{2})\b/g
    );

    var year = matches
      ? matches[matches.length - 1]
      : '';

    item.setAttribute('data-year',year);

    if (year && years.indexOf(year) === -1) {
      years.push(year);
    }

  });

  years.sort(function (a,b) {
    return Number(b) - Number(a);
  });

  years.forEach(function (year) {

    var option = document.createElement('option');

    option.value = year;
    option.textContent = year;

    yearFilter.appendChild(option);

  });

  function filterPublications() {

    var query = search.value
      .trim()
      .toLowerCase();

    var selectedYear = yearFilter.value;

    var visible = 0;

    items.forEach(function (item) {

      var text = item.textContent.toLowerCase();

      var itemYear = item.getAttribute('data-year');

      var matchesSearch =
        query === '' || text.indexOf(query) !== -1;

      var matchesYear =
        selectedYear === 'all' ||
        selectedYear === itemYear;

      var show = matchesSearch && matchesYear;

      item.hidden = !show;

      if (show) {
        visible++;
      }

    });

    count.textContent =
      'Showing ' + visible + ' of ' +
      items.length + ' publications';

    empty.hidden = visible !== 0;
  }

  search.addEventListener('input',filterPublications);

  yearFilter.addEventListener(
    'change',
    filterPublications
  );

  filterPublications();

})();
</script>
