---
layout: default
title: Publications
permalink: /publications/
---

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
