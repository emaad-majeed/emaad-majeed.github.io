---
title: "Pancake Robot Cooker"
year: "2024"
class: "wide pancake-robot-layout"
featured: true
thumb: "/assets/projects/pancake-robot/thumb.png"
featured_order: 2
tagline: "cooking robot"
blurb: "A robot that dispenses batter and flips pancakes using stepper motors."
---

I designed a pancake robot cooker with a two axis batter dispenser and a robotic arm. Stepper motors move the dispenser across the griddle and position the spatula to flip the pancakes.

<dl class="meta">
  <div><dt>Methods</dt><dd>CAD, 3D printing, motor control and assembly</dd></div>
  <div><dt>Tools</dt><dd>Fusion 360, 3D printer and stepper motors</dd></div>
</dl>

<p class="project-resources">Project documents: <a href="https://docs.google.com/document/d/e/2PACX-1vR8-MLkhSianqUsATvhWb2WghDUGNtmBo-8VOJ7ifEEtweeYRMAqfeL8VUVWDdBMkrhjn0erY5AsTHw/pub">Proposal</a>, <a href="https://a360.co/4oIOM2h">3D model</a>, <a href="https://docs.google.com/spreadsheets/d/e/2PACX-1vR_hkSceqagxelOayXScqAluhtnqh_gcnb7x5TrQ5hM504eRw2bxdCvHpCVNM5JWxAvUI6A0E-uNZVA/pubhtml">Budget</a>, <a href="https://docs.google.com/document/d/e/2PACX-1vQqXlZm5AVfn5CdtCuRi0AXv-CfZ8zAXOLhaFIQY8W0qVKGx9TYSIF7k3DeA0UCua7RY27E6Msbse_B/pub">Daily Log</a>, <a href="https://docs.google.com/spreadsheets/d/e/2PACX-1vQ7DZmYkYslHKd_D3PtjO2-QvRWc9_9jz5lOwbYD4-RWNZvrBUDmmNUFHYIkBr8qOjRfh_3Mkr_UJc4/pubhtml">Gantt Chart</a> and <a href="https://docs.google.com/document/d/e/2PACX-1vQBmln5hbauL22uz0APqdl6XLuMb3rRxYuLtOCmDesw7ZI5zYSKcYolPNqBlJmTZMCRtxqbGlqhzc9K/pub">Decision Matrix</a>.</p>

## 1. Process

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

I began by exploring a system with two robotic arms, one for the batter dispenser and one for the spatula. I then replaced the dispenser arm with a two axis machine that could move the dispenser over the griddle. This gave the design a clearer division of work: the dispenser handles the batter while the robotic arm handles the flip.

I modelled the assembly in Fusion 360 before building it. The model brought the griddle, dispenser, arm and base together so I could work through the placement of the parts before making them.

</div>
<div class="step-images" markdown="1">

<figure class="process-image">
  <img src="/assets/projects/pancake-robot/screenshot-2024-03-04-at-9.46.15e280afpm.png" alt="CAD view of the pancake robot cooker with the griddle, batter dispenser and robotic arm">
  <figcaption aria-hidden="true">CAD view of the pancake robot cooker with the griddle, batter dispenser and robotic arm</figcaption>
</figure>

<figure class="process-image">
  <img src="/assets/projects/pancake-robot/screenshot-2024-03-04-at-8.27.20e280afpm.png" alt="CAD drawing of the pancake robot cooker assembly with the batter dispenser and robotic arm">
  <figcaption aria-hidden="true">CAD drawing of the pancake robot cooker assembly with the batter dispenser and robotic arm</figcaption>
</figure>

<div class="fusion-model"><iframe src="https://glenbrook225484.autodesk360.com/g/shares/SH90d2dQT28d5b602811a8117f0c6075dcbb?mode=embed" title="Interactive Fusion 360 model of the pancake robot cooker" loading="lazy" allowfullscreen></iframe></div>

</div>
</div>

## 2. Final Design

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

The final design places the batter dispenser at one end of the griddle and the robot arm with its spatula at the other. I printed parts for both mechanisms and assembled the system around the griddle. Testing the motors and wiring showed where the motion needed adjustment, and I refined the design through those iterations.

</div>
<div class="step-images" markdown="1">

<div class="video"><iframe src="https://www.youtube.com/embed/CJ-02lUsz2o" title="Pancake robot cooker demonstration" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></div>

<figure class="final-image">
  <img src="/assets/projects/pancake-robot/render-01.png" alt="Render of the pancake robot cooker with the arm and dispenser on opposite sides of the griddle">
  <figcaption aria-hidden="true">Render of the pancake robot cooker with the arm and dispenser on opposite sides of the griddle</figcaption>
</figure>

<figure class="final-image">
  <img src="/assets/projects/pancake-robot/render-02.png" alt="Render of the pancake robot cooker with the batter dispenser and robot arm on the base">
  <figcaption aria-hidden="true">Render of the pancake robot cooker with the batter dispenser and robot arm on the base</figcaption>
</figure>

</div>
</div>
