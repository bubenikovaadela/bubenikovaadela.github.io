---
layout: page
title: Home
permalink: /
---

<div class="home-hero">
  <img class="avatar" src="/assets/img/profile.jpg" alt="Adela Bubenikova">
  <div>
    <p>I’m <strong>Adela Bubenikova</strong>, a neuroscience researcher originally based in Prague—though these days I’m often elsewhere. I work close to neurosurgery, using neuroimaging and quantitative methods to ask how brains become lives.</p>

    <p>Alongside research, I write essays and make photographs. This site holds both sides of my life: careful work with data, and careful attention to experience. I’m interested in learning—how it fails, how it returns, and what we do when answers don’t.</p>

    <p>I had the good fortune to begin research at a young age, thanks to the generosity and support of my advisors and academic community. I’m interested in helping ambitious undergraduate students likewise break into the world of academia. <strong>Please get in touch.</strong></p>

    <p>If you’re trying to find me in person, you’ll have better luck by email than by geography.</p>
  </div>
</div>

---

## Explore

- **Research** → [/research/](/research/)
- **Publications** → [/publications/](/publications/)
- **Writing** → [/writing/](/writing/)
- **Photography** → [/photography/](/photography/)
- **Contact** → [/contact/](/contact/)

---

## Latest

{% for post in site.posts limit:8 %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
