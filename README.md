# Amazepad

A hackpad with six keys, a rotary encoder and a small OLED display featuring Rocky from Project Hail Mary to help you with your projects.

![The PCB routing in Kicad](https://github.com/fish-in-a-puddle/Amazepad/blob/main/Images/pcb.png)


![The full case in SketchUp]()

#### This project was made for Hack Club's Stardance! Check it out [here](https://stardance.hackclub.com/projects/46887)

#### If you're a teenager wanting to make your own hackpad, you can find the tutorial [here](https://hackpad.hackclub.com/)

## Inspiration

A few weeks ago, I saw an interesting project on Reddit - a small voice assistant on a Raspberry Pi that talked like Rocky from Project Hail Mary. I had also been looking at the hackpads submitted through Stardance, so I thought "What about a hackpad with an engineering friend to encourage you?". This Rocky doesn't respond to questions, of course, but he shows different messages on the OLED depending on how fast you're typing.

![A screenshot of the project that inspired me to add Rocky to a hackpad](https://github.com/fish-in-a-puddle/Amazepad/blob/main/Images/inspiration.png)

## Layout

The Amazepad features 6 mechanical keyswitches and one rotary encoder. In my firmware, the rotary encoder controls the computer's volume and the keys are arranged like so:

| MUTE | CRTL+A | CTRL+Z |

| CTRL+C | CTRL+V | CTRL+S |

The Amazepad also has a 0.91" OLED display that shows three different images depending on your WPM, all pixel art of Rocky with one of his favorite phrases.

## Design

Before starting this project, I had never made a PCB before. It took a little while to get used to Kicad, but I eventually got everything properly connected. I had originally planned to add a second rotary encoder and lights under each key, but that ended up being way more complicated than I was prepared for, so I scaled back the design to make it easier to solder and program. Once the PCB was done, I moved on to designing the case.

![The schematic in Kicad](https://github.com/fish-in-a-puddle/Amazepad/blob/main/Images/schematic.png)

The tutorial suggested using Fusion 360, so I downloaded it. The moment I opened it, I regretted it. Nothing worked - not even drawing a rectangle. I probably could have hunkered down, watched some videos and figured it out in a few hours, but I didn't. I went back to the ever-reliable Sketchup and made a simple case there. Just a rectangle box with cutouts on the cover. I plan to add some stickers to it once I print it to make it a little cooler, though.

![The top of the case in my slicer](https://github.com/fish-in-a-puddle/Amazepad/blob/main/Images/casetop.png)

As for the firmware, I used QMK to port the macropad and set everything up. That took a while and a whole lot of trial and error. At this point the firmware has not been tested (as I do not have the actual hackpad yet) but I am fairly confident that it will work.

![A screenshot of the QMK code](https://github.com/fish-in-a-puddle/Amazepad/blob/main/Images/keymap.png)

## Bill of Materials

|Part                 |Qty|Cost(USD)|Source        |
|---------------------|---|---------|--------------|
|4.7k ohm resistor    | 2 | $0      | My workspace |
|1N4148 diode         | 6 | $0      | Hackpad kit  |
|Cherry MX keyswitches| 6 | $0      | Hackpad kit  |
|Rotary encoder       | 1 | $0      | Hackpad kit  |
|Seeeduino Xiao RP2040| 1 | $0      | Hackpad kit  |
|0.91 OLED            | 1 | $0      | Hackpad kit  |
