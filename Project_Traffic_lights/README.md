# Traffic Light Simulation with STM32F103C8

This project demonstrates a traffic light simulation using STM32F103C8. The system uses 3 LEDs (Red, Yellow, Green) to represent the traffic light states, with the Red LED turning on for 5 seconds, Yellow for 2 seconds, and Green for 5 seconds, repeating the cycle.

## Overview

This traffic light system uses 3 LEDs connected to an STM32F103C8 microcontroller. The LEDs represent the following states:
- **Red LED**: Turns on for 5 seconds.
- **Yellow LED**: Turns on for 2 seconds.
- **Green LED**: Turns on for 5 seconds.

The system continuously cycles through the traffic light states.

- **Traffic Light States**:
  - **Red**: 5 seconds
  - **Yellow**: 2 seconds
  - **Green**: 5 seconds
  
Each state will be represented by lighting up the corresponding LED for the specified time.

## Components Used

- 3 LEDs (Red, Yellow, Green) for traffic light simulation
- Resistors for current limiting
- Microcontroller: STM32F103C8
- Proteus software for simulation

## Logic

The microcontroller will implement a simple timer-based logic to switch between the traffic light states:
- The Red LED turns on for 5 seconds, then turns off.
- The Yellow LED turns on for 2 seconds, then turns off.
- The Green LED turns on for 5 seconds, then turns off.

The cycle repeats indefinitely.

## How to Use

1. Open the Proteus simulation file.
2. Start the simulation to watch the traffic light cycle.
3. The LEDs will turn on and off in the following sequence:
   - Red for 5 seconds
   - Yellow for 2 seconds
   - Green for 5 seconds
4. The cycle repeats automatically.

## Files

- [Proteus Circuit Design File]
- [Code for Microcontroller - HEX file for STM32F103C8]

## Instructions

1. Download the files.
2. Open the Proteus simulation in Proteus software.
3. Load the HEX file to the STM32F103C8 microcontroller in the simulation.
4. Start the simulation to observe the traffic light cycle.

## Contributing

Feel free to fork the repository and submit pull requests if you'd like to improve the project. Issues and feature suggestions are welcome!

## License

This project is licensed under the MIT License.
