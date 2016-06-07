**FIRMWARE UPDATES ARE ALWAYS AT YOUR OWN RISK!**

Based on our tests the following should be possible:

* Up or downgrade from any 1.x/2.x firmware to any 1.x/2.x firmware.
* Up or downgrade from 3.x to any 3.x.
* Upgrade from 2.x to 3.x via migration firmware

## Upgrading from 2.x to 3.x

### Warnings
* Upgrading from 2.x to 3.x will update the recovery to 3.8
* Downgrading from 3.x to 2.x won't downgrade the recovery firmware and your data will be lost, we haven't tested it and do not know the correct procedure to update to 3.x again

1. Flash the migration firmware (tested 3.x-migration_v1_5_v3.8-mig9.pbz) and **wait till the Pebble reboots, ignoring errors if any** 
2. The pebble will start in a 3.x recovery, flash the real firmware from there (tested Pebble-3.8-v1_5.pbz)

**NOTE: Install firmware files from .pbz files by selecting them from a file manager and opening them in Gadgetbridge's App/FW Installer**

**DO NOT FLASH A RECOVERY FIRMWARE, IF YOU WANT TO UPDATE THE RECOVERY FIRMWARE TO A NEWER VERSION, INSTALL THE LATEST MIGRATION, AND THEN THE NORMAL FIRMWARE AGAIN**

## Firmware Download Locations
### Pebble
https://pebblefw.s3.amazonaws.com/pebble/v1_5/release-v3.8/pbz/3.x-migration_v1_5_v3.8-mig10.pbz (MIGRATION)

https://pebblefw.s3.amazonaws.com/pebble/v1_5/release-v3.8/pbz/Pebble-3.12.1-v1_5.pbz

### Pebble Steel
https://pebblefw.s3.amazonaws.com/pebble/v2_0/release-v3.8/pbz/3.x-migration_v2_0_v3.8-mig10.pbz (MIGRATION)

https://pebblefw.s3.amazonaws.com/pebble/v2_0/release-v3.8/pbz/Pebble-3.12.1-v2_0.pbz

### Pebble Time
https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-3.13-snowy_dvt.pbz

### Pebble Time Steel
https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-3.13-snowy_s3.pbz

### Pebble Time Round
https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-3.13-spalding.pbz
