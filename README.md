# LED Sensor LED

This circuit contained a LDR or photo cell. When the photo resistor detects light the 555 timer turns on and the LED turns on as a result. When it is covered or it is dark, the LED turns off.

![Hero Image](attachments/Bird%20with%20Knife%20PCB.png.png)

## Features

- The board contains a light depedent resistor (LDR) or a photo resistor. 
- It senses how much light is coming and proceeds to activate the 555 timer as it is connected to pin 8, VCC of the 555 timer.
- Potentiometer adjusts the light sensitivity.
  
## Schematic

![Schematic Image](attachments/image22.png)

## PCB

![PCB Image](attachments/image18.png)

## BOM

| Designator | Value |
| ---------- | ----- |
| R1         | 10K   |
| R2         | 22k   |
| R3         | 4.7k   |
| R4         | LDR   |
| R5         | 330   |
| R6         | 330   |
| C1         | 0.1uF |
| C2         | 0.01uF |
| C3         | 10uF |
| C4         | 10uF |
| U1         | NE555 |
| RV1         | 100k |
| D1         | LED |
| D2         | LED |

## Assembly / Usage

Best to assemble smaller parts first. Resistor, then capacitator, LEDs, and potentiometer. I would do the USB connector port last. Since I only put in the designator values, R1 is 10k, R2 is 22k, R3 is 4.7k, R3 is the LDR, R5 and R6 are 330 ohm resistor.
For capacitor, C1 is 0.1u and C2 is 0.01u, C3 and C4 is 10u. LED can be any color but red would be better to make the bird evil.

The LDR does not need to be soldered in flush.
