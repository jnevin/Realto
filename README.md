# Realto
The Realto Live Cinema project.

## Realto Agile Project Status Tracking Board
- https://tree.taiga.io/project/jnevin-realto/

## Overview
This repo contains software application templates for the Realto Live Cinema project.

The Realto application is Mac-OSX-only software. The application's components are built on top of three foundation frameworks: 
- [Quartz Composer](https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/QuartzComposerUserGuide/qc_intro/qc_intro.html)
- [CoGeVJ](http://imimot.com/cogevj/)
- [Vezer](http://imimot.com/vezer/)

### Quartz Composer
The Realto project uses Quartz Composer to create its Cue Manager and its Text Manager. 

The Cue Manager responds to OSC-enabled device inputs. In turn, using OSC messages of its own, it triggers playhead movement in the realto's Timeline Manager to cue media playback.

The Text Manager responds to OSC messages from the Timeline Manager in order to advance through the realto's sequence of text clips. 

### CoGeVJ
The Realto project uses CoGeVJ to create is Media Manager. The Media Manager keeps track of a realto's audio/visual media such as video clips, images, effects and layers. The Media Manager's interactive mixer, responding to OSC messages from the Timeline Manger, composites the media and displays it for projection. 

## What's Here Now
- Realto model for CoGeVJ template.

## What's To Do:
- Add Vezer Realto model
- Add Cue Manager Quartz Composer tool 
- Add caption support Quartz Composer syphon server toool
- Extend CoGeVJ Realto template
- Normalize media
