**FIRMWARE UPDATES ARE ALWAYS AT YOUR OWN RISK!**

Based on our tests the following should be possible:

* Up or downgrade from any 1.x/2.x firmware to any 1.x/2.x firmware.
* Up or downgrade from 3.x to any 3.x.
* Upgrade von 2.x to 3.x via migration firmware

**WARNING: IF YOU WANT TO UPDATE YOUR OG PEBBLE FROM 2.x TO 3.x, READ THIS**

**YOUR RECOVERY WILL BE UPDATED TO 3.8-prf9**

**DOWNGRADING FROM 3.8.x to 2.x IS UNTESTED, IT MAY BRICK YOUR WATCH**

1. Flash the migration firmware (tested 3.x-migration_v1_5_v3.8-mig9.pbz) and **wait till the Pebble reboots, ignoring errors if any** 
2. The pebble will start in a 3.x recovery, flash the real firmware from there (tested Pebble-3.8-v1_5.pbz)

**NOTE: Install firmware files from .pbz files by selecting them from a file manager and opening them in Gadgetbridge's App/FW Installer**

**DO NOT FLASH A RECOVERY FIRMWARE, IF YOU WANT TO UPDATE THE RECOVERY FIRMWARE TO A NEWER VERSION, INSTALL THE LATEST MIGRATION, AND THEN THE NORMAL FIRMWARE AGAIN**
