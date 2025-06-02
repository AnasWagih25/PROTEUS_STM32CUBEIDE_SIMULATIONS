# ⚡ EV Electronics Simulation with Deadman Switch (STM32F103C8)

This project simulates an **Electric Vehicle (EV) electronics system** for racing applications using the **STM32F103C8** microcontroller. It includes a **deadman switch** mechanism for safety and features **two LCDs** and **two 7-segment displays** used as digital speedometers.

## 🧩 Features

- Deadman switch for driver presence detection and safety cutoff
- Dual 16x2 LCDs for displaying vehicle status, battery info, etc.
- Dual 7-segment displays for real-time speed monitoring
- Built using STM32CubeIDE and STM32 HAL libraries
- Intended for EV simulation and testing environments

## 🔧 Tools

- **Microcontroller:** STM32F103C8 ("Blue Pill")
- **Displays:**
  - 2 × 16x2 LCDs (I2C or Parallel)
  - 2 × 7-segment displays
- **Safety Switch:** Deadman switch (e.g., pushbutton or presence sensor)
- **Optional:** Speed input source (e.g., analog, sensor)

## 🛠 Development Tools

- **IDE:** STM32CubeIDE
- **Language:** C (HAL drivers)
- **Debugger:** ST-Link or USB-TTL (via bootloader)
- **Simulation:** Proteus 

## 📁 Project Structure

```
EV_Electronics_Deadman_Simulation/
├── Core/
│   ├── Inc/
│   └── Src/
├── Drivers/
├── LCD/
├── SegmentDisplay/
├── .ioc
├── README.md
```

## 🧪 Usage

1. Flash the firmware to the STM32F103C8 using STM32CubeIDE
2. Power the circuit and activate the deadman switch
3. Monitor data on the LCDs and speed values on the 7-segment displays
4. Disable the deadman switch to simulate an emergency stop condition

## 🔄 Expansion Ideas

- Add telemetry output via UART or CAN
- Integrate logging with SD card
- Implement FreeRTOS for task separation
- Expand display data (temperature, voltage, etc.)

## 📜 License

This project is open source under the MIT License.

