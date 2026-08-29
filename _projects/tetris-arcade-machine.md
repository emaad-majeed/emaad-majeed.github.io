---
title: "Tetris Arcade Machine"
year: "2025"
class: "wide tetris-layout"
featured: true
thumb: "/assets/projects/tetris-arcade-machine/thumb.png"
featured_order: 1
tagline: "arcade cabinet"
hero: "/assets/projects/tetris-arcade-machine/hero.png"
hero_w: 2200
hero_h: 1307
hero_alt: "Render of the Tetris arcade cabinet with a game in play on the LED matrix"
blurb: "A playable Tetris arcade built on a NeoPixel matrix with a joystick, a rotate button, and a 3D printed and laser engraved cabinet."
---

A working Tetris arcade machine in a bartop cabinet. The game runs on a NeoPixel LED matrix, with a joystick for movement and a single button for rotation. The cabinet is laser cut and engraved, assembled with tab and slot joints, and finished with spray paint and printed vinyl artwork. The project pulled together two halves that had to meet in the middle: writing the game logic and driving the hardware, and designing and building the physical machine it lives in.

<dl class="meta">
  <div><dt>Methods</dt><dd>CAD, laser cutting and engraving, 3D printing, spray finishing, electronics, embedded code</dd></div>
  <div><dt>Tools</dt><dd>Fusion 360, laser cutter, 3D printer, NeoPixel matrix, joystick and button input</dd></div>
</dl>

## 1. Process

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

I started from the classic upright arcade silhouette and worked it down to something that could sit on a table. The sketches explore the profile: how far the screen leans back, how deep the control shelf sticks out, and where the marquee sits above the display. The stepped side profile came out of those passes, because it keeps the screen angled toward the player while letting the whole machine stay small.

<figure class="process-sketch">
  <img src="/assets/projects/tetris-arcade-machine/sketches.png" alt="Sketch studies working through the cabinet profile, screen angle and control shelf">
  <figcaption aria-hidden="true">Sketch studies working through the cabinet profile, screen angle and control shelf</figcaption>
</figure>

</div>
<div class="step-images" markdown="1">

<figure class="line-sketch">
  <img src="/assets/projects/tetris-arcade-machine/sketch-icon.png" alt="Line sketch of the arcade cabinet in three quarter view">
  <figcaption aria-hidden="true">Line sketch of the arcade cabinet in three quarter view</figcaption>
</figure>

</div>
</div>

<div class="project-step cad-step" markdown="1">
<div class="step-copy" markdown="1">

I took the chosen profile into Fusion 360 and built the cabinet as a set of flat panels that interlock. Modeling it as an assembly meant I could check that the screen opening lined up with the matrix, that the control shelf sat at a comfortable height, and that every joint met at the right place before anything was cut.

</div>
<div class="cad-images" markdown="1">

<figure class="cad-image cad-image-top-one">
  <img src="/assets/projects/tetris-arcade-machine/design-01.png" alt="CAD render of the full Tetris arcade cabinet">
  <figcaption aria-hidden="true">CAD render of the full Tetris arcade cabinet</figcaption>
</figure>
<figure class="cad-image cad-image-top-two">
  <img src="/assets/projects/tetris-arcade-machine/design-02.png" alt="Side view of the cabinet showing the screen rake and the projecting control shelf">
  <figcaption aria-hidden="true">Side view of the cabinet showing the screen rake and the projecting control shelf</figcaption>
</figure>
<figure class="cad-image cad-image-top-three">
  <img src="/assets/projects/tetris-arcade-machine/exploded.png" alt="Exploded view showing how the side panels, front face and control shelf tab together">
  <figcaption aria-hidden="true">Exploded view showing how the side panels, front face and control shelf tab together</figcaption>
</figure>
<figure class="cad-image cad-image-side">
  <img src="/assets/projects/tetris-arcade-machine/photo-01.jpg" alt="The cabinet panels modelled as separate flat pieces">
  <figcaption aria-hidden="true">The cabinet panels modelled as separate flat pieces</figcaption>
