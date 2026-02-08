---
layout: default
title: Curriculum Vitae
permalink: /cv/
---

<div class="cv-download">
  <a href="{{ "/assets/files/cv.pdf" | relative_url }}" class="btn">Download Full CV (PDF)</a>
</div>

## Education
{% for edu in site.data.education %}
<div class="cv-item">
  <div class="cv-header">
    <h3>{{ edu.degree }}</h3>
    <span class="cv-date">{{ edu.years }}</span>
  </div>
  <div class="cv-sub">
    <strong>{{ edu.university }}</strong>, {{ edu.location }}
  </div>
  {% if edu.thesis_title %}
  <p class="cv-detail">Thesis: <em>{{ edu.thesis_title }}</em></p>
  {% endif %}
</div>
{% endfor %}

## Experience
{% for exp in site.data.experience %}
<div class="cv-item">
  <div class="cv-header">
    <h3>{{ exp.role }}</h3>
    <span class="cv-date">{{ exp.dates }}</span>
  </div>
  <div class="cv-sub">
    <strong>{{ exp.company }}</strong>, {{ exp.location }}
  </div>
  <ul class="cv-bullets">
    {% for point in exp.bullet_points %}
    <li>{{ point }}</li>
    {% endfor %}
  </ul>
</div>
{% endfor %}

## Publications
{% for pub in site.data.publications %}
<div class="cv-item">
  <div class="cv-header">
    <h3><a href="{{ pub.pdf_link }}">{{ pub.title }}</a></h3>
    <span class="cv-date">{{ pub.year }}</span>
  </div>
  <p class="cv-detail">{{ pub.authors }}</p>
  <p class="cv-detail" style="font-style: italic;">{{ pub.journal }}</p>
</div>
{% endfor %}

## Conferences & Talks
{% for conf in site.data.conferences %}
<div class="cv-item">
  <div class="cv-header">
    <h3>{{ conf.title }} <span class="cv-type">[{{ conf.type }}]</span></h3>
    <span class="cv-date">{{ conf.date }}</span>
  </div>
  <div class="cv-sub">
    {{ conf.event }}, {{ conf.location }}
  </div>
</div>
{% endfor %}

## Awards & Honors
{% for award in site.data.awards %}
<div class="cv-item">
  <div class="cv-header">
    <h3>{{ award.award_name }}</h3>
    <span class="cv-date">{{ award.date }}</span>
  </div>
  <div class="cv-sub">
    {{ award.organization }}
  </div>
</div>
{% endfor %}
