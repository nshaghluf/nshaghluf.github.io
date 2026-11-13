---
layout: page
title: Blog
permalink: /blog/
---

Research notes, technical experiments, and
reflections on artificial intelligence,
learning, and scientific discovery.

{% for post in site.posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

---

{% endfor %}
