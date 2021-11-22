# signal-generator

A simple audio-frequency+ waveform generator

I need a half-decent one of these, and it also makes a good use case for my RDF project management code/data noodling.

## Core Components

Cheap modules based around these devices :

- [AD9833](#ad9833) Signal Generator
- [ESP32](#esp32) Microcontroller
- [PAM8403](pam8403) Audio Amplifier
- [LCD Display](lcd-display)
- [Rotary Encoders](rotary-encoders)
- [JTAG Debugger](jtag-debugger)

### AD9833

Has 2 channels!!

SPI

https://github.com/Carlo47/AD9833FunctionGenerator

Instead of SPI hardware pins the library uses three regular IO pins – for SCK, FSYNC(CS) and DATA(MOSI). As you can see it does not use any pin for MISO, because AD9833 registers are only writable.
https://github.com/daumemo/Arduino-AD9833-GPIO-only-library

https://daumemo.com/diy-generator-ad9833-library-and-further-output-noise-reduction-part-13/

The circuit includes an opamp (signal out on the "PGA" pin) controlled by a digipot MCP41010 (Chip select for the digipot is on the "CS" pin). I had best results with the digipot set at not quite full rate, at 247 out of 256 steps. Square wave is reasonably clean/usable up to about 1Mhz. SIN wave is nice and clean up to the max frequency of 12.5Mhz, but the amplitude drops significantly above 1Mhz. This could probably be improved with an opamp with higher gain. Overall a nice gadget, great value for money.

https://www.banggood.com/AD9833-DDS-Signal-Generator-Module-0-12_5MHz-Square-Triangle-Sine-Wave-p-1161804.html
16,19€

### ESP32

### PAM8403

### LCD Display

interfacing LCD using 4-bit mode and hence we need only 6 pins: RS, EN, D7, D6, D5, and D4 to talk to the LCD.

### Rotary Encoders

3 Inputs required for each : SW, A & B

### JTAG Debugger

GND – The Ground connection.
+V – The VCC or positive supply voltage, usually 3.3 or 5-volts.
SW – The pushbutton switch output. When the shaft is depressed this goes to ground level.
DT – The Output A connection.
CLK – The output B connection.
