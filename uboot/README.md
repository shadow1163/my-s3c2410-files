# uboot
-- branch nor-flash: boot from nor flash

--branch master: boot from nand flash, it did not using skyeye.

# transfer file to board using serail console.
kermit

# load u-boot to SDRAM
add line 

#define CONFIG_SKIP_LOWLEVEL_INIT

#define CONFIG_SKIP_RELOCATE_UBOOT

to file include/configs/smdk2410.h

change TEXT_BASE = 0xa3f80000 on config.mk file

# Nand flash
nand erase 0x280000 0x400000

nand write 0x30008000 0x280000 0x400000
