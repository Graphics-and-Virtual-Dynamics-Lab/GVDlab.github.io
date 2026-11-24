---
title: "GVD Lab - Team"
layout: gridlay
excerpt: "Meet the researchers and students of the Graphics and Virtual Dynamics Lab."
sitemap: false
permalink: /team/
---

<div class="gvd-page" markdown="0">

<section class="gvd-page-hero">
<p class="gvd-eyebrow">GVD Lab · Our people</p>
<h1>Meet the <span>team.</span></h1>
<p>Meet the researchers, students, alumni, and collaborators behind the Graphics and Virtual Dynamics Lab at Ontario Tech University.</p>
<div class="gvd-page-actions">
<a class="gvd-action" href="{{ '/open-positions' | relative_url }}">Join our team &rarr;</a>
<a class="gvd-action gvd-action-outline" href="#current-students">Meet our students &darr;</a>
</div>
</section>

<nav class="gvd-team-nav" aria-label="Team sections">
<a href="#principal-investigator">Principal Investigator</a>
<a href="#current-students">Current Students</a>
<a href="#alumni">Alumni</a>
<a href="#external-collaborators">External Collaborators</a>
<a href="#administrative-support">Administrative Support</a>
</nav>

<!-- PRINCIPAL INVESTIGATOR -->

<section class="gvd-page-section" id="principal-investigator">
<p class="gvd-page-kicker">Lab leadership</p>
<h2>Principal Investigator.</h2>
<div class="gvd-profile-grid">

{% for member in site.data.pi_members %}

<article class="gvd-profile gvd-pi-profile">
<div class="gvd-profile-photo">
{% if member.photo and member.photo != empty %}
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name | escape }}" onerror="this.style.display='none'; this.nextElementSibling.hidden=false;">
<span hidden>GVD Lab</span>
{% else %}
<span>GVD Lab</span>
{% endif %}
</div>

<div class="gvd-profile-body">
<span class="gvd-label">Principal Investigator</span>
<h3>{{ member.name | escape }}</h3>

{% if member.info %}
<p class="gvd-profile-role">{{ member.info }}</p>
{% endif %}

{% assign education_fields = "education1|education2|education3|education4|education5" | split: "|" %}

<ul>
{% for field in education_fields %}
{% assign education = member[field] %}
{% if education and education != empty %}
<li>{{ education }}</li>
{% endif %}
{% endfor %}
</ul>

</div>
</article>

{% endfor %}

</div>
</section>

<!-- CURRENT STUDENTS -->

<section class="gvd-page-section" id="current-students">
<p class="gvd-page-kicker">Emerging researchers</p>
<h2>Current Students.</h2>
<p class="gvd-page-section-lead">Our students explore research across crowd dynamics, virtual reality, computer graphics, and intelligent virtual environments.</p>

{% assign student_categories = "PhD|Masters|Undergrad|Visiting" | split: "|" %}

{% for category in student_categories %}

{% assign category_members = site.data.current_members | where: "category", category %}

<h3 class="gvd-category-heading" id="students-{{ category | downcase }}">{{ category }}</h3>

{% if category_members.size > 0 %}

<div class="gvd-profile-grid">

{% for member in category_members %}

<article class="gvd-profile">

<div class="gvd-profile-photo">
{% if member.photo and member.photo != empty %}
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name | escape }}" loading="lazy" onerror="this.style.display='none'; this.nextElementSibling.hidden=false;">
<span hidden>GVD Lab</span>
{% else %}
<span>GVD Lab</span>
{% endif %}
</div>

<div class="gvd-profile-body">

<span class="gvd-label">{{ category }}</span>

<h4>{{ member.name | escape }}</h4>

{% if member.info %}
<p class="gvd-profile-role">{{ member.info | escape }}</p>
{% endif %}

{% if member.supervisors and member.supervisors.size > 0 %}

