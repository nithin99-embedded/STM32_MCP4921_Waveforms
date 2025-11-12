\# MCP4921 Square Wave using STM32 Nucleo-F103RB



This project generates a \*\*square wave\*\* (0V ↔ 3.3V) using the MCP4921 12-bit SPI DAC.





---





\## 🧩 Description

\- STM32 alternately writes \*\*0\*\* and \*\*4095\*\* to MCP4921.

\- Output voltage switches between \*\*0V\*\* and \*\*3.3V\*\*.

\- Each state lasts \*\*2000 ms\*\*, giving a 4 Hz square wave.



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



\## 📈 Expected Output

A square waveform toggling between \*\*0 V\*\* and \*\*3.3 V\*\*  

with a period of 4 second (frequency ≈ 4 Hz).

