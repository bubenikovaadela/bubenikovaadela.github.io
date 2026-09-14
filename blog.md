---
layout: page
title: Essays
permalink: /blog/
---

<ul class="writing-list">
{% for post in site.posts %}
  <li class="writing-item">
    <div class="writing-title-line">
      <a class="writing-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="writing-date">· {{ post.date | date: "%b %Y" }}</span>
    </div>
    {% if post.subtitle %}
      <p class="writing-description">{{ post.subtitle }}</p>
    {% elsif post.description %}
      <p class="writing-description">{{ post.description }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
