---
layout: page
title: Home
permalink: /
---

<div class="home-hero">
  <div>
    <p>I’m <strong>Adela Bubenikova</strong>, a neuroscience researcher originally based in Prague—though these days I’m often elsewhere. I work close to neurosurgery, using neuroimaging and quantitative methods to ask how brains become lives.</p>

    <p>
      I’m part of <a href="https://praguebrainsgroup.com/" target="_blank" rel="noopener">PragueBrainsGroup</a> and I study at the
      <a href="https://www.lf2.cuni.cz/en" target="_blank" rel="noopener">Second Faculty of Medicine, Charles University</a>.
      I also write science communication for <a href="https://vesmir.cz/" target="_blank" rel="noopener">Vesmír</a>, and I teach.
    </p>

    <p>Alongside research, I write essays. This site holds careful work with data, and careful attention to experience. I’m interested in learning—how it fails, how it returns, and what we do when answers don’t.</p>

    <p>I was lucky to begin research at a young age, supported by generous mentors and an academic community that opened doors for me. I’m keen to help ambitious undergraduates take their first steps into academia in the same spirit.<a href="mailto:bubenikova.adela.ab@gmail.com"><strong>Please get in touch.</strong></a></p>

    <p>If you’re trying to find me in person, you’ll have better luck by email than by geography.</p>
  </div>

  <img class="avatar" src="/assets/img/profile.jpg" alt="Adela Bubenikova">
</div>

---

## Explore

- **Research** → [/research/](/research/)
- **Publications** → [/publications/](/publications/)
- **Blog** → [/blog/](/blog/)
- **Contact** → [/contact/](/contact/)

---

## Latest

{% for post in site.posts limit:8 %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
