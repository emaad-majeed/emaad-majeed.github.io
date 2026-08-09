---
layout: page
title: "About"
permalink: /about/
---

{% assign shot = site.static_files | where_exp: "f", "f.path contains '/assets/about/headshot'" | first %}
{% if shot %}<div class="headshot"><img src="{{ shot.path | relative_url }}" alt="Emaad Majeed"></div>{% endif %}

<p class="whoami">Emaad Majeed</p>

<p class="contact"><a href="mailto:emaadmajeed@outlook.com">emaadmajeed@outlook.com</a></p>

I am an aspiring industrial designer at Glenbrook South High School in Glenview, Illinois, with a passion for solving problems, digital design, electronics and cooking. Across my projects I have worked in Fusion 360 along with electronics, programming, woodworking and laser cutting.
