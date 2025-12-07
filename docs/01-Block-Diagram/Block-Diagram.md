---
title: Individual Block Diagram
tags:
- tag1
- tag2
---

## Overview
The purpose of this block diagram is to get a basic visual representation of what my subsystem for the ClapSense will look like. It indicates the mechanism for creating a system that automatically shuts the ClapSense off when there's already enough light present. It also shows how many connections will be made as well as where they will be on the board.

### Functionality 
* The upper left corner of the block diagram holds the voltage source and regulator. The source (outsidethe box) is 9V, and the LM7805 voltage regulator converts this 9V into the necessary 5V.
* Just below the voltage regulating system is the sensor and op-amp system, which acts as an input to the microcontroller's pin RC5. RC5 is an ADC, meaning it converts the signal from analog to digital for the microcontroller. 
* To the right of the microcontroller is the PWM LED, which is controlled by the microcontroller output RB3. The LED can give an idea of when the subsystem is activating, allowing the user to determine if it is false triggering or not (the system can be shut off in the case that it is false triggering).
* Finally, the output pin RA1 indicates the signal that goes to the actual clap light's microcontoller. It functions largely the same as the PWM LED, but it turns the clap light system on or off, rather than just being for debugging.

## Block Diagram 

![ Individual Block Diagram ](IndividualBlockDiagram.png)

The PDF of the above block diagram can be found ![here.](IndividualBlockDiagram.pdf)
