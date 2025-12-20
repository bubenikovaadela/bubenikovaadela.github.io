---
layout: page
title: Photography
permalink: /photography/
---

I make photographs as a practice of noticing.

## Photo essays (on this site)
{% raw %}
{% assign photos = site.photo_essays | sort: "date" | reverse %}
{% for post in photos limit:12 %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endraw %}

If you’re interested in prints, collaborations, or commissioning a photo-essay, please reach out.
