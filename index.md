---
layout: default
title: Emaad Majeed
description: Aspiring industrial designer portfolio
class: home
---

# Emaad Majeed

<p class="tagline"><a href="{{ '/about/' | relative_url }}">Aspiring industrial designer.</a></p>

<section class="list">
  <h2>Select Projects</h2>
  <div class="grid">
  {% assign featured = site.projects | where: "featured", true | sort: "featured_order" %}
  {% for p in featured %}
    <a class="card" href="{{ p.url | relative_url }}">
      <img src="{{ p.thumb | relative_url }}" alt="{{ p.title }}" loading="lazy">
      <span class="card-title">{{ p.title }}</span>
      <span class="card-label">
        <span class="t">{{ p.title }}</span>
        {% if p.tagline %}<span class="s">{{ p.tagline }}</span>{% endif %}
      </span>
    </a>
  {% endfor %}
  </div>
</section>

<section class="list">
  <h2>All Projects</h2>
  {% assign projects = site.projects | sort: "year" | reverse %}
  {% for p in projects %}
  <a class="row" href="{% if p.external %}{{ p.external }}{% else %}{{ p.url | relative_url }}{% endif %}"{% if p.external %} target="_blank" rel="noopener noreferrer"{% endif %}>
    <span class="year">{{ p.year }}</span>
    <span class="title">{{ p.title }}</span>
    <span class="desc">{{ p.blurb }}</span>
  </a>
  {% endfor %}
</section>

<section class="list">
  <h2>Press</h2>
  <a class="row" href="https://theoracle.glenbrook225.org/news/2026/02/27/vex-robotics-builds-talent-relationships-from-various-competitions/" target="_blank" rel="noopener noreferrer">
    <span class="year">2026</span>
    <span class="title">VEX robotics builds talent, relationships from various competitions</span>
    <span class="desc">The Oracle, on the invitational tournament South hosted for 17 teams from around Chicago.</span>
  </a>
  <a class="row" href="https://theoracle.glenbrook225.org/top-stories/web-exclusives/2025/03/10/souths-vex-robotics-team-qualifies-for-worlds-competition/" target="_blank" rel="noopener noreferrer">
    <span class="year">2025</span>
    <span class="title">South's VEX robotics team qualifies for Worlds competition</span>
    <span class="desc">The Oracle, on our team reaching the World Championship in Dallas for the first time in school history.</span>
  </a>
</section>

<p class="foot"><a href="{{ '/about/' | relative_url }}">About</a></p>
