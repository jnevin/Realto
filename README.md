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
The Realto project uses Quartz Composer to create its Cue Manager and its Text Manager. 

The Cue Manager responds to messages from OSC-enabled devices available to the realto sayer (the realto narrator/actor). In turn, using OSC messages of its own, the Cue Manager triggers playhead movement in the realto's Timeline Manager in order to cue media playback.

The Text Manager responds to OSC messages from the Timeline Manager in order to advance through the realto's sequence of text clips. 

### CoGeVJ
The Realto project uses CoGeVJ to create is Media Manager. 

The Media Manager keeps track of a realto's audio/visual media such as video clips, images, effects and layers. The Media Manager's interactive mixer, responding to OSC messages from the Timeline Manger, composites the media and displays it for projection.

### Vezer
The Realto project uses Vezer to create its Timeline Manager.

The Timeline Manager is the "communications central" of a realto. It receives OSC message inputs from the sayer-controlled Cue Manager and responds by moving its playhead correspondingly through the realto composition timeline. Each composition contains and synchronizes a set of media-controller tracks that trigger events in the Media Manager via OSC outputs. 

## What's Here Now
- Realto model for CoGeVJ template.

## What's To Do:
- Add Vezer Realto model
- Add Cue Manager Quartz Composer tool 
- Add caption support Quartz Composer syphon server toool
- Extend CoGeVJ Realto template
- Normalize media
