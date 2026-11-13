---
layout: page
title: Blog
permalink: /blog/
---

# Blog

Research notes, ideas, and reflections on
artificial intelligence and machine learning.

{% for post in site.posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

---

{% endfor %}
