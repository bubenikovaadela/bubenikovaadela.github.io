---
layout: page
title: Writing
permalink: /blog/
---

<p class="writing-intro">Essays and notes on science, medicine, technology, and the questions I keep coming back to.</p>

<ul class="essay-list essay-list--writing">
{% for post in site.posts %}
  <li class="essay-item">
    <div class="essay-line">
      <a class="essay-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="essay-date"> · {{ post.date | date: "%b %Y" }}</span>
    </div>
    {% if post.description %}
      <p class="essay-description">{{ post.description }}</p>
    {% elsif post.subtitle %}
      <p class="essay-description">{{ post.subtitle }}</p>
    {% else %}
      <p class="essay-description">{{ post.excerpt | strip_html | strip_newlines | truncate: 145 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
