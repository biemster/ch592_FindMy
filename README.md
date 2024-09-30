ch592 FindMy firmware
=======================

Based on [rgoulter/ch592-ble-hid-keyboard-example](https://github.com/rgoulter/ch592-ble-hid-keyboard-example) and [Suniasuta makefile template](https://github.com/Suniasuta/CH592_Makefile_Template)

The elf can be flashed to the CH592 using [wchisp](https://github.com/ch32-rs/wchisp). (Enter the CH592 bootloader by holding down BOOT when connecting it using USB).\
The SDK for CH592 from the openwch EVT is vendored under ``sdk/``. (Encoding has been changed from gbk to utf-8). 

``make`` to complie \
``make clean`` to clean/remove the compiled elf \
``make flash`` to flash \
``make f`` to compile and flash.
