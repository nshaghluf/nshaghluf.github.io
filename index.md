---
layout: default
title: Home
permalink: /
---


<div class="portfolio-hero" style="display:grid;grid-template-columns:1fr 1fr;gap:45px;align-items:center;padding:65px 0;">

  <div>
    <p style="font-size:13px;letter-spacing:2px;text-transform:uppercase;color:#65766e;">
      AI Researcher · Montréal, Canada
    </p>

    <h1 style="font-family:Georgia,serif;font-size:clamp(44px,5vw,76px);line-height:1.05;margin:20px 0;color:#172b25;">
      Nagwa<br>
      <span style="color:#c45129;">Shaghluf.</span>
    </h1>

    <p style="font-size:18px;color:#53645e;">
      PhD in Electrical and Computer Engineering<br>
      Deep Reinforcement Learning · Multi-Agent Systems · Applied AI
    </p>

    <p style="margin-top:30px;">
      <a href="#research" style="background:#172b25;color:white;padding:13px 22px;border-radius:25px;text-decoration:none;">
        Explore Research
      </a>
    </p>
  </div>

  <div>
    <p style="font-size:12px;letter-spacing:2px;color:#65766e;">
      MY RESEARCH PHILOSOPHY
    </p>

    <h2 style="font-family:Georgia,serif;font-size:clamp(28px,3vw,43px);line-height:1.15;color:#172b25;">
      Research is not limited to a discipline.
      <span style="color:#c45129;">It is a way of thinking.</span>
    </h2>

    <p style="font-size:17px;line-height:1.8;color:#53645e;">
      I believe being a researcher is more than specializing in a particular field.
      It is about developing a mindset that allows you to recognize problems,
      investigate existing solutions, identify opportunities for improvement,
      and build solutions that can be implemented, tested, and refined.
    </p>
  </div>

</div>

<section id="research">

## About My Research

I hold a PhD in Electrical and Computer Engineering from the University of Victoria.

My research focuses on intelligent decision-making, multi-agent deep reinforcement learning, predictive modeling, and autonomous systems.

</section>

---

## Recent Writing

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{% endfor %}

[View all articles]({{ '/blog/' | relative_url }})

