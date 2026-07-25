---
title: "737 Arduino Wiring"
year: "2023"
blurb: "The wiring layer that carries every cockpit panel input back to an Arduino."
---

This is the wiring layer that ties the switches and buttons of my Boeing 737 cockpit back to an Arduino. I soldered rows of red and white signal wires to a prototyping shield that sits on top of the Arduino, then bundled the harness with cable ties so it stays organized as it runs off toward the panels. The shield uses numbered pin rows so I could keep track of which panel input lands on which pin. Every input in the cockpit eventually comes back to this board so the microcontroller can read it and pass the state to the flight simulator.

![Prototyping shield with a soldered red and white wire harness leaving through a cable tie](/assets/projects/737-arduino-wiring/photo-01.jpg)
![The same wiring shield seen mounted with the harness looped and tied above it](/assets/projects/737-arduino-wiring/photo-02.jpg)
