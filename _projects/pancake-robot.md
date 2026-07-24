---
title: "Pancake Robot Cooker"
year: "2024"
blurb: "A countertop robot that pours batter with a two-axis dispenser and flips pancakes with a stepper-motor arm."
---

By: Emaad Majeed

*Year: 2024 · Tools: Fusion 360, 3D printer, bandsaw, mitre saw, Dremel, stepper motors*

## Overview

The Pancake Robot Cooker is a kitchen machine that makes pancakes from start to finish: a two-axis dispenser pours batter onto the griddle, and a stepper-motor robotic arm flips each pancake so it cooks evenly on both sides. The design intent was to take a familiar breakfast task and automate it with an approachable, buildable mechanism rather than an over-engineered one.

[View the project proposal (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vR8-MLkhSianqUsATvhWb2WghDUGNtmBo-8VOJ7ifEEtweeYRMAqfeL8VUVWDdBMkrhjn0erY5AsTHw/pub)

## The Problem

We wanted to automate cooking, but when we looked at existing cooking robots we found they were too complicated to actually build. The challenge was to land on a cooking task simple enough to design and prototype ourselves, while still requiring real mechanical and electronic problem-solving. Pancakes fit: pouring and flipping are two clear, repeatable motions that a machine can be built to handle.

## Ideation & Concept Development

We started by brainstorming a range of ideas, including go-karts, RC cars, and RC planes, before settling on the Pancake Robot Cooker once we realized other cooking robots were too complex to make.

[View the project decision matrix (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vQBmln5hbauL22uz0APqdl6XLuMb3rRxYuLtOCmDesw7ZI5zYSKcYolPNqBlJmTZMCRtxqbGlqhzc9K/pub)

Our first concept used two robotic arms: one to hold the batter dispenser and another to flip pancakes with a spatula. We later revised this, replacing one of the arms with a two-axis (CNC-style) laser machine to carry the batter dispenser. Splitting the roles this way made the design more practical and efficient: a precise gantry for pouring, and a dedicated arm for flipping.

## Design & Development

We modeled the concept in Fusion 360, then sourced parts online and ordered everything we needed before starting to 3D print components for both the robotic arm and the CNC machine.

[![3D model of the pancake robot in Fusion 360](/assets/projects/pancake-robot/screenshot-2024-03-04-at-9.46.15e280afpm.png)](https://a360.co/4oIOM2h)

*Click image for the Fusion 360 model*

![Pancake robot assembly in the 3D model](/assets/projects/pancake-robot/screenshot-2024-03-04-at-8.27.20e280afpm.png)

The first parts to arrive were bearings, nuts, rods, and bolts, which we used to start building the base of the robotic arm. We tested the motor and gradually built up the arm structure. Wiring and coding the stepper motors took a lot of trial and error to get working. The movement was rough at first, and adding grease helped the gears turn more smoothly. We still had significant trouble getting the motors to reliably change direction, and at times they even broke the base. In parallel, we began assembling the CNC machine, which involved cutting metal rods and 3D printing additional parts.

On the electronics side, I applied circuitry principles from class, wiring components in both parallel and series. The batter dispenser motor and the arm's stepper motors were connected in parallel to the power supply so they could operate independently while sharing one source, and I added switches as manual overrides to start and stop specific functions, such as activating the dispenser when it was time to pour. Building and troubleshooting the system was hands-on practice in reading circuit schematics and coordinating components.

Throughout the build I learned to use a range of tools, including a 3D printer, bandsaw, mitre saw, and Dremel.

[View the project budget (Google Sheet)](https://docs.google.com/spreadsheets/d/e/2PACX-1vR_hkSceqagxelOayXScqAluhtnqh_gcnb7x5TrQ5hM504eRw2bxdCvHpCVNM5JWxAvUI6A0E-uNZVA/pubhtml)

[View the daily log (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vQqXlZm5AVfn5CdtCuRi0AXv-CfZ8zAXOLhaFIQY8W0qVKGx9TYSIF7k3DeA0UCua7RY27E6Msbse_B/pub)

[View the Gantt chart (Google Sheet)](https://docs.google.com/spreadsheets/d/e/2PACX-1vQ7DZmYkYslHKd_D3PtjO2-QvRWc9_9jz5lOwbYD4-RWNZvrBUDmmNUFHYIkBr8qOjRfh_3Mkr_UJc4/pubhtml)

## Outcome & Reflection

We didn't fully solve the robotic arm's motor issues, but the project was a big step forward in my understanding of engineering and design. It pushed me to work methodically: when the motors misbehaved, we had to analyze what was going wrong and experiment with different fixes, iterating through testing, troubleshooting, and refining. Collaborating with my teammates mattered just as much: we communicated, divided tasks around our strengths, and supported each other through the hard parts.

More than anything, the project taught me perseverance and the value of continuous improvement. Seeing it come together, even imperfectly, was rewarding, and it has pushed me to keep exploring robotics and technology.

[Watch the project video on YouTube](https://www.youtube.com/watch?v=CJ-02lUsz2o)