</figure>

</div>
</div>

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

The assembly was flattened into a single cut file. Every panel carries tabs and matching slots so the cabinet locks together without brackets, and the screen and control openings are cut in the same pass. After cutting I engraved and painted the panels, then applied printed vinyl for the marquee and the tetromino artwork on the sides.

</div>
<div class="step-images" markdown="1">

![Flat pattern of every cabinet panel laid out for the laser cutter](/assets/projects/tetris-arcade-machine/flat-pattern.png)
![Cut panels off the laser bed](/assets/projects/tetris-arcade-machine/photo-06.jpg)
![Laser engraving the cabinet panels](/assets/projects/tetris-arcade-machine/photo-07.jpg)
![Panels tabbed together into the finished cabinet](/assets/projects/tetris-arcade-machine/photo-08.jpg)
![Vinyl artwork laid out on the computer before printing](/assets/projects/tetris-arcade-machine/photo-04.jpg)
![Printed sticker sheet of the Tetris artwork](/assets/projects/tetris-arcade-machine/photo-05.jpg)

</div>
</div>

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

The playfield is a NeoPixel matrix sitting behind the screen opening. Raw, the individual LEDs read as bright points rather than clean blocks, so I put a diffuser film over the face. That spreads each pixel into an even square and makes the stack of tetrominoes read properly from a normal viewing distance. Behind the panel the matrix is wired back to the board along with the joystick and the rotate button.

</div>
<div class="step-images" markdown="1">

![Wiring behind the panel connecting the matrix and the controls](/assets/projects/tetris-arcade-machine/photo-10.jpg)
![Diffuser film laid over the matrix](/assets/projects/tetris-arcade-machine/photo-11.jpg)
![The same display with the film in place, showing how it evens out each pixel](/assets/projects/tetris-arcade-machine/photo-12.jpg)
![Working through a NeoPixel programming exercise](/assets/projects/tetris-arcade-machine/photo-13.jpg)

</div>
</div>

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

The game had to be written from the ground up for a display that is only a few dozen pixels across. That meant mapping the LED strip into a grid, tracking the playfield state, and redrawing it cleanly every frame. Movement comes off the analog joystick and rotation off a debounced button. On top of the basic falling and clearing, I added a soft drop for faster placement, a level system that speeds the game up as it goes, line clears, and win and lose animations.

</div>
<div class="step-images" markdown="1">

![Writing and testing the game code](/assets/projects/tetris-arcade-machine/photo-03.jpg)
![Working between the code and the CAD model](/assets/projects/tetris-arcade-machine/photo-02.jpg)

</div>
</div>

## 2. Final Design

<div class="project-step" markdown="1">
<div class="step-copy" markdown="1">

The finished machine is a white bartop cabinet with the marquee above the screen, tetromino artwork down the sides, and the joystick and rotate button set into the control shelf.

Building our Pixel Arcade Tetris game was challenging but also really rewarding. At first the idea seemed simple, but once we started coding the NeoPixel matrix, handling joystick movement, and writing the game logic, we realized how many small details had to work together. Learning how to map the LEDs, read analog inputs, debounce the rotate button, and update the screen correctly taught us a lot about combining hardware with programming.

One feature I am especially proud of is the soft drop, because it made the gameplay feel smoother and required careful timing. The hardest part was definitely the joystick. The analog values were unpredictable, and getting the movement to feel consistent took a lot of trial and error. Adding the level system made things even tougher because fixing one part of the code often messed up another part. It felt like trying to solve a Rubik's cube where every twist created a new problem to fix, while you also had to retain the previously solved parts.

</div>
<div class="step-images" markdown="1">

![The finished Tetris arcade cabinet](/assets/projects/tetris-arcade-machine/photo-14.jpg)
![Gameplay running on the finished machine](/assets/projects/tetris-arcade-machine/photo-15.jpg)
![The lose scene on the display](/assets/projects/tetris-arcade-machine/photo-16.jpg)

</div>
</div>
