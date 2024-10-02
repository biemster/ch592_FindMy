ch592 FindMy firmware
=======================

## Installation
Based on [rgoulter/ch592-ble-hid-keyboard-example](https://github.com/rgoulter/ch592-ble-hid-keyboard-example) and [Suniasuta makefile template](https://github.com/Suniasuta/CH592_Makefile_Template)

The firmware can be compiled with the xpack riscv compiler: https://github.com/xpack-dev-tools/riscv-none-elf-gcc-xpack

The ELF can be flashed to the CH592 using [wchisp](https://github.com/ch32-rs/wchisp). (Enter the CH592 bootloader by holding down BOOT when connecting it using USB).\
The SDK for CH592 from the openwch EVT is vendored under ``sdk/``. (Encoding has been changed from gbk to utf-8). 

``make`` to compile \
``make clean`` to clean/remove the compiled elf \
``make flash`` to flash \

## Further preparation
I assume here you are already familiar with the FindMy scripts from `biemster/FindMy`. If you're not, please refer to that repository for further info.
1. Generate a `.keys` file with `FindMy/generate_keys.py`
2. Add the key to the firmware using the `prep_fw.py` script like this: `./prep_fw.py <path to .keys file>`
3. Flash the new `FindMy_XXXXXXX.bin` file using `wchisp`

## Retrieving the location of the module
This is explained in more detail in the `FindMy` repository, but boils down to running the `request_reports.py` script in the same
directory as the `.keys` file generated here.
