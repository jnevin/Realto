# Realto
The Realto Live Cinema project.

A realto (re&#772;a&#774;l-to&#772;) is a new, hybrid form of visual storytelling -- part live narrative, part pre-recorded movie, part text, part electronic theater -- all coming together in an experience best described, perhaps, as Live Cinema.

## Realto Agile Project Status Tracking Board
- https://tree.taiga.io/project/jnevin-realto/

## Overview
This repo contains software application tools and templates for the Realto Live Cinema project.

The Realto Live Cinema application is Mac-OSX-only software. The application's components are built on top of three foundation frameworks: 
- [Quartz Composer](https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/QuartzComposerUserGuide/qc_intro/qc_intro.html)
- [CoGeVJ](http://imimot.com/cogevj/)
- [Vezer](http://imimot.com/vezer/)

The application has four main components: 
- the **Cue Manager**
- the **Timeline Manager**
- the **Media Manager**
- the **Text Manager** 

### Application Flow
Communication between these four components is over the local TCP network, primarily via [OSC, Open Sound Control](https://en.wikipedia.org/wiki/Open_Sound_Control). The application uses other protocols such as [DMX](https://en.wikipedia.org/wiki/DMX512) and [ART-NET](https://en.wikipedia.org/wiki/Art-Net) to control lighting and [MIDI](https://en.wikipedia.org/wiki/MIDI) for certain types of device input.

![alt text](https://github.com/jnevin/Realto/blob/develop/Diagrams/Realto-Application-Flow.png)

### Quartz Composer
The project uses Quartz Composer to create its **Cue Manager** and its **Text Manager**. Quartz Composeer is a free developer tool bundled with Mac OS X.

The **Cue Manager** responds to messages from OSC-enabled and MIDI-enabled interactive devices that are available to the live realto sayer (the realto's narrator/actor). In turn, with OSC messages of its own, the Cue Manager triggers playhead movement in the realto's Timeline Manager, cueing media playback and other theater events.

The **Text Manager** responds to OSC messages from the Timeline Manager in order to advance through the realto's sequence of text clips, which are then displayed via the Media Manager. 

### CoGeVJ
The project uses CoGeVJ to create its **Media Manager**. CoGeVJ is an amazing, low-cost commercial VJ software app from [Imimot](http://imimot.com/).

The **Media Manager** manages a realto's audio/visual media, such as video clips, images, effects and layers, and live streams from video cameras and green screen. The Media Manager's interactive mixer responds to OSC messages from the Timeline Manager, composites the media and then displays it for projection.

### Vezer
The project uses Vezer to create its **Timeline Manager**. Vezer is a unique, low-cost commercial sequencer software app also from [Imimot](http://imimot.com/) -- amazing, as well!

The **Timeline** Manager is the "communications central" of a realto. It receives OSC message inputs from the sayer-controlled Cue Manager. In response, it moves its playhead through the realto composition timeline. 

Each timeline's composition contains a set of synchronized media control tracks that trigger events in the Media Manager with outbound OSC messages. 

## What's Here Now
- Realto model for CoGeVJ template.

## What's To Do:
- Add Vezer Realto model
- Add Cue Manager Quartz Composer tool 
- Add caption support Quartz Composer syphon server toool
- Extend CoGeVJ Realto template
- Normalize media
