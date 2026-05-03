# GRBL v1.1 for Atmega328p (Arduino UNO or NANO) with Backlash Compensation

## Compile
It is recommended to use avr-gcc v4.92 and not to use the Arduino IDE for compilation.

  1. Set the avr-gcc path to an environment variable.
  2. Run ```make clean & make``` for compilation.

## Upload 
**IMPORTANT:**
Do not use the Arduino IDE to upload, or do not use the ```avrdude``` command with the ```-carduino``` parameter to upload the hex file.
***This means you cannot upload the HEX file via the bootloader.***

  1. Prepare a separate Arduino board (e.g., Arduino Mega2560) and burn the ArduinoISP sketch.
  2. Wire up the two Arduino boards as shown in the [figure](https://docs.arduino.cc/static/a2d9d884287f098ba5ef53a61943adc5/e07e9/MegaToUNO.jpg).
  3. Run command:
     ```
     avrdude -C[your avrdude.conf path] -v -patmega328p -cstk500v1 -PCOM6 -b19200 -Uflash:w:[your grbl.hex]:i
     ```

## Set Backlash Compensation
    $140=x.xxx  ;X-axis backlash compensation, unit: mm 
    $141=x.xxx  ;y-axis backlash compensation, unit: mm 
    $142=x.xxx  ;z-axis backlash compensation, unit: mm
    

## Thanks
  Jeff Dill
