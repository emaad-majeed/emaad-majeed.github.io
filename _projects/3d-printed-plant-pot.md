---
title: "Self Watering Plant Pot"
year: "2026"
class: "wide plant-pot-layout"
featured: true
thumb: "/assets/projects/3d-printed-plant-pot/thumb.png"
featured_order: 3
tagline: "smart self watering system"
hero: "/assets/projects/3d-printed-plant-pot/hero.png"
hero_w: 2140
hero_h: 1272
hero_alt: "Close view of the plant pot design with a round display set into the front"
blurb: "A smart self watering plant system I built for Maker Faire 2026, using soil moisture sensing to water a plant only when it needs it."
---

For Maker Faire 2026, I built a smart self watering plant system for one indoor plant. Inconsistent care can leave soil too wet or too dry, so I designed a system that measures moisture and waters only when the soil needs it. The project brought biology and engineering together through sensing, electronics, code, 3D printing, and water delivery.

<dl class="meta">
  <div><dt>Year</dt><dd>2026</dd></div>
  <div><dt>Context</dt><dd>Maker Faire biology project</dd></div>
  <div><dt>Methods</dt><dd>CAD, 3D printing, electronics, coding, soldering, testing</dd></div>
  <div><dt>Tools</dt><dd>Fusion 360, Arduino Mega, soil moisture sensor, water pump</dd></div>
</dl>

## 1. Process

<div class="project-step system-step" markdown="1">
<div class="step-copy" markdown="1">

I began by defining the problem around plant care and water use. A fixed schedule cannot respond to the actual condition of the soil, while a moisture sensor can provide a direct reading. My goal was to maintain a more stable growing environment by checking the soil before adding water.

I divided the system into five functions: sensing soil moisture, processing the reading, controlling the pump, delivering water, and supplying power. The soil moisture sensor sends an analog signal to the Arduino Mega. The Arduino compares that reading with a threshold and sends a control signal to the pump driver circuit when the soil is dry. The pump then moves water from a separate reservoir through tubing to the plant.

</div>
<div class="step-images" markdown="1">

<figure class="system-image">
  <img src="/assets/projects/3d-printed-plant-pot/system-diagram.png" alt="System diagram tracing the moisture signal from the sensor to the controller and the water path from the reservoir to the plant">
  <figcaption aria-hidden="true">System diagram tracing the moisture signal from the sensor to the controller and the water path from the reservoir to the plant</figcaption>
</figure>

</div>
</div>

<div class="project-step form-step" markdown="1">
<div class="step-copy" markdown="1">

In Fusion 360, I developed the cylindrical pot form, a printed holder, and a ring intended to distribute water around the plant. I kept the exterior simple so the project could read as a plant pot first while still giving the water path and controls a defined place.

After preparing the parts, I began 3D printing and checked how the holder, ring, tubing, plant container, and electronics would fit together. The physical arrangement had to support the plant without interfering with the sensor or water delivery system.

</div>
<div class="step-images design-images" markdown="1">

<figure class="design-image design-image-one">
  <img src="/assets/projects/3d-printed-plant-pot/design-01.png" alt="Plant pot design with the round display set into the front">
  <figcaption aria-hidden="true">Plant pot design with the round display set into the front</figcaption>
</figure>
<figure class="design-image design-image-two">
  <img src="/assets/projects/3d-printed-plant-pot/design-02.png" alt="Straight front view of the cylindrical pot and compact display">
  <figcaption aria-hidden="true">Straight front view of the cylindrical pot and compact display</figcaption>
</figure>

</div>
</div>

<div class="project-step controls-step" markdown="1">
<div class="step-copy" markdown="1">

I tested each electronic part before combining the full system. The moisture sensor produced different analog readings in dry soil, moist soil, and water. Those tests showed that the code needed a calibrated threshold based on real readings rather than an assumed value. I later adjusted that threshold so the controller could distinguish dry soil more reliably.

The Arduino could not power the pump directly, so I used a MOSFET driver circuit as a switch between the controller and the separate pump supply. I connected the grounds, tested the pump control, and added red, yellow, and green LEDs. Red means the soil needs water, yellow means the pump is running, and green means the moisture condition is acceptable.

I soldered the sensor, LED, and pump control connections to make the circuit more secure. Water testing then helped me refine the pump timing, since a cycle that is too long can add too much water and a cycle that is too short does not solve the dry soil condition.

</div>
<div class="step-images interface-images" markdown="1">

<figure class="interface-image interface-image-one">
  <img src="/assets/projects/3d-printed-plant-pot/design-03.png" alt="Round interface with water, temperature, and plant status readings">
  <figcaption aria-hidden="true">Round interface with water, temperature, and plant status readings</figcaption>
</figure>
<figure class="interface-image interface-image-two">
  <img src="/assets/projects/3d-printed-plant-pot/design-04.png" alt="Compact round interface set flush into the pot body">
  <figcaption aria-hidden="true">Compact round interface set flush into the pot body</figcaption>
</figure>

</div>
</div>

## 2. Final Design

<div class="project-step final-step" markdown="1">
<div class="step-copy" markdown="1">

The final prototype combines the planted pot, moisture sensor, Arduino Mega, pump driver circuit, water reservoir, tubing, and three status LEDs. When the soil is dry, the controller turns on the red indicator and starts a controlled watering cycle. Yellow communicates active watering. When the moisture reading is acceptable, the pump remains off and the green indicator gives immediate confirmation.

The working build taught me how much an automated system depends on calibration and physical organization. The code, sensor, pump, tubing, soldered connections, and printed parts all had to work together under realistic conditions. Troubleshooting unstable readings, pump control, wiring, and water flow made the project a practical exercise in testing one variable at a time.

I also explored a compact round screen that could bring the LED feedback and water information into one interface. A future version could add a water level sensor, test more soil conditions, refine the watering duration, and organize the electronics into a cleaner enclosure.

</div>
<div class="step-images final-images" markdown="1">

<figure class="prototype-image">
  <img src="/assets/projects/3d-printed-plant-pot/build-01.jpg" alt="Working prototype with the planted pot, tubing, reservoir, Arduino Mega, wiring, and status LEDs">
  <figcaption aria-hidden="true">Working prototype with the planted pot, tubing, reservoir, Arduino Mega, wiring, and status LEDs</figcaption>
</figure>

</div>
</div>
