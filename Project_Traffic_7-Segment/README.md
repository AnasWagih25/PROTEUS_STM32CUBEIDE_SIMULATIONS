# STM32 Traffic Light Simulation with 7-Segment Countdown Display

## Overview

This project simulates a dual traffic light system using the STM32F103C8 microcontroller. Each light is paired with a 7-segment display to show a countdown timer:
- **Red/Green phases** count down from **9 to 0**
- **Yellow phase** counts down from **2 to 0**

The simulation is developed in **STM32CubeIDE** and tested in **Proteus**.

---

## Hardware Configuration

**Microcontroller**: STM32F103C8 (Blue Pill)

### Traffic Light 1 (TL1)
- **Red LED**: PA0  
- **Yellow LED**: PA1  
- **Green LED**: PA2  
- **7-Segment Display (Common Cathode)**: PA8 to PA14 (segments A–G)

### Traffic Light 2 (TL2)
- **Red LED**: PA3  
- **Yellow LED**: PA4  
- **Green LED**: PA5  
- **7-Segment Display (Common Cathode)**: PB8 to PB14 (segments A–G)

---

## Logic Flow

1. **Phase 1**:  
   - TL1: Red LED ON, 7-seg counts down from 9  
   - TL2: Green LED ON, 7-seg counts down from 9  
   - Duration: 10 seconds

2. **Phase 2**:  
   - Both TL1 and TL2: Yellow LED ON  
   - Both 7-seg displays count down from 2  
   - Duration: 3 seconds

3. **Phase 3**:  
   - TL1: Green LED ON, 7-seg counts down from 9  
   - TL2: Red LED ON, 7-seg counts down from 9  
   - Duration: 10 seconds

4. **Phase 4**:  
   - Same as Phase 2  
   - Then loop back to Phase 1

---

## Development Tools

- **IDE**: STM32CubeIDE  
- **Simulation**: Proteus 8 Professional  
- **Programming Language**: C  
- **HAL Drivers** used for GPIO control and delay

---

## How to Run

In Proteus:
   - Add the STM32, LEDs, and 7-segment displays as per the pin configuration.
   - Load the compiled `.hex` file into the STM32 model.
   - Run the simulation.

---

## Notes

- Make sure to debounce or delay properly to match 1-second intervals.
- Use a look-up table or bitmask array for displaying digits on the 7-segment.
- Use `HAL_Delay(1000)` for 1-second steps.

---

## Author

Simulation by [Your Name]  
Tested with STM32F103C8 + Proteus  
