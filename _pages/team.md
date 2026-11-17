---
title: "GVD Lab - Team"
layout: gridlay
excerpt: "GVD Lab: Team members"
sitemap: false
permalink: /team/
---

# People

**We are looking for new PhD and Master students to join the team** [(see openings)]({{ site.baseurl }}/open-positions) **!**

Jump to [PIs](#principal-investigator), [Current Students](#current-students), [Alumni](#alumni), [External Collaborators](#external-collaborators), or [Administrative Support](#administrative-support).

## Principal Investigator

{% assign number_printed = 0 %}
{% for member in site.data.pi_members %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-right: 15px;" alt="{{ member.name | escape }}">
<h4>{{ member.name }}</h4>
<i>{{ member.info }}</i>
<ul style="overflow: hidden;">
{% if member.number_educ == 1 %}
<li>{{ member.education1 }}</li>
{% endif %}
{% if member.number_educ == 2 %}
<li>{{ member.education1 }}</li>
<li>{{ member.education2 }}</li>
{% endif %}
{% if member.number_educ == 3 %}
<li>{{ member.education1 }}</li>
<li>{{ member.education2 }}</li>
<li>{{ member.education3 }}</li>
{% endif %}
{% if member.number_educ == 4 %}
<li>{{ member.education1 }}</li>
<li>{{ member.education2 }}</li>
<li>{{ member.education3 }}</li>
<li>{{ member.education4 }}</li>
{% endif %}
{% if member.number_educ == 5 %}
<li>{{ member.education1 }}</li>
<li>{{ member.education2 }}</li>
<li>{{ member.education3 }}</li>
<li>{{ member.education4 }}</li>
<li>{{ member.education5 }}</li>
{% endif %}
</ul>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Current Students

{% assign student_categories = "PhD|Masters|Undergrad|Visiting" | split: "|" %}
{% for category in student_categories %}
{% assign category_members = site.data.current_members | where: "category", category %}

<h3 id="students-{{ category | downcase }}">{{ category }}</h3>

{% if category_members.size > 0 %}
<div class="row">
{% for member in category_members %}
<div class="col-sm-6" style="margin-bottom: 30px;">
<div style="display: flex; flex-wrap: wrap; gap: 16px; align-items: flex-start;">
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="{{ member.name | escape }}" loading="lazy" style="width: 110px; max-width: 100%; height: 130px; object-fit: cover; border-radius: 8px; box-shadow: 0 2px 6px rgba(0,0,0,0.15); flex-shrink: 0;">
<div style="flex: 1; min-width: 160px; overflow-wrap: anywhere;">
<h4 style="margin-top: 0;">{{ member.name | escape }}</h4>
{% if member.info %}
<p><i>Role: {{ member.info | escape }}</i></p>
{% endif %}
{% if member.supervisors and member.supervisors.size > 0 %}
<p><strong>{% if member.supervisors.size > 1 %}Supervisors:{% else %}Supervisor:{% endif %}</strong> {{ member.supervisors | join: ", " | escape }}</p>
{% elsif member.education1 %}
<p>{{ member.education1 }}</p>
{% endif %}
{% if member.projects and member.projects.size > 0 %}
<p><strong>Research Projects:</strong></p>
<ul style="padding-left: 20px; margin-top: 6px;">
{% for project in member.projects %}
<li style="margin-bottom: 8px;">{{ project.title | escape }}{% if project.status == "previous" %} <small style="color: #777;">(Previous project)</small>{% endif %}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>
{% endfor %}
</div>
{% else %}
<p style="color: #777;">No students currently listed in this category.</p>
{% endif %}
{% endfor %}

## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix" style="margin-bottom: 25px;">
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-right: 15px; border-radius: 8px;" alt="{{ member.name | escape }}" loading="lazy">
<h4>{{ member.name }}</h4>
{% if member.duration %}
<p><i>{{ member.duration }}</i></p>
{% endif %}
{% if member.info %}
<p><i>Role: {{ member.info }}</i></p>
{% endif %}
{% if member.education1 %}
<ul style="overflow: hidden; margin-top: 10px;">
<li>{{ member.education1 }}</li>
</ul>
{% endif %}
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## External Collaborators

{% assign number_printed = 0 %}
{% for member in site.data.external_collaborators %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix" style="margin-bottom: 25px;">
<img src="{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-right: 15px;" alt="{{ member.name | escape }}" loading="lazy">
<h4>{{ member.name }}</h4>
<i>{{ member.info }}</i>
<ul style="overflow: hidden;">
{% if member.number_research == 1 %}
<li>{{ member.research1 }}</li>
{% endif %}
{% if member.number_research == 2 %}
<li>{{ member.research1 }}</li>
<li>{{ member.research2 }}</li>
{% endif %}
{% if member.number_research == 3 %}
<li>{{ member.research1 }}</li>
<li>{{ member.research2 }}</li>
<li>{{ member.research3 }}</li>
{% endif %}
{% if member.number_research == 4 %}
<li>{{ member.research1 }}</li>
<li>{{ member.research2 }}</li>
<li>{{ member.research3 }}</li>
<li>{{ member.research4 }}</li>
{% endif %}
{% if member.number_research == 5 %}
<li>{{ member.research1 }}</li>
<li>{{ member.research2 }}</li>
<li>{{ member.research3 }}</li>
<li>{{ member.research4 }}</li>
<li>{{ member.research5 }}</li>
{% endif %}
</ul>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Administrative Support

Reach out to <a href="mailto:muhammad.usman8@ontariotechu.ca">GVD lab</a>.
