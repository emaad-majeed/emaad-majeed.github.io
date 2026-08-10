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

Skills: 3D printing, agentic workflows, analog input reading, Arduino, Autodesk Fusion 360, bandsaw, button debouncing, C++, CAD modeling, Claude Code, CNC machining, Codex, concept sketching, dado joinery, DeepSeek, design for 3D printing, design for laser cutting, Desmos, distance sensors, Dremel, drilling, end grain lamination, Excel, exploded assembly views, FastLED, flat pattern layout, Git and GitHub, glue up and clamping, inertial sensors, interface design, iterative prototyping, laser cutting, laser engraving, LCD displays, LED matrices, LemLib, microcontrollers, Microsoft Flight Simulator 2020, miter saw, motor control, NeoPixel addressable LEDs, odometry, Opencode, optical sensors, PID tuning, pneumatics and pistons, PowerPoint, PROS, Python, rendering, resistors, rotation sensors, sanding and finishing, servo motors, soldering, spray painting, stepper motors, switch wiring and harnesses, tab and slot construction, table saw, technical drawing, TinkerCad, V5 smart motors, vector artwork, vinyl and sticker printing, woodworking, Word.
