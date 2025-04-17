# STM32F103C8 + 7-Segment Display (Common Anode) Counter

This project demonstrates how to interface a **common anode 7-segment display** with the **STM32F103C8 ("Blue Pill")** microcontroller using **STM32CubeIDE / HAL** or bare-metal C. It counts up from `0` to `9` in a loop, displaying the digits sequentially.

## 🧠 Overview

- **MCU:** STM32F103C8T6 (Blue Pill)
- **Display:** Common Anode 7-Segment Display
- **Count Range:** 0 → 9
- **Update Rate:** 1 digit per second (adjustable via delay)
- **Programming Tools:** STM32CubeIDE or any ARM-compatible IDE

## 🔌 Wiring

| Segment | 7-Segment Pin | STM32 Pin (Example) |
|---------|----------------|---------------------|
| A       | 1              | PA0                 |
| B       | 2              | PA1                 |
| C       | 4              | PA2                 |
| D       | 5              | PA3                 |
| E       | 6              | PA4                 |
| F       | 7              | PA5                 |
| G       | 9              | PA6                 |
| COM     | 3 or 8         | +3.3V (via resistor)|



