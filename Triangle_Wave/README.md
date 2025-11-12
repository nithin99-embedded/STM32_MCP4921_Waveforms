\# MCP4921 Triangle Wave using STM32 Nucleo-F103RB



This project generates a \*\*triangle waveform\*\* using the MCP4921 12-bit SPI DAC.



\## Description

\- STM32 sends values 0 → 4095 (rise) then 4095 → 0 (fall).

\- DAC outputs a smooth linear up-down voltage.

\- Delay = \*\*100 ms\*\* per step for easy viewing on multimeter.



\## ⚙️ Circuit Connections



| MCP4921 Pin | STM32 Pin | Description |

|--------------|------------|-------------|

| \*\*VDD (1)\*\*  | 3.3 V | Power |

| \*\*CS̅ (2)\*\*  | PA4 | Chip Select |

| \*\*SCK (3)\*\*  | PA5 | SPI Clock |

| \*\*SDI (4)\*\*  | PA7 | SPI MOSI |

| \*\*LDAC̅ (5)\*\* | GND | Latch (always enabled) |

| \*\*VREF (6)\*\* | 3.3 V | Reference |

| \*\*VSS (7)\*\*  | GND | Ground |

| \*\*VOUT (8)\*\* | Multimeter / Oscilloscope | Output Voltage |



\## 🧮 Formula

\\\[

V\_{out} = \\frac{D}{4096} \\times V\_{REF}

\\]



\## 🖼️ Hardware Setup



\### Full Setup

!\[Full Setup](images/Full\_Setup.jpg)



\### Close-up of MCP4921 Wiring

!\[Close-up](images/MCP4921\_Closeup.jpg)



\## 🧰 Expected Output

Voltage linearly increases from 0 V to 3.3 V,

then linearly decreases back to 0 V,

forming a triangle-shaped waveform.

