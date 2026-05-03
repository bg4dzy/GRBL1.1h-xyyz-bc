# GRBL v1.1 for Atmega328p (Arduino UNO or NANO) with backlash compensation

## Compile
- It is recommended to use avr-gcc v4.7.3 and not to use the Arduino IDE for compilation. 
1.Set the avr-gcc path to an environment variable.
2.Run make ```clean & make``` for compilation.

## Upload 
- **IMPORTANT:** Do not use the Arduino IDE to upload, or do not use the ```avrdude``` command with the ```-carduino``` parameter to upload the hex file.
This means you cannot upload the HEX file via the bootloader.
You must use another Arduino Board as 
