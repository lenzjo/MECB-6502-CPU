# TLC-6502-CPU for MECB

This is the latest version of my 6502 pcb with several useful additions.

There are 3 sets of pin headers marked with **NMOS** and/or **WDC**. **WDC** refers to Western Digitals 65C02, If you're using that then jumper the pins marked **WDC**, otherwise jumper the **NMOS** marked pins.

This pcb uses a 16Mhz oscillator that is divided down to 1, 2, 4 and 8 Mhz. Jumper the relevant pair of pins for the clock speed you want.

The button's usage is jumper selectable. The **RESET** pin is connected to the reset line and the **PANIC** pin is connected to the **NMI** line. **PANIC** is only useful if your backplane has **Reset** button on it already, like mine. I am currently writing the needed firmware addition to TLCmon. If you are not using TLCmon then you will have to supply the necessary firmware.

The last set of pins (**EEPROM**) allow you to select if the eeprom is in either read or write mode. Under normal usage the **RD** pin should be jumpered.

You may have noticed the socket with double row pins. I have made a 28pin zif socket adapter that has pins spaced at 7.62mm. So on the pcb you use a cheap socket for the inner row of pins. When, if ever ;) , you finish developing your firmware you can solder in two rows of turned pins on the outer rows. I have included the gerbers for the adapter in the **gerbers** directory.


