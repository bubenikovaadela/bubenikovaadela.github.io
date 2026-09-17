---
layout: page
title: Home
hide_title: true
permalink: /
---

<div class="home-intro">
  <img class="home-photo" src="{{ "/assets/img/profile.jpg" | relative_url }}" alt="Adela Bubenikova">

  <p>I’m <strong>Adela Bubenikova</strong>, a medical student and neuroscience researcher from Prague, usually working somewhere close to neurosurgery. I’m interested in neuroimaging, quantitative methods, and questions about how brains become lives.</p>

  <p>I’m part of <a href="https://praguebrainsgroup.com/" target="_blank" rel="noopener">PragueBrainsGroup</a> and study at the <a href="https://www.lf2.cuni.cz/en" target="_blank" rel="noopener">Second Faculty of Medicine, Charles University</a>. I also write science communication for <a href="https://vesmir.cz/" target="_blank" rel="noopener">Vesmír</a>.</p>

  <p>This site is where I keep research, writing, and things I am still trying to understand.</p>
</div>

<hr>

<section class="home-section">
  <div class="section-heading-row">
    <h2>Writing</h2>
    <a class="section-link" href="{{ "/blog/" | relative_url }}">All writing →</a>
  </div>
  <p class="section-kicker">Essays and notes on science, medicine, technology, and the questions I keep coming back to.</p>
  <ul class="essay-list">
  {% for post in site.posts limit:7 %}
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
</section>

<hr>

<section class="home-section">
  <h2>Research</h2>
  <p>My research sits around neurosurgery, neuroimaging, cerebrovascular disease, hydrocephalus, brain-fluid physiology, and quantitative clinical methods.</p>
  <p class="inline-links"><a href="{{ "/research/" | relative_url }}">Research</a> · <a href="{{ "/publications/" | relative_url }}">Publications</a></p>
</section>

<hr>

<section class="home-section">
  <h2>Contact</h2>
  <p>I was lucky to begin research early, helped by generous mentors and academic communities that opened doors for me. I’m always happy to hear from students trying to find their first way into research.</p>
  <p class="inline-links"><a href="mailto:bubenikova.adela.ab@gmail.com">Email</a> · <a href="https://www.linkedin.com/in/adela-bubenikova-2a273718a/?originalSubdomain=cz" target="_blank" rel="noopener">LinkedIn</a></p>
</section>
