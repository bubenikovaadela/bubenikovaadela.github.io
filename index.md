---
layout: page
title: Home
hide_title: true
permalink: /
---

<div class="home-hero">
  <div>
    <p>I’m <strong>Adela Bubenikova</strong>, a neuroscience researcher and medical student from Prague, usually working somewhere close to neurosurgery. I’m interested in neuroimaging, quantitative methods, and questions about how brains become lives.</p>

    <p>I’m part of <a href="https://praguebrainsgroup.com/" target="_blank" rel="noopener">PragueBrainsGroup</a> and study at the <a href="https://www.lf2.cuni.cz/en" target="_blank" rel="noopener">Second Faculty of Medicine, Charles University</a>. I also write science communication for <a href="https://vesmir.cz/" target="_blank" rel="noopener">Vesmír</a>, and I teach.</p>

    <p>Alongside research, I write essays about science, attention, learning, ambition, and the parts of life that resist being made useful.</p>
  </div>

  <img class="avatar" src="/assets/img/profile.jpg" alt="Adela Bubenikova">
</div>

<hr>

<section class="home-section">
  <h2>Essays</h2>

  <ul class="writing-list">
  {% for post in site.posts limit:8 %}
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

  <p><a href="{{ "/blog/" | relative_url }}">All writing →</a></p>
</section>

<hr>

<section class="home-section">
  <h2>Research</h2>

  <p>My research sits around neurosurgery, neuroimaging, cerebrovascular disease, hydrocephalus, brain-fluid physiology, and quantitative clinical methods.</p>

  <p>
    <a href="{{ "/research/" | relative_url }}">Research projects →</a><br>
    <a href="{{ "/publications/" | relative_url }}">Publications →</a>
  </p>
</section>

<hr>

<section class="home-section">
  <h2>Contact</h2>

  <p>I was lucky to begin research early, helped by generous mentors and academic communities that opened doors for me. I’m always happy to hear from students trying to find their first way into research.</p>

  <p><a href="mailto:bubenikova.adela.ab@gmail.com">bubenikova.adela.ab@gmail.com</a></p>
</section>
