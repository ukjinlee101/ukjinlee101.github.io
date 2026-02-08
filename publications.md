---
layout: default
title: Publications
permalink: /publications/
---

## Publications

{% for pub in site.data.publications %}
<div class="cv-item pub-item">
  {% if pub.image %}
  <div class="pub-image">
    <img src="{{ pub.image | relative_url }}" alt="{{ pub.title }}">
  </div>
  {% endif %}
  <div class="pub-content">
    <div class="cv-header">
      <h3><a href="{{ pub.pdf_link }}">{{ pub.title }}</a></h3>
      <span class="cv-date">{{ pub.year }}</span>
    </div>
    <p class="cv-detail">{{ pub.authors | replace: "UkJin Lee", "<strong>UkJin Lee</strong>" }}</p>
    <p class="cv-detail" style="font-style: italic;">{{ pub.journal }}</p>
  </div>
</div>
{% endfor %}
