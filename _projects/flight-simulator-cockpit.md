---
title: "737 Flight Simulator Cockpit Project (Part 1)"
year: "2023"
blurb: "A backlit, Arduino-driven 737 cockpit built panel by panel for Microsoft Flight Simulator 2020."
---

## Overview

I'm building a backlit, Arduino-driven Boeing 737 cockpit for Microsoft Flight Simulator 2020. The goal is to recreate the feel of a real 737 flight deck at home: laser-cut panels that glow through engraved text, and physical switches and buttons that actually control the simulator. This is Part 1 of an ongoing build.

## The Problem

Ready-made cockpit hardware exists, but I didn't want to buy a finished product. I wanted to design and build the panels myself and make real, tactile inputs drive a flight simulator, which meant figuring out both the physical fabrication and the electronics from scratch.

## Research & Insights

A friend mentioned a nearby facility with a realistic, publicly available flight simulator. My dad found the place and took me. The whole space was full of 737 souvenirs, and the flight instructor walked us through it and set up a takeoff and a landing. Stepping inside the cockpit amazed me.

That night I spent hours searching for images and videos of other people's home-built simulators. At first the task felt impossible, but I quickly found tools to help. The key discovery was open-source software that takes inputs from an Arduino and converts them into inputs for my favorite flight simulator, Microsoft Flight Simulator 2020.

## Ideation & Concept Development

As a kid I was obsessed with airplanes, always asking my parents how they worked and flying flight simulators on my iPad. As I got older, that obsession shifted to RC planes, and I dreamed of building an RC replica of my favorite real-life plane, the Boeing 737.

Rather than buy a model, I wanted to build one. I found a YouTube tutorial with full instructions, convinced my dad to let me start, and picked up thin foam board from an arts and crafts store to cut into pieces. I printed paper templates and glued them onto the foam as cutting guides. But the builder in the video used a special foam that bent easily while staying firm; my foam snapped whenever I tried to bend it slowly. I couldn't find that material anywhere, so I gradually abandoned the RC plane and eventually pivoted to building a cockpit instead.

## Design & Development

I started with a lot of design work for the panels, experimenting with many circuits and programming them to work.

I've used my local library makerspace's laser cutter countless times to make every panel. Early on I wasn't skilled at spray painting or designing, but my panel-building skills have improved significantly. Every single panel in my simulator is backlightable: when I place a light behind a panel, only the engraved text lets a small amount of light through, so the text and some lines glow. Getting that engraving-and-lighting effect right was one of my toughest tasks.

![Backlightable fuel panel for the 737 overhead](/assets/projects/flight-simulator-cockpit/img_1354.jpg)

*The fuel panel for the 737 overhead.*

[YouTube video](https://www.youtube.com/watch?v=reo1Y2sBgJU)

Another area I've made progress on is the FMC.

![My hand-built version of the 737 FMC](/assets/projects/flight-simulator-cockpit/img_1344.jpg)

*My version of the FMC.*

On the back, functioning tactile push buttons are soldered to an Arduino protoshield board. The buttons are programmed with *MobiFlight* to work with *Microsoft Flight Simulator 2020*.

![FMC back-side wiring detail](/assets/projects/flight-simulator-cockpit/img_1724.jpg)

![FMC back-side soldering in progress](/assets/projects/flight-simulator-cockpit/img_1725.jpg)

*Lots of soldering progress still to go.*

![The FMC from a real 737 for reference](/assets/projects/flight-simulator-cockpit/maxresdefault.jpg)

*The real FMC from a real 737.*

To confirm the electronics work end to end, I've wired individual controls straight into the sim:

[Rotary switch working with the 737 in Microsoft Flight Simulator 2020](https://www.youtube.com/watch?v=2gJR1mi_Bgs)

*More clips of things working are on my YouTube channel.*

## Outcome & Reflection

This is still very much a work in progress. The panels backlight, the FMC and switches drive Microsoft Flight Simulator 2020, and there's plenty of soldering and building left to do. Part 2 is still being created.

*Year: 2023 · Tools: Arduino, Arduino protoshield, MobiFlight, laser cutter, Microsoft Flight Simulator 2020*
