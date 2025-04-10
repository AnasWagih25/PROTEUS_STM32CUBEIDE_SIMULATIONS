# LED Control with Switch Input

This project demonstrates controlling multiple LEDs using a switch. When the switch is pressed, an `if` condition is used to check the state of the switch, and based on this state, the LEDs will toggle on and off.

## Overview

The system uses multiple LEDs controlled by a switch connected to a microcontroller. When the switch is pressed:
- The program checks the switch state using an `if` condition.
- If the switch is pressed (e.g., in the ON state), the LEDs will turn on and off in sequence.
- If the switch is not pressed, the LEDs remain in the OFF state.

## Components Used

- Multiple LEDs (for visual feedback)
- Switch (for input control)
- Microcontroller (STM32F103C8)
- Proteus software for simulation

## Logic

The system uses an `if` condition to check the state of the switch:
1. **If the switch is pressed** (e.g., in the ON state):
   - The LEDs will toggle on and off in sequence.
2. **If the switch is not pressed** (e.g., in the OFF state):
   - The LEDs will remain off.

The program continuously checks the switch state and controls the LEDs accordingly.

## How to Use

1. Open the Proteus simulation file.
2. Press the switch to start the LED toggle sequence.
3. The LEDs will turn on and off in sequence when the switch is pressed.
4. Release the switch to stop the LED sequence.

## Files

- [Proteus Circuit Design File]
- [Code for Microcontroller - HEX File]

## Instructions

1. Download the files.
2. Open the Proteus simulation in Proteus software.
3. Load the HEX file to the microcontroller in the simulation.
4. Press the switch to start the LED sequence and observe the LEDs turning on and off.
5. Release the switch to stop the LED sequence.

