---
title: "Multistaging Water Rocket"
year: "2025"
blurb: "A multistage, water-and-air-pressure rocket exploring a cleaner, cheaper alternative to combustion propulsion."
---

## Overview

*Year: 2025 · Tools: Autodesk 3D modeling, TinkerCad, Arduino*

The Multistaging Water Rocket is a model rocket propelled entirely by compressed air and water, designed and built for Maker Faire 2025. The design intent was to prototype an eco-friendly propulsion system that trades fuel and combustion for a renewable, low-cost energy source while still chasing real performance. I led the project as Team Manager, working with Suleiman Mohiuddin and [Jay Kim](https://jayyoungkim.wordpress.com/maker-faire-2025/); the full documentation lives in our shared drive.

[Google Drive Folder](https://drive.google.com/drive/folders/1QSSotiYyObDgM7XdwC-f8b0XvqyzKIN1?usp=sharing)

[Project Documentation (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vTNehrOdVGPvrKH-wq1wFbw2nVfDeTCcbdGQuLiJUqzl7mQr5_KufcLFxr8okMhxwIH32zGnZfOJLEA/pub)

## The Problem

There is a growing need for sustainable, eco-friendly fuel sources. Combustion is a leading cause of environmental pollution, and traditional rockets rely on fossil fuels that release harmful chemicals such as carbon monoxide and carbon dioxide into the atmosphere. For Maker Faire 2025, I wanted to explore an alternative: instead of fuel and oil, use water — a renewable, eco-friendly source — powered by water and air pressure. The design challenge was to make water work as an energy source while maximizing performance and efficiency, and to do it as something innovative, creative, and genuinely fun to build.

## Research & Insights

The project leans on chemistry principles that govern how gases behave under pressure. Pumping air into the bottle compresses the gas and raises its pressure according to Boyle's Law, which states that pressure and volume are inversely related at constant temperature. That high-pressure air stores potential energy; on release, it rapidly expands, forcing water out and generating thrust — converting the behavior of gases under pressure into mechanical motion. Understanding this relationship is what lets me tune the air-to-water ratio for maximum performance. I also studied existing water-rocket builds to ground the design.

[Research Video (YouTube)](https://www.youtube.com/watch?v=KYQx9Sr7S38)

## Ideation & Concept Development

I generated several propulsion concepts before committing to a direction:

1. **Water pulse jet rocket** — rapid, repeated bursts of water and air from a chamber for pulse-like propulsion, using only water and air.
2. **Water rocket glider hybrid** — launches on water pressure, then deploys glider wings at peak altitude for a slow descent and long horizontal distance.
3. **Water propulsion rocket with adjustable nozzle** — standard water-rocket mechanics with a swappable nozzle to control water loss and test efficiency.
4. **Multistage water rocket** — two or more stacked, connected bottles; the first stage launches on water pressure, then a second stage detaches mid-flight and launches on its own water/air pressure.
5. **Water rocket with internal ballast control** — an internal mechanism shifts weight during flight to adjust the center of gravity.

I chose the multistage concept. Building a multi-stage, water-propelled rocket promised a fuel solution that is cheaper, environmentally sustainable, and a more efficient use of energy than combustion propulsion. Each stage launches independently: the first provides the initial launch and thrust, and the second launches off the momentum of the first plus its own propulsion. Compared to conventional designs, this avoids wasting limited natural-resource fuel and the high cost of commercial-scale combustion engines.

## Design & Development

I developed the rocket from sketch to physical prototype, moving through 3D modeling and control circuitry before the final build.

[3D Modeling](https://glenbrook225484.autodesk360.com/g/shares/SH286ddQT78850c0d8a4cd14dc1f8639bad2)

![Water rocket concept sketch](/assets/projects/water-rocket/water-rocket-sketch.png)

![3D model of the water rocket](/assets/projects/water-rocket/3d-model.png)

[TinkerCad](https://www.tinkercad.com/things/elPIuS9y1Pw-maker-faire-2025/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=bLE5LTWjfZFG1QfULEZQAYKS4VibtDNCHDa5rSSaP3Y)

![TinkerCad model of the rocket assembly](/assets/projects/water-rocket/maker-faire-2025-1.png)

To handle staging and control, I prototyped Arduino circuitry.

![Arduino control circuit model](/assets/projects/water-rocket/arduino-model-2025.png)

[Arduino Demo Video (Google Drive)](https://drive.google.com/file/d/1bLjLAnJrx5Z138bFRAU4pdC3BdD2hLZs/preview)

The modeling and circuitry came together in the final physical prototype.

![Final prototype of the multistage water rocket](/assets/projects/water-rocket/image.png)

![Final prototype detail, stage connection](/assets/projects/water-rocket/image-1.png)

![Final prototype detail, nozzle and body](/assets/projects/water-rocket/image-2.png)

## Outcome & Reflection

Reflecting on the project, we hit both successes and setbacks that pushed us to think like engineers and problem-solvers. The staging system performed decently — not perfect, but promising. The separation worked as intended, shedding extra weight mid-flight and slightly increasing airtime; it wasn't as smooth or efficient as I hoped, but it proved the concept was valid and worth improving. With only one launch, I couldn't refine the timing or structure of the stages, but I learned a lot from watching how staging affected stability and thrust. Next, I'd design a more reliable and lighter staging mechanism, test different detachment timings, and reinforce the connection points for cleaner separation. Despite limited testing and minor stability issues, the project let me apply real scientific principles and practice adapting, analyzing, and improving under pressure — just like real engineers.

[Final Video](https://www.canva.com/design/DAGoFrzL6LU/T9HjOBf9G8_2yGPMaICjww/edit?utm_content=DAGoFrzL6LU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

[Daily Log (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vSb86L6MeVFkLDKhx2myBvZcYRFRwtS52-chLx0T1Pxes3i3dYPO72s2cTFYt_xLvmqbZzLefMMiOcP/pub)
