---
layout: default
title: Home
permalink: /
---

# Ukjin Lee

Hello! I am a Ph.D.
You can find my CV [here]({{ "/cv" | relative_url }}) and read my latest blog posts [here]({{ "/blog" | relative_url }}).

## Latest Posts

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
    </li>
  {% endfor %}
</ul>
