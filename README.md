# 42ES
E-ink based 42S scientific calculator (alpha version).  Uses the M5Stack Paper S3 hardware.

Remember to use a high speed micro SD card for best results when saving data.

See the 42LCmoreNotes file (in 42LC repository) for how data is saved. Also 42LCtestPrograms for Hitomezashi and Nqueens test programs

To access the Config menu, press Shift and Cat (catalog).  The catalog is not currently implemented.  But in this menu, you can save and load different calculator states.

To save a calculator state, enter a number from 1 to 99 on the stack, and press Enter. Then press the "save" softkey. To load a calculator state, enter a number from 1 to 99 on the stack and press Enter. Then the "load" softkey. If you want to change the "matrix number" variable, put the number (0 to 9) on the stack and press Enter. Then the "mtnum" softkey. The next new matrix will have that number. After 9, mtnum will wrap around back to 0 and may overwrite another matrix if it was stored there. If you want to change the program count number (useful when doing GTO ..), put the number from 0 to 14 on the stack and press Enter. Then the "pcount" softkey.

Using GTO .####

It is possible to go to a particular program by doing a GTO .####, where #### is a 4 digit number for the address. To go to address 99, put GTO .0099
Entering a number more than 1499 may lead to unpredictable results. First program is usually 0000 to 0099, second program is usually 0100 to 0199 and so on.

Burning firmware:

This 42ES firmware may be used for non-commercial personal or educational purposes. No warranties are made on the use of the firmware. It is up to the user to verify the accuracy or precision of this calculator implementation.

Go to Github riker2072 42ES repository. Get 42ES.ino.bin, 42ES.ino.bootloader.bin and 42ES.ino.partitions.bin files. Get Windows ESP32 flash download tool at: https://www.espressif.com/en/support/download/other-tools Click on … to select 42ES.ino.bin file directory location. In the @ box, put 0x10000 Click on … to select 42ES.ino.bootloader.bin file directory location. In the @ box, put 0x0000 Click on … to select 42ES.ino.partitions.bin file directory location. In the @ box, put 0x8000 SPI speed is 40MHz, SPI mode is DIO. Check mark in the box labeled “DoNotChgBin”. My port settings are COM4, baud 115200. Connect the M5 Cardputer to your PC using a USB C cable. Click on START to burn the firmware.
