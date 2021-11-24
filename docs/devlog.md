**2021-11-24**

Trying JTAG debug with ESP-prog

undefined/home/danny/.platformio/packages/toolchain-xtensa32/bin/xtensa-esp32-elf-gdb: error while loading shared libraries: libncurses.so.5: cannot open shared object file: No such file or directory

had to install

The system seems to be talking to the esp-prog board/esp32, but it's not working...

**2021-11-22**

script for md link list -> turtle?

## ESP32 Pin allocation : from most specific

- JTAG has fixed pins

- AD9833 uses SPI - can potentially any GPIO, but might as well use built-in SPI (if available)

- rotary controllers : 2 x 3 in GPIO - SW, A & B

- Display :

#include <LiquidCrystal.h>

// Creates an LCD object. Parameters: (rs, enable, d4, d5, d6, d7)
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

- Need one analog in, one out

**2021-11-20**

Just starting.

Already reckon I need more specific terms.
