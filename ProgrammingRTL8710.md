# Programming the RTL8710 via DAP

# Hardware
* a RTL8710 RTL00.
* a DAP board with NXP LPC11U35FHI33/501.
* some wires.
* a usb cable

# Prepare DAP board
* I use TG-LPC11U35-501. (https://developer.mbed.org/platforms/TG-LPC11U35-501/)
* Download Realtek's DAP firmware. (https://github.com/Ameba8195/Arduino/blob/master/misc/dap_firmware/DAP_FW_Ameba_V10_2_3-2M.bin)
* Program DAP firmware to DAP board.

# Wiring

| DAP board | RTL8710 RTL00 |
|---|---|
| SWCLK | 4 |
| SWIO | 6 |
| 3.3V | 8 |
| GND | 15 |

# Programming
* Connect the PC and the board with a USB cable
* The mbed drive is displayed on the PC.
* Copy ram_all.bin to the mbed drive.
* reboot RTL8710.

# List of DAP board with LPC11U35FHI33/501.
* Realtek Ameba dev board ( require pattern cut to original ameba module.)
* B&T RTL8710 debug board
* TG-LPC11U35-501. (https://developer.mbed.org/platforms/TG-LPC11U35-501/)

# Remark
* You can programming the RTL8710 via J-Link and other CMSIS DAP, but you don't erase MAC address and WLAN calibration data in 0x9000 - 0xAFFF.
* Realtek's DAP firmeware prevents to erase 0x9000 - 0xAFFF.

