# tgyi6_chibios

ChibiOS/RT running on Turnigy TGY-i6 / FlySky FS-i6

( MKL16Z64VLH4 Cortex M0+ 64KByte Flash / 8 kByte SRAM )
It's just flashing the backlight led.
There is no kinetis KL1x port in ChibiOS, it's use the KL2x port, looks like
they are differ in the USB controller (KL1x have no).
Be careful, you may permanently brick your device with a wrong image if turn 
on secured and disable mass erase.(FSEC @0x040C==0x7E ok).
Read about the security features:
http://cache.freescale.com/files/microcontrollers/doc/app_note/AN4507.pdf
KL16 Sub-Family Reference Manual:
http://cache.freescale.com/files/microcontrollers/doc/ref_manual/KL16P80M48SF4RM.pdf

ChibiOS_3.0.2 must be one dir up or edit the makefile.
Based on the demo "RT-FREEDOM-KL25Z", edited the memory sizes in the linker scipt, added openocd
config files, some pinout mapping.

