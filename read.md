
## SHININGIC Solar LED String 8-Function Controller

**1. Features**
- Output voltage: 3.3V
- Fast short-circuit protection between channels
- Input current up to 400mA (white LED string) @ 1.2V
- Can drive red or yellow LED strings with up to 300mA @ 2.4V
- Built-in button for selecting flashing modes
- Press and hold the touch switch for 3 seconds to turn off the light; standby current as low as 9μA
- High efficiency: 90%
- Optional SOP8 and DIP8 packages

**2. Description**
The YX8628H adopts a dual-channel bridge output structure, greatly simplifying the system design. It requires only two wires to drive dual-color LED strings, reducing the number of output wires compared to traditional designs. The maximum output current of 300mA supports large-scale LED string applications (note: if the VOUT terminal is connected to a load, the total output current from LEDs and other loads must not exceed the maximum capability). It provides 3.3V constant voltage output.

The chip has built-in protection circuits that guard against short circuits between channels and automatically resume operation after faults are cleared.

Multiple flashing effects are available and can be selected via the Key button. Holding the Key button for 3 seconds turns the lights off, minimizing power consumption, and only requires external capacitors and inductors for operation. During solar charging, the flashing mode remains unchanged. The extremely low operating current further reduces system power consumption.

**3. Application Range**
- Christmas lights
- Running/waterfall lights
- Decorative lights
- Other LED light control systems

**4. Typical Application**

*Note: During PCB layout, capacitor C1 between VOUT and GND should be placed as close as possible.*

**5. Ordering Information**

| Device Model | Order Code         | Package Description | Temperature Range | Package Marking | Packaging Option | Remarks         |
|--------------|-------------------|---------------------|------------------|-----------------|-----------------|-----------------|
| YX8628H      | YX8628HS08NRA2    | SOP8                | -40°C to +125°C  |                 | Tape and Reel   |                 |
| YX8628H      | YX8628HDP08TA2    | DIP8                | -40°C to +125°C  |                 | Tube            |                 |

**6. Pin Information**

| Pin | Name  | Description                    |
|-----|-------|--------------------------------|
| 1   | LX    | Boost switch pin               |
| 2   | GND   | Chip ground                    |
| 3   | BAT   | Battery positive               |
| 4   | SOL   | Solar panel positive           |
| 5   | Key   | Mode control                   |
| 6   | L2    | Output port 2                  |
| 7   | L1    | Output port 1                  |
| 8   | VOUT  | Internal power/constant voltage output |

**7. Absolute Maximum Ratings**

| Description              | Range      | Unit      |
|--------------------------|------------|-----------|
| Input voltage (BAT)      | -0.3~5V    | V         |
| Other pins               | -0.3~5V    | V         |
| Maximum charging current | 450        | mA        |
| Maximum junction temp.   | 150        | °C        |
| Operating temp. range    | -25~85     | °C        |
| Storage temp. range      | -40~125    | °C        |
| Recommended soldering    | +260 (5s)  | °C        |
| ESD (HBM)                | 2000       | V         |
| ESD (MM)                 | 200        | V         |

**8. Thermal Dissipation**

| Description             | Range      | Unit      |
|-------------------------|------------|-----------|
| Thermal resistance (θJA)| SOP8 150   | °C/W      |
|                         | DIP8 120   | °C/W      |
| Power dissipation (PD)  | SOP8 0.6   | W         |
|                         | DIP8 0.8   | W         |

**9. Recommended Operating Conditions**

| Description                  | Range      | Unit      |
|------------------------------|------------|-----------|
| Junction temp.               | -40~125    | °C        |
| Ambient temp.                | -40~85     | °C        |
| Input voltage                | 0.9~3.3    | V         |
| Max input current (white LED)| 400@1.2V   | mA        |

**10. Electrical Characteristics**

*(VBAT = 1.2V, CIN=10uF, COUT=22uF, TA=25°C, unless otherwise specified)*

