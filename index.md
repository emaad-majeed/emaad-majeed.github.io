---
layout: default
title: Emaad Majeed
description: Maker & engineer — portfolio
class: home
---

# Emaad Majeed

Maker &amp; engineer.

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

<section class="list">
  <h2>Writing</h2>
  {% assign posts = site.blog | sort: "year" | reverse %}
  {% for p in posts %}
  <a class="row" href="{{ p.url | relative_url }}">
    <span class="year">{{ p.year }}</span>
    <span class="title">{{ p.title }}</span>
    <span class="desc">{{ p.blurb }}</span>
  </a>
  {% endfor %}
</section>

<p class="foot"><a href="{{ '/about/' | relative_url }}">About</a></p>
