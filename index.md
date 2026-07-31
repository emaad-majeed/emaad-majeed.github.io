---
layout: default
title: Emaad Majeed
description: Aspiring industrial designer portfolio
class: home
---

# Emaad Majeed

Aspiring industrial designer.

<section class="list">
  <h2>Selected Projects</h2>
  <div class="grid">
  {% assign featured = site.projects | where: "featured", true | sort: "year" | reverse %}
  {% for p in featured %}
    <a class="card" href="{{ p.url | relative_url }}">
      <img src="{{ p.thumb | relative_url }}" alt="{{ p.title }}" loading="lazy">
      <span class="card-title">{{ p.title }}</span>
    </a>
  {% endfor %}
  </div>
</section>

<section class="list">
  <h2>All Projects</h2>
  {% assign projects = site.projects | sort: "year" | reverse %}
  {% for p in projects %}
  <a class="row" href="{{ p.url | relative_url }}">
    <span class="year">{{ p.year }}</span>
    <span class="title">{{ p.title }}</span>
    <span class="desc">{{ p.blurb }}</span>
  </a>
  {% endfor %}
</section>

<p class="foot"><a href="{{ '/about/' | relative_url }}">About</a></p>
