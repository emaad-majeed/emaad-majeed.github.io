---
layout: page
title: "About"
permalink: /about/
---

{% assign shot = site.static_files | where_exp: "f", "f.path contains '/assets/about/headshot'" | first %}
{% if shot %}<div class="headshot"><img src="{{ shot.path | relative_url }}" alt="Emaad Majeed"></div>{% endif %}

<p class="whoami">Emaad Majeed</p>

<p class="contact"><a href="mailto:emaadmajeed@outlook.com">emaadmajeed@outlook.com</a></p>

Emaad Majeed is an aspiring industrial designer from the Chicagoland area. He is a student at Glenbrook South High School in Glenview, Illinois, where he competes in VEX Robotics with team 38535X.

## Skills

<dl class="meta skills">
  <div>
    <dt>Design</dt>
    <dd>CAD modeling, concept sketching, design for 3D printing, design for laser cutting, exploded assembly views, flat pattern layout, interface design, iterative prototyping, rendering, technical drawing, vector artwork</dd>
  </div>
  <div>
    <dt>Electronics</dt>
    <dd>Analog input reading, button debouncing, distance sensors, inertial sensors, LCD displays, LED matrices, microcontrollers, motor control, NeoPixel addressable LEDs, odometry, optical sensors, PID tuning, pneumatics and pistons, resistors, rotation sensors, servo motors, soldering, stepper motors, switch wiring and harnesses, V5 smart motors</dd>
  </div>
  <div>
    <dt>Fabrication</dt>
    <dd>3D printing, bandsaw, CNC machining, dado joinery, Dremel, drilling, end grain lamination, glue up and clamping, laser cutting, laser engraving, miter saw, sanding and finishing, spray painting, tab and slot construction, table saw, vinyl and sticker printing, woodworking</dd>
  </div>
  <div>
    <dt>Materials</dt>
    <dd>Acrylic, aluminum, carbon fiber, cherry, Delrin, foam, maple, padauk, plywood, polycarbonate, walnut</dd>
  </div>
  <div>
    <dt>Software</dt>
    <dd>Arduino, Autodesk Fusion 360, C++, Desmos, FastLED, Git and GitHub, LemLib, Microsoft Flight Simulator 2020, PROS, TinkerCad</dd>
  </div>
</dl>
