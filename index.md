---
layout: default
title: Home
---

# Ideas, Research & Learning

Welcome to my personal space for research,
exploration, and learning.

I hold a PhD in Electrical and Computer Engineering,
with research experience in multi-agent reinforcement
learning, predictive modeling, and autonomous
decision-making.

My interests extend to artificial intelligence,
generalization, continual learning, and building
reliable intelligent systems.

This blog is a place to explore questions, document
experiments, and share ideas as they develop.

---

## Recent Writing

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{% endfor %}

---

[Read all articles]({{ '/blog/' | relative_url }})
