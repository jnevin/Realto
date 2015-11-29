# Realto
The Realto Live Cinema project.

## Realto Agile Project Status Tracking Board
- https://tree.taiga.io/project/jnevin-realto/

## Overview
This repo contains software application tools and templates for the Realto Live Cinema project.

The Realto Live Cinema application is Mac-OSX-only software. The application's components are built on top of three foundation frameworks: 
- [Quartz Composer](https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/QuartzComposerUserGuide/qc_intro/qc_intro.html)
- [CoGeVJ](http://imimot.com/cogevj/)
- [Vezer](http://imimot.com/vezer/)

### Quartz Composer
The project uses Quartz Composer to create its Cue Manager and its Text Manager. 

The Cue Manager responds to messages from OSC-enabled devices made available to the live realto sayer (the realto's narrator/actor). In turn, with OSC messages of its own, the Cue Manager triggers playhead movement in the realto's Timeline Manager, cueing media playback and other theater events.

The Text Manager responds to OSC messages from the Timeline Manager in order to advance through the realto's sequence of text clips, which are then displayed via the Media Manager. 

### CoGeVJ
The project uses CoGeVJ to create its Media Manager. 

The Media Manager manages a realto's audio/visual media, such as video clips, images, effects and layers, and live streams from video cameras and green screen. The Media Manager's interactive mixer responds to OSC messages from the Timeline Manager, composites the media and then displays it for projection.

### Vezer
The project uses Vezer to create its Timeline Manager.

The Timeline Manager is the "communications central" of a realto. It receives OSC message inputs from the sayer-controlled Cue Manager. In response, it moves its playhead through the realto composition timeline. 

Each timeline's composition contains a set of synchronized media control tracks that trigger events in the Media Manager with outbound OSC messages. 

## What's Here Now
- Realto model for CoGeVJ template.

## What's To Do:
- Add Vezer Realto model
- Add Cue Manager Quartz Composer tool 
- Add caption support Quartz Composer syphon server toool
- Extend CoGeVJ Realto template
- Normalize media
