# OtterPill

STM32F072 devboard featuring USB 2.0 full-speed, DFU Bootloader, USB-PD Phy, Arduino nano alike pinout and size.

HW v1.1 is finished and tested, v1.2 will be finished and tested soon. New features/changelog: BOM cost reduction by ~40%, PCB can be fully populated by JLCSMT, more efficient buck converter (PCB gets less warm at 20V), GND-hook for probing, Reset-Pin will be exposed as pad, power pads for 20V/5A

More documentation and firmware examples will be aviable soon (including pinout diagram). 

## Building and Flashing
### Via Arduino

[You can build and flash the firmware via Arduino as described here.](https://github.com/stm32duino/Arduino_Core_STM32)

## Via Makefile and DFU

Or you can generate a basic firmware, with HAL init and Makefile, with CubeMX. The binary can then be build with make and flashed with dfu-utils. To enter DFU mode, press and hold the Button while plugging in power.

    $ make
    $ dfu-util -a 0 -s 0x08000000:leave -D build/firmware.bin

## USB-PD example firmware

This is a working USB-PD example using ChibiOS, a new voltage can be requested by pressing the Button.

[https://github.com/Jan--Henrik/USB-PD-Firmware](https://github.com/Jan--Henrik/USB-PD-Firmware)

## Images

![](images/1.jpg)
![](images/2.jpg)
![](images/3.jpg)
![](images/4.jpg)
