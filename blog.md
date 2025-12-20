---
layout: page
title: Blog
permalink: /blog/
---

{% raw %}
{% for post in site.posts %}
- **{{ post.date | date: "%Y-%m-%d" }}** — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endraw %}
