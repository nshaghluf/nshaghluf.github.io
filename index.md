---
layout: default
title: Home
permalink: /
---
<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">
<div class="portfolio-hero">
  <div>
    <p style="font-size:13px;letter-spacing:2px;text-transform:uppercase;color:#65766e;">
      AI Researcher · Montréal, Canada
    </p>

    <h1 style="color:#172b25;">
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

    <h2 style="color:#172b25;">
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

<section id="projects">

  <h2>Selected Projects</h2>

  <p>
    Exploring intelligent systems through research,
    experimentation, and practical applications.
  </p>

  <div class="project-grid">

    <article class="project-card">
      <span class="project-type">Research</span>
      <h3>Multi-Agent Reinforcement Learning</h3>
      <p>
        Doctoral research on intelligent
        decision-making, resource allocation,
        and cooperation in wireless networks.
      </p>
    </article>

    <article class="project-card">
      <span class="project-type">Machine Learning</span>
      
<article class="project-card">
  <span class="project-type">Machine Learning</span>

  <h3>BIXI Availability Prediction</h3>

  <a href="{{ '/projects/' | relative_url }}">
    <img
      src="{{ '/assets/images/bixi_availability_now_versus_next.png' | relative_url }}"
      alt="BIXI availability prediction concept showing current and future bike availability"
      class="project-image"
      loading="lazy">
  </a>

  <p>
    Forecasting bike and dock availability
    using historical station data, predictive modeling,
    and time-series analysis.
  </p>

  <a href="{{ '/projects/' | relative_url }}">
    Explore project
  </a>
</article>


    <article class="project-card">
      <span class="project-type">Software Engineering</span>
      <h3>ReturnEra</h3>
      <p>
        A parcel-return pickup platform
        combining online booking, backend APIs,
        database design, cloud infrastructure,
        and payment integration.
      </p>
      <a href="https://returnera.ca"
         target="_blank"
         rel="noopener noreferrer">
        Visit ReturnEra
      </a>
    </article>

  </div>

</section>

---

## Recent Writing

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %d, %Y" }}*

{{ post.excerpt }}

{% endfor %}

[View all articles]({{ '/blog/' | relative_url }})

