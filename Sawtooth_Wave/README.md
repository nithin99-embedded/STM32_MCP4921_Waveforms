\# MCP4921 Sawtooth Wave using STM32 Nucleo-F103RB



This project generates a \*\*sawtooth (ramp)\*\* waveform using the MCP4921 12-bit SPI DAC.



\## 🧩 Description

\- STM32 sends values 0 → 4095 to DAC via SPI.

\- MCP4921 converts these to analog voltages 0 V → 3.3 V.

\- Delay = \*\*100 ms\*\* per step for easy viewing on multimeter.

\- Reduce delay for faster oscillation on oscilloscope.



\## ⚙️ Circuit Connections

| MCP4921 Pin  | STM32 Pin               | Description    |

|--------------|-------------------------|----------------|

| VDD (1)      | 3.3 V                   | Power          |

| CS̅ (2)       | PA4                     | Chip Select    |

| SCK (3)      | PA5                     | SPI Clock      |

| SDI (4)      | PA7                     | SPI MOSI       |

| LDAC̅ (5)     | GND                     | Latch          |

| VREF (6)     | 3.3 V                   | Reference      |

| VSS (7)      | GND                     | Ground         |

| VOUT (8)     | Multimeter/Oscilloscope | Output Voltage |



\## 🧮 Formula

\\\[

V\_{out} = \\frac{D}{4096} \\times V\_{REF}

\\]



\## 🖼️ Hardware Setup

!\[Setup](images/Full\_Setup.jpg)

!\[Setup](images/MCP4921\_Closeup.jpg)



\## 🧰 Expected Output

A ramp waveform gradually increasing from 0 V → 3.3 V then resetting to 0 V.

