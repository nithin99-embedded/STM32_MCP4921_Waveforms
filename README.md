# STM32 Nucleo-F103RB + MCP4921 Waveform Generator 🎛️

This repository contains **four waveform generation examples** using the  
**STM32 Nucleo-F103RB** microcontroller and **MCP4921 12-bit SPI DAC**.

---

## ⚙️ Overview

The STM32 communicates with the MCP4921 DAC via SPI to produce analog waveforms from digital values.  
All projects are written using **STM32CubeIDE** with **HAL drivers**.

Each project demonstrates a different waveform type with clear code, circuit connections, and hardware images.

---

## 🧩 Hardware Used

| Component | Description |
|------------|-------------|
| **STM32 Nucleo-F103RB** | Main MCU board |
| **MCP4921 DAC** | 12-bit SPI Digital-to-Analog Converter |
| **Breadboard + Jumper Wires** | For prototyping |
| **Multimeter / Oscilloscope** | For observing waveforms |
| **Power Supply** | 3.3V from Nucleo board |

---

## ⚡ Circuit Connections (Common for All)

| MCP4921 Pin | STM32 Pin | Description |
|--------------|------------|-------------|
| **VDD (1)** | 3.3 V | Power |
| **CS̅ (2)** | PA4 | Chip Select |
| **SCK (3)** | PA5 | SPI Clock |
| **SDI (4)** | PA7 | SPI MOSI |
| **LDAC̅ (5)** | GND | Latch (always enabled) |
| **VREF (6)** | 3.3 V | Reference voltage |
| **VSS (7)** | GND | Ground |
| **VOUT (8)** | Output | Connect to multimeter or oscilloscope |

---

## 📁 Project Structure

STM32_MCP4921_Waveforms/
├── Sawtooth_Wave/
├── Triangle_Wave/
├── Square_Wave/
└── Random_Wave/


Each folder includes:
- Complete STM32CubeIDE project (`Core/`, `Drivers/`, `.ioc`)
- Individual `README.md` explaining code and output
- Hardware setup photos in `/images/`

---

## 🧮 Generated Waveforms

| Waveform | Description | Output Range |
|-----------|--------------|---------------|
| **Sawtooth Wave** | Gradually increases 0V → 3.3V, resets to 0V | 0 – 3.3 V |
| **Triangle Wave** | Ramps up and down linearly | 0 – 3.3 V |
| **Square Wave** | Switches between 0V and 3.3V | 0 / 3.3 V |
| **Random Wave** | Randomly fluctuating voltages | 0 – 3.3 V |

---

## 🔗 Individual Projects

| Project | Folder | Description |
|----------|---------|-------------|
| 🔸 [Sawtooth Wave](./Sawtooth_Wave) | `Sawtooth_Wave/` | Ramp output using for-loop |
| 🔹 [Triangle Wave](./Triangle_Wave) | `Triangle_Wave/` | Up/down linear ramp |
| ⬛ [Square Wave](./Square_Wave) | `Square_Wave/` | Alternating 0V–3.3V |
| 🎲 [Random Wave](./Random_Wave) | `Random_Wave/` | Random voltage generation |

---

## 🖼️ Hardware Setup Example

![Hardware Setup](Sawtooth_Wave/images/Full_Setup.jpg)
*Example setup of STM32 Nucleo-F103RB with MCP4921 on breadboard.*

---

## 🧠 How It Works

1. The STM32 sends **12-bit SPI data** to MCP4921.  
2. MCP4921 converts digital input `D` into analog voltage:

\[
V_{out} = \frac{D}{4096} \times V_{REF}
\]

3. By varying `D` according to mathematical patterns (sinusoidal, ramp, random, etc.),  
   we get corresponding analog waveforms at the output.

---

## 🧰 Tools & Software

| Tool | Purpose |
|------|----------|
| STM32CubeIDE | Code development |
| STM32 HAL Drivers | Hardware abstraction |
| MCP4921 | SPI DAC for analog conversion |
| Multimeter / Oscilloscope | Output measurement |

---

## 📸 Author

**Nithin Reddy**  
Embedded Systems Developer | STM32 & C Programming  
🗺️ Hyderabad, India  
📅 November 2025  

---

## 💬 License
This project is open-source under the **MIT License** —  
you’re free to use, modify, and share it with credit.