| Parameter                | Symbol  | Test Condition                  | Min   | Typ   | Max   | Unit  |
|--------------------------|---------|---------------------------------|-------|-------|-------|-------|
| Input voltage            | VIN     |                                 | 0.9   |       | 3.3   | V     |
| SOL shutdown current     | IQ1     | VBAT 1.2V, VSOL>0.4V            |       |       | 8     | μA    |
| Key long press current   | IQ1     | VBAT=1.2V, Key held 3s          |       |       | 8.5   | μA    |
| Startup voltage          | VSTART  | Iload=1mA, Vin: 0→2V            | 0.8   |       | 1.0   | V     |
| Hold voltage             | VHOLD   | Iload=1mA, Vin: 2→OV            |       | 0.75  |       | V     |
| Oscillation frequency    | Fosc    |                                 |       | 270   |       | kHz   |
| Current limit            | Ilimit  |                                 | 800   | 1000  | 1200  | mA    |
| VOUT output voltage (SOL low) | VOUT1 | SOL low                         | 3.23  | 3.3   | 3.36  | V     |
| VOUT output voltage (SOL high)| VOUT2 | SOL high                        |       | VBAT  |       | V     |
| Solar control threshold  | V开关   | VBAT=1.2V                       |       | 0.34  |       | V     |
| Solar enable resistance  | RSOL-GND|                                 |       | 14    |       | kΩ    |
| Min. charging voltage diff.| VCHAmin| VBAT 1.2V, ISOL-OUT=1mA         |       | 180   |       | mV    |
| Charging current         | ICH     | VBAT 1.2V, VSOL-OUT=350mV       |       | 450   |       | mA    |
| Efficiency               | η       |                                 |       | 85    | 90    | %     |

*Note 1: When the battery voltage drops below its typical value, the LED will be turned off, and the output voltage will decrease as the input voltage drops, but it will not completely shut down. Only when the input voltage drops below 0.55V will the output voltage equal the input voltage.*

*Note 2: Conditions: L=22uH (r<0.12), tantalum capacitor.*

**11. Functional Block Diagram**

*(Not translated in detail; see original for diagram.)*

**12. Application Circuit**

*Note: Output capacitor C2 must not be less than 10μF or greater than 22μF, otherwise there may be delayed startup. The switch should be placed on the positive power rail, not the negative, to avoid charging issues and startup problems.*

**13. Typical Characteristics Curves**

*(Not translated in detail; see original for graphs.)*

**14. PCB Reference Layout**

- Place C2 as close as possible to pin 8 of the IC, with the capacitor’s negative terminal close to the chip’s GND.
- Pin 2 (GND) should be close to the battery’s negative terminal, with short traces. C1 should also be close to the IC.

**15. Functional Description**

The YX8628H is an 8-function solar LED string controller chip, suitable for solar products using 1–2 rechargeable 1.2V batteries. It features boost, light control, and eight functional modes.

**Charge/Discharge and Enable Control:**
- SOL pin connects to the solar panel positive, BAT pin to the rechargeable battery positive.
- During the day, the solar panel converts light to electricity; at night, the battery powers the LEDs.
- An internal comparator detects the voltage between SOL and BAT. If SOL is 28% higher than BAT, the chip shuts down the LEDs. If SOL is 20% lower than BAT, the chip resumes operation, enabling automatic day/night control without affecting charging.

**Function Control:**
- The Key pin is for LED mode selection. If not connected, the chip defaults to 7 automatic cycling modes.
- Pressing the Key cycles through modes; holding it for 3 seconds shuts down the LEDs for minimum power consumption.
- The chip includes a complete flashing mode program. On power-up, it starts flashing and cycles through modes with each press.

**Eight Modes:**
1. Modes 2–8 cycle
2. Star flash (two-speed)
3. Alternating flash (four-speed)
4. Single channel fade in/out (variable speed)
5. Single flash four times, alternating flash four times
6. All channels fade in/out (variable speed)
7. Single flash four times
8. Full on

**Key Long Press:**
- Key has debounce; holding for 3s shuts down, reducing power to <9μA. Press again to unlock and cycle modes.

**Mode Memory:**
- After battery power loss, the chip defaults to mode 1. If battery remains above 0.5V, solar charging does not affect the mode; the previous mode is retained after sunset.

**Input Current Adjustment:**
- Adjust LED current by changing the series resistor. No need to adjust the inductor. Use 22μH/0410 or 0510 inductors; avoid 0307 for lower loss. Output capacitors: 10μF or 22μF.

**PCB Layout:**
- Input and output capacitors should be close to the IC, especially VOUT and GND.
- Battery negative should be close to chip GND for stability.

**Power Consumption:**
- Junction temperature depends on ambient temperature, PCB layout, load, and package.
- Power dissipation and junction temperature can be calculated as:
  - $$ PD = R_{DS(ON)} \times I_{OUT}^2 $$
  - $$ T_J = PD \times \theta_{JA} + T_A $$
  - Where:
    - $$ T_J $$: Junction temperature
    - $$ T_A $$: Ambient temperature
    - $$ \theta_{JA} $$: Package thermal resistance

**16. Package Description**

*(Dimensions and mechanical drawings for SOP8 and DIP8 packages; check attachment *
