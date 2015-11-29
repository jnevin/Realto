# Realto
The Realto Live Cinema project.

## Realto Agile Project Status Tracking Board
- https://tree.taiga.io/project/jnevin-realto/

## Overview
This repo contains software application templates for the Realto Live Cinema project.

The Realto application is Mac-OSX-only software. It's components are built on top of three foundation applications: 
- [Quartz Composer](https://developer.apple.com/library/mac/documentation/GraphicsImaging/Conceptual/QuartzComposerUserGuide/qc_intro/qc_intro.html)
- [CogeVJ](http://imimot.com/cogevj/)
- [Vezer](http://imimot.com/vezer/).

### Quartz Composer
The Realto project uses Quartz Composer to create its Cue Manager and its Text Manager. 

The Cue Manager responds to OSC-enabled device inputs. In turn, it triggers playhead movement in the realto's media playback Timeline Manager with OSC messages of its own.

The Text Manager responds to OSC messages from the Timeline Manager in order to advance through the realto's sequence of text clips. 

## What's Here Now
- Realto model for CoGeVJ template.

## What's To Do:
- Add Vezer Realto model
- Add Cue Manager Quartz Composer tool 
- Add caption support Quartz Composer syphon server toool
- Extend CoGeVJ Realto template
- Normalize media
