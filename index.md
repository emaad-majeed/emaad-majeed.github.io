---
layout: default
title: Emaad Majeed
description: Aspiring industrial designer — portfolio
class: home
---

# Emaad Majeed

Aspiring industrial designer.

<section class="list">
  <h2>Select Projects</h2>
</section>

<section class="list">
  <h2>Projects</h2>
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
