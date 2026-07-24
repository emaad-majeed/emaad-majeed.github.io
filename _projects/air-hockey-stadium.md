---
title: "Air Hockey Stadium"
year: "2024"
blurb: "A Bears-themed air hockey table with a fan-powered play surface, Arduino scoreboard, and LED lighting."
---

## Overview

The Air Hockey Stadium is a working, fan-powered air hockey table styled to look like a Bears football field. What started as a small penny hockey assignment grew into a full build combining woodworking, 3D printing, acrylic, and Arduino electronics into a table that actually plays. My intent was to design a real, playable stadium that pushed past the scope of the original brief.

*Year: 2024 · Tools: Fusion 360, Arduino, table saw, miter saw, band saw, laser cutter, soldering, 3D printer*

## The Problem

The project was originally supposed to be a small penny hockey project, but I was inspired by an older engineering student who had built a working air hockey stadium a few years earlier. I wanted to build a real air hockey table, and the central challenge was engineering a play surface with enough airflow to lift and glide the puck, then wrapping it in a structure and electronics that held together and worked reliably.

## Research & Insights

I talked to Chase, the student who had built the earlier air hockey table, and asked many questions that helped me a lot in creating my own. I asked about the fan, its voltage, its size, and how to direct the airflow to the table. One of the biggest parts was finding a powerful enough fan: if the fan wasn't strong enough, I'd have to source another and keep testing until one worked. Chase recommended a 12v 120mm squirrel fan, and in testing it was perfect for the table.

![Chase's air hockey table, back view](/assets/projects/air-hockey-stadium/img_1613.jpg)

*Chase's air hockey table: back view*

I also studied an existing DIY build for reference on how a low-cost air hockey surface is constructed.

The airflow principle is straightforward: the fan creates high pressure below the surface, and that high-pressure air flows out through the holes underneath the puck, reducing its friction so it glides.

![Diagram of airflow through the holes beneath the puck](/assets/projects/air-hockey-stadium/image-1.png)

*Instructables: DIY Low Cost Air Hockey Table*

As a reference point, a small air hockey table with goals, play surface, goal counter, corner stoppers, and planks uses an external air pump for airflow.

[Project documentation (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vQIMWr4jiqaTGpnyYdVg6tYBONWw2tMAzo1J6kNGUGY2PVrKhzGIrpQomUzxUole1ywWIX-epn_Deck/pub)

[Project documentation (Google Doc)](https://docs.google.com/document/d/e/2PACX-1vQYaHvx_5WL5u16hSfXN5HMaKzP-SZKc0qFgy_LXVbxEvPS_CD90lGf9ow0goQk7yxJ7Z2wZBnr8Moe/pub)

[Project data (Google Sheet)](https://docs.google.com/spreadsheets/d/e/2PACX-1vQvadYZrY1coKHQ5jojlZFQ80PY6EajIsDz-o9H8J4lJjO1arQcviAKCSUToXaHJukPIlxw1MV68EDB/pubhtml)

## Design & Development

I modeled the table in Fusion 360 before building. The structure uses two dado cuts on each plank to hold the top acrylic play surface (with its holes) and the bottom wood piece together.

![Assembly plan for the table structure](/assets/projects/air-hockey-stadium/long-image-2024-01-09-02.02.09.jpg)

[![Fusion 360 model of the air hockey table](/assets/projects/air-hockey-stadium/screen-shot-2024-01-09-at-2.12.17-am.png)](https://a360.co/41PQGDm)

*Click the image above for the Fusion 360 file*

For the airflow, the 120mm squirrel fan blows air into a 3D printed tunnel that channels it beneath the play surface. Arduinos control both the scoreboard and the fan.

![Arduino and 120mm squirrel fan setup feeding the airflow tunnel](/assets/projects/air-hockey-stadium/image.png)

*Instructables: DIY Low Cost Air Hockey Table*

After assembly, I had the idea to paint the table so it would look like a Bears football field, modeled on Soldier Field.

![Soldier Field, the visual reference for the play surface](/assets/projects/air-hockey-stadium/soldier-field.jpg)

I went to my local library's makerspace and sanded and painted the backside of the acrylic.

![Painted backside of the acrylic play surface](/assets/projects/air-hockey-stadium/img_1770.jpg)

I added white field lines on top with a white paint marker, along with the marks and yard numbers of a real football field.

![Acrylic surface with painted field markings and yard numbers](/assets/projects/air-hockey-stadium/img_1783.jpg)

[Watch on YouTube](https://www.youtube.com/watch?v=fTexOYbA57g)

For decoration, I ran LED strips along the backside, driven by an Arduino running FastLED.

```cpp
#include <FastLED.h>
#define LED_PIN 13
#define NUM_LEDS 78

CRGB leds[NUM_LEDS];


void setup() {
  FastLED.addLeds<WS2812, LED_PIN, GRB>(leds, NUM_LEDS);
  FastLED.setMaxPowerInVoltsAndMilliamps(5, 500);
  FastLED.clear();
  FastLED.show();
 
}

void loop() {
  // Turn lights from green to blue from left to right   R G B 
  for (int i=0; i<NUM_LEDS; i++){
    leds[i] = CRGB(0, 255 - 4*i, 4*i );
    FastLED.setBrightness(2*i);
    FastLED.show();
    delay(50);
  }
  // Turn lights from blue to magenta from right to left 
  for (int i=NUM_LEDS; i>0; i--){
    leds[i] = CRGB(4*i,0 , 255-4*i);
    FastLED.setBrightness(100-i);
    FastLED.show();
    delay(50);
  }
  
  
}
```

*LED strip Arduino code from Github*

For the play pieces, I laser cut a foam puck because it's really light and easy to make, and I 3D printed the hitters and glued fabric on the bottom to prevent scratching. Across the build I used wood planks, 3D printed goals, an acrylic play space, Arduinos, LCDs, fans, wires, and buttons.

## Outcome & Reflection

Overall I had fun making this project, but there were many challenges and obstacles. Achieving the right dimensions for the side planks to fit with the acrylic play space was a big challenge that took lots of trial and error, but in the end it came out great. I learned a new type of cut, the dado cut, which holds the acrylic play space and the wooden backplate close together, and I learned to use woodworking machines like the table saw and the miter saw. I also learned that setting goals along the way helps you achieve anything: I set many goals for the individual aspects of the table and worked through them one by one. Every tool we learned over the year (Arduino, soldering, miter saw, band saw, table saw, laser cutter, and drilling) was incorporated into this project, and I'm really happy with how it turned out.

![Finished air hockey stadium, lit and painted](/assets/projects/air-hockey-stadium/img_1809.jpg)

![Finished air hockey stadium, full view](/assets/projects/air-hockey-stadium/img_1808.jpg)

Sources:

Technovation, & Instructables. (2019, August 26). *DIY Low Cost Air Hockey table*. Instructables. [https://www.instructables.com/DIY-Low-Cost-Air-Hockey-Table/](https://www.instructables.com/DIY-Low-Cost-Air-Hockey-Table/)

Hendog993. (2020). Youtube_arduino/LEDStrip.ino. Github. [https://github.com/hendog993/Youtube_arduino/blob/master/LEDStrip.ino](https://github.com/hendog993/Youtube_arduino/blob/master/LEDStrip.ino).