<p>
<strong>{% if member.supervisors.size > 1 %}Supervisors:{% else %}Supervisor:{% endif %}</strong>
{{ member.supervisors | join: ", " | escape }}
</p>

{% elsif member.education1 %}

<p>{{ member.education1 }}</p>

{% endif %}

{% if member.projects and member.projects.size > 0 %}

<p><strong>Research Projects:</strong></p>

<ul>
{% for project in member.projects %}
<li>
{{ project.title | escape }}
{% if project.status == "previous" %}
<small style="color:#5f728a;">(Previous project)</small>
{% endif %}
</li>
{% endfor %}
</ul>

{% endif %}

</div>
</article>

{% endfor %}

</div>

{% else %}

<div class="gvd-empty-state">
No students currently listed in this category.
</div>

{% endif %}

{% endfor %}

</section>

<!-- ALUMNI -->

<section class="gvd-page-section" id="alumni">

<p class="gvd-page-kicker">Our research community</p>
<h2>Alumni.</h2>

<p class="gvd-page-section-lead">
Former members of GVD Lab and the researchers who have contributed to its work.
</p>

<div class="gvd-profile-grid">

{% for member in site.data.alumni_members %}

<article class="gvd-profile">

<div class="gvd-profile-photo">
{% if member.photo and member.photo != empty %}
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name | escape }}" loading="lazy" onerror="this.style.display='none'; this.nextElementSibling.hidden=false;">
<span hidden>GVD Lab</span>
{% else %}
<span>GVD Lab</span>
{% endif %}
</div>

<div class="gvd-profile-body">

<h4>{{ member.name | escape }}</h4>

{% if member.duration %}
<p class="gvd-profile-role">{{ member.duration }}</p>
{% endif %}

{% if member.info %}
<p><strong>Role:</strong> {{ member.info }}</p>
{% endif %}

{% assign education_fields = "education1|education2|education3|education4|education5" | split: "|" %}

<ul>
{% for field in education_fields %}
{% assign education = member[field] %}
{% if education and education != empty %}
<li>{{ education }}</li>
{% endif %}
{% endfor %}
</ul>

</div>
</article>

{% endfor %}

</div>

</section>

<!-- EXTERNAL COLLABORATORS -->

<section class="gvd-page-section" id="external-collaborators">

<p class="gvd-page-kicker">Research partnerships</p>
<h2>External Collaborators.</h2>

<p class="gvd-page-section-lead">
Meet the collaborators who contribute expertise and new perspectives to our research.
</p>

<div class="gvd-profile-grid">

{% for member in site.data.external_collaborators %}

<article class="gvd-profile">

<div class="gvd-profile-photo">
{% if member.photo and member.photo != empty %}
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name | escape }}" loading="lazy" onerror="this.style.display='none'; this.nextElementSibling.hidden=false;">
<span hidden>GVD Lab</span>
{% else %}
<span>GVD Lab</span>
{% endif %}
</div>

<div class="gvd-profile-body">

<h4>{{ member.name | escape }}</h4>

{% if member.info %}
<p class="gvd-profile-role">{{ member.info }}</p>
{% endif %}

{% assign research_fields = "research1|research2|research3|research4|research5" | split: "|" %}

<ul>
{% for field in research_fields %}
{% assign research = member[field] %}
{% if research and research != empty %}
<li>{{ research }}</li>
{% endif %}
{% endfor %}
</ul>

</div>
</article>

{% endfor %}

</div>
</section>

<!-- ADMINISTRATIVE SUPPORT -->

<section class="gvd-page-section" id="administrative-support">

<p class="gvd-page-kicker">Get in touch</p>
<h2>Administrative Support.</h2>

<div class="gvd-panel">

<h3>Contact GVD Lab</h3>

<p>For administrative inquiries, recruitment questions, or research-related information, please contact the lab.</p>

<a class="gvd-action gvd-action-dark" href="mailto:muhammad.usman8@ontariotechu.ca">Contact the lab &#8599;</a>

</div>

</section>

</div>
