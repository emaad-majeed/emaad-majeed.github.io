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
hero_alt: "Conceptual redesign of the plant pot with a round display set into the front"
blurb: "A working self watering plant system I built for Maker Faire 2026, followed by a conceptual redesign for a more integrated product."
---

For Maker Faire 2026, I built a smart self watering plant system for one indoor plant. Inconsistent care can leave soil too wet or too dry, so I designed a system that measures moisture and waters only when the soil needs it. After completing and testing the working plant system, I redesigned it as a more refined product concept with an integrated enclosure and interface.

<dl class="meta">
  <div><dt>Year</dt><dd>2026</dd></div>
  <div><dt>Context</dt><dd>Maker Faire biology project</dd></div>
  <div><dt>Methods</dt><dd>CAD, 3D printing, electronics, coding, soldering, testing, product redesign, interface design</dd></div>
  <div><dt>Tools</dt><dd>Fusion 360, Arduino Mega, soil moisture sensor, water pump</dd></div>
</dl>

## 1. Process

<div class="project-step system-step" markdown="1">
<div class="step-copy" markdown="1">

I began by defining the problem around plant care and water use. A fixed schedule cannot respond to the actual condition of the soil, while a moisture sensor can provide a direct reading. My goal was to maintain a more stable growing environment by checking the soil before adding water.

I divided the system into five functions: sensing soil moisture, processing the reading, controlling the pump, delivering water, and supplying power. The soil moisture sensor sends an analog signal to the Arduino Mega. The Arduino compares that reading with a threshold and sends a control signal to the pump driver circuit when the soil is dry. The pump then moves water from a separate reservoir through tubing to the plant.

I designed and printed a holder and a ring intended to distribute water around the plant. I checked how the printed parts, tubing, plant container, and electronics fit together without interfering with the sensor or water delivery system.

I tested each electronic part before combining the full system. The moisture sensor produced different analog readings in dry soil, moist soil, and water, so I calibrated the threshold using actual sensor readings. I also soldered the sensor, LED, and pump control connections, then refined the watering duration by testing the pump and tubing with water.

</div>
<div class="step-images" markdown="1">

<figure class="system-image">
  <img src="/assets/projects/3d-printed-plant-pot/system-diagram.png" alt="System diagram tracing the moisture signal from the sensor to the controller and the water path from the reservoir to the plant">
  <figcaption aria-hidden="true">System diagram tracing the moisture signal from the sensor to the controller and the water path from the reservoir to the plant</figcaption>
</figure>

</div>
</div>

## 2. Working Prototype and Product Redesign

<div class="project-step final-step" markdown="1">
<div class="step-copy" markdown="1">

### Working Prototype

The working prototype combines the planted pot, moisture sensor, Arduino Mega, pump driver circuit, water reservoir, tubing, and three status LEDs. When the soil is dry, the controller turns on the red indicator and starts a controlled watering cycle. Yellow communicates active watering. When the moisture reading is acceptable, the pump remains off and the green indicator gives immediate confirmation.

The working build taught me how much an automated system depends on calibration and physical organization. The code, sensor, pump, tubing, soldered connections, and printed parts all had to work together under realistic conditions. Troubleshooting unstable readings, pump control, wiring, and water flow made the project a practical exercise in testing one variable at a time.

This was the actual system I built and tested. It used the three LEDs for feedback and did not have a screen.

</div>
<div class="step-images final-images" markdown="1">

<figure class="prototype-image">
  <img src="/assets/projects/3d-printed-plant-pot/build-01.jpg" alt="Working prototype with the planted pot, tubing, reservoir, Arduino Mega, wiring, and status LEDs">
  <figcaption aria-hidden="true">Working prototype with the planted pot, tubing, reservoir, Arduino Mega, wiring, and status LEDs</figcaption>
</figure>

</div>
</div>

<div class="project-step redesign-step" markdown="1">
<div class="step-copy" markdown="1">

### Product Redesign Concept

After completing the working plant system, I returned to the project and redesigned it as a more refined product concept. In Fusion 360, I developed a simple cylindrical enclosure that brings the plant, water storage, and controls into one unified form. The redesign explores how the exposed prototype could become a cleaner indoor product.

The round screen exists only in this redesign concept. It was never installed on the working plant system. I imagined the screen as a future replacement for the separate LED indicators, combining water level, temperature, and plant status information in one place.

The redesign remains a CAD and interface proposal for a future version. It helped me translate what I learned from the working prototype into a clearer product direction with a more integrated enclosure and easier to understand feedback.

</div>
<div class="step-images redesign-images" markdown="1">

<figure class="redesign-image redesign-image-one">
  <img src="/assets/projects/3d-printed-plant-pot/design-01.png" alt="Conceptual redesign of the plant pot with a round display set into the front">
  <figcaption aria-hidden="true">Conceptual redesign of the plant pot with a round display set into the front</figcaption>
</figure>
<figure class="redesign-image redesign-image-two">
  <img src="/assets/projects/3d-printed-plant-pot/design-02.png" alt="Front view of the conceptual cylindrical enclosure and compact display">
  <figcaption aria-hidden="true">Front view of the conceptual cylindrical enclosure and compact display</figcaption>
</figure>
<figure class="redesign-image redesign-image-three">
  <img src="/assets/projects/3d-printed-plant-pot/design-03.png" alt="Concept interface with water, temperature, and plant status readings">
  <figcaption aria-hidden="true">Concept interface with water, temperature, and plant status readings</figcaption>
</figure>
<figure class="redesign-image redesign-image-four">
  <img src="/assets/projects/3d-printed-plant-pot/design-04.png" alt="Concept interface set flush into the redesigned pot enclosure">
  <figcaption aria-hidden="true">Concept interface set flush into the redesigned pot enclosure</figcaption>
</figure>

</div>
</div>
