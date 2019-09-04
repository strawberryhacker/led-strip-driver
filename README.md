# WS2812b driver

This is a simple ws2812b driver. This means that the CPU only can drive on led strip at a time. This library also supports 
newer ATmega chip such
as the ATmega4809, and the XMEGA series of microcontrollers.

## Use
1) Place the .h and the .c file in your solution. If you place the header file in a folder, you can add the directory of that 
folder to 
the Toolchain -> AVR/GNU C Compiler -> Directories list.
2) In the header file, change the defines specifying where the led strip is connected, and if neccessary change the frequency
3) Include the headerfile whereever you want to use it ```#include "ws2812b.h"```
4) Define the number of leds that you want to control ```#define NUMBER_OF_LEDS 100```
5) Make a list containing all the leds ```color led_strip[NUMBER_OF_LEDS]```
6) Update the content of the led strip ```led_strip[5] = (color){ 20, 0, 100 }```
7) Call the function that pushes the data to the led strip ```update_led_strip(led_strip, NUMBER_OF_LEDS)```
