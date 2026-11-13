---
layout: default
title: Home
permalink: /
---

# Nagwa Shaghluf, PhD

**Researcher · Artificial Intelligence · Reinforcement Learning**

Montréal, Québec, Canada

---

## Welcome

I am a researcher with a PhD in Electrical and
Computer Engineering from the University of Victoria.

My work focuses on intelligent decision-making,
multi-agent deep reinforcement learning, predictive
modeling, and autonomous systems.

This website is a place to share my research,
technical projects, scientific questions, and
ideas as they develop.

## Recent Writing

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{% endfor %}

[View all articles]({{ '/blog/' | relative_url }})

