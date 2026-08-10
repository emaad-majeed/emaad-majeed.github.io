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

Skills: 3D Printing, Agentic Workflows, Analog Input Reading, Arduino, Autodesk Fusion 360, Bandsaw, Button Debouncing, C++, CAD Modeling, Claude Code, CNC Machining, Codex, Concept Sketching, Dado Joinery, DeepSeek, Design for 3D Printing, Design for Laser Cutting, Desmos, Distance Sensors, Dremel, Drilling, End Grain Lamination, Excel, Exploded Assembly Views, FastLED, Flat Pattern Layout, Git and GitHub, Glue Up and Clamping, Inertial Sensors, Interface Design, Iterative Prototyping, Laser Cutting, Laser Engraving, LCD Displays, LED Matrices, LemLib, Microcontrollers, Microsoft Flight Simulator 2020, Miter Saw, Motor Control, NeoPixel Addressable LEDs, Odometry, Opencode, Optical Sensors, PID Tuning, Pneumatics and Pistons, PowerPoint, PROS, Python, Rendering, Resistors, Rotation Sensors, Sanding and Finishing, Servo Motors, Soldering, Spray Painting, Stepper Motors, Switch Wiring and Harnesses, Tab and Slot Construction, Table Saw, Technical Drawing, Tinkercad, V5 Smart Motors, Vector Artwork, Vinyl and Sticker Printing, Woodworking, Word.
