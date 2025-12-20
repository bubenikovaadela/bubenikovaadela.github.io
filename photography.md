---
layout: page
title: Photography
permalink: /photography/
---

I make photographs as a practice of noticing.

## Photo essays
{% assign photos = site.photo_essays | sort: "date" | reverse %}
{% for post in photos limit:12 %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
