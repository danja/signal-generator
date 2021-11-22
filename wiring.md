### AD9833

DAT -> Arduino Pin 11 // SPI Data pin
CLK -> Arduino Pin 13 // SPI Clock pin
FSY -> Arduino Pin 10 // SPI Load pin (FSYNC in AD9833 terminology)
CS -> Arduino Pin 9 // chip select for MCP41010

### Rotary Encoders

3 Inputs required for each : SW, A & B

GND – The Ground connection.
+V – The VCC or positive supply voltage, usually 3.3 or 5-volts.
SW – The pushbutton switch output. When the shaft is depressed this goes to ground level.
DT – The Output A connection.
CLK – The output B connection.

### ESP32 Devkit V1 DOIT (Banggood)

```
Pin
1 EN - 100n -> GND
2 GPIO 36 ADC -> JOYSTICK X f1f
3 GPIO 39 ADC -> JOYSTICK Y f2f
4 GPIO 34 ADC -> POT larynx
5 GPIO 35 ADC -> POT pitch
6 GPIO 32 ADC -> POT f3f
7 GPIO 33 ADC -> POT f3q
8 GPIO 25 DIGITAL -> 100R -> DAC WSEL
9 GPIO 26 DIGITAL -> 100R -> DAC BLCK
10 GPIO 27 DIGITAL 100R -> -> DAC DIN
11 GPIO 14 DIGITAL -> SWITCH aspirated [JTAG]
12 GPIO 12 DIGITAL -> SWITCH sf3 [JTAG]
13 GPIO 13 DIGITAL -> SWITCH voiced [JTAG]
14 GPIO 9 (unavailable)
15 GPIO 10 (unavailable)
16 GPIO 11 (unavailable)
17 GND
18 VIN

19 3V3
20 GPIO 6 (unavailable)
21 GPIO 7 (unavailable)
22 GPIO 8 (unavailable)
23 GPIO 0 (limited use)
24 GPIO 15 DIGITAL -> TOGGLE T1 [JTAG]
25 GPIO 2 DIGITAL -> TOGGLE T2
26 GPIO 4 DIGITAL -> TOGGLE T4
27 GPIO 16 [UART 2 TX] DIGITAL -> TOGGLE T0
28 GPIO 17 [UART 2 RX] DIGITAL -> SWITCH x5
29 GPIO 5 DIGITAL -> SWITCH x7 (needed 10k pulldown resistor)
30 GPIO 18 DIGITAL -> SWITCH x6
31 GPIO 19 DIGITAL -> SWITCH sf1
32 GPIO 21 [I2C SDA]  -> MIDI IN ...(((was DISPLAY?)))
33 GPIO 3 [UART 0 RX] ...(((was MIDI IN)))
34 GPIO 1 [UART 0 TX] ...(((wasMIDI OUT)))
35 GPIO 22 [I2C SCL] -> MIDI OUT ...(((wasDISPLAY?)))
36 GPIO 23 DIGITAL -> SWITCH sf2
```

### JTAG

```
ESP32       JTAG

EN          TRST_N
MTDO/GPIO15 TDO
MTDI/GPIO12 TDI
MTCK/GPIO13 TMS
GND         GND
```
