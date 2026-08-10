---
layout: page
title: "About"
permalink: /about/
---

{% assign shot = site.static_files | where_exp: "f", "f.path contains '/assets/about/headshot'" | first %}
{% if shot %}<div class="headshot"><img src="{{ shot.path | relative_url }}" alt="Emaad Majeed"></div>{% endif %}

<p class="whoami">Emaad Majeed</p>

<p class="contact"><a href="mailto:emaadmajeed@outlook.com">emaadmajeed@outlook.com</a></p>

Emaad Majeed is an aspiring industrial designer from the Chicagoland area. He is drawn to problems where how a thing looks and how it works have to be solved at the same time, and he would rather finish a project as an object he can hand to someone than as a drawing.

His work runs from a playable Tetris arcade cabinet and a self watering plant pot to VEX V5 competition robots, a homemade Boeing 737 cockpit and end grain cutting boards. He designs in Fusion 360 and builds with laser cutting and engraving, 3D printing, woodworking, electronics and C++, carrying a project from the first sketches through CAD to something that actually runs.

He is a student at Glenbrook South High School in Glenview, Illinois, where he competes in VEX Robotics with team 38535X.
