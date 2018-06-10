**FIRMWARE UPDATES ARE ALWAYS AT YOUR OWN RISK!**

## Foreword
The following should be possible for Pebble and Pebble Steel:
* Up or downgrade from 1.x/2.x to any 1.x/2.x firmware
* Upgrade from 1.x/2.x to 3.x via migration firmware

The following should be possible for all models:
* Up or downgrade from 3.x/4.x to any 3.x/4.x firmware

## General flashing instructions
There are three types of firmware. Each instance of a firmware comes in its own .pbz file.

_Recovery firmware_ is the only firmware available in a new Pebble, and when a Pebble is given a factory reset. Its sole purpose is to flash another firmware. *Never flash a recovery firmware separately!*

_Migration firmware_ is a special firmware that embeds recovery firmware. It must be used to switch between major firmware versions. The only use case is upgrading the Pebble and Pebble Steel from 1.x/2.x to 3.x. Ignore migration firmware in all other situations.

_Normal firmware_ contains the regular software that provides all functions. It must be flashed when the Pebble is used for the first time, after a factory reset, or after a migration firmware is flashed. It can be flashed for minor version upgrades (e.g. 4.0 to 4.3). This firmware is erased after a factory reset.

Pair the Pebble first before flashing a firmware. After it is paired and connected, select the firmware's .pbz file in an Android file manager. Open it with App/FW Installer to flash it.

First read the special flashing instructions for different models before continuing to the firmware tables.

## Special flashing instructions for Pebble and Pebble Steel
To upgrade a recovery/normal firmware from 1.x/2.x to 3.x it is required to first flash a migration firmware. Do this in two steps:

1. Flash a migration firmware and let the Pebble reboot. Ignore any errors.
2. Flash normal firmware.

Tested combinations include:

| Model  | Migration firmware (step 1)       | Normal firmware (step 2) | Tested by       |
|--------|-----------------------------------|------------------------- |-----------------|
| Pebble | 3.x-migration_v1_5_v3.8-mig9.pbz  | Pebble-3.8-v1_5.pbz      | ashimokawa      |
| Pebble | 3.x-migration_v1_5_v3.8-mig10.pbz | Pebble-3.12.2-v1_5.pbz   | PabloCastellano |

### Note
* Upgrading from 1.x/2.x to 3.x will update the recovery to 3.8.
* It is advised not to downgrade. Downgrading from 3.x to 2.x won't downgrade the recovery firmware and your data will be lost. The correct procedure to update to 3.x again is unknown.

## Special flashing instructions for Pebble Time, Pebble Time Steel and Pebble Time Round
It is possible to upgrade from 3.x to 4.x. A migration firmware is not required. Just flash the normal firmware.

## Special flashing instructions for Pebble 2
Flashing a firmware on a Pebble 2 can fail at 0%. Do not panic. Try the following process on your Android device:
1. Unpair the Pebble 2 in Gadgetbridge.
2. Turn Bluetooth off and on
3. Pair the Pebble 2 again.
4. Flash the firmware again.

## Firmware download locations
If you think there might be something newer available, please check the [Pebble wiki](http://www.pebbledev.org/wiki/Firmware_Updates/) on how to find out for real.

### Normal firmware

| Model                                           | 3.12.3     | 4.0     | 4.0.1     | 4.0.2     | 4.1     | 4.2     | 4.3     |
|:----------------------------------------------  | ---------- | ------- | --------- | --------- | ------- | ------- | ------- |
| Pebble (Kickstarter edition, HW revision: V2R2) | [3.12.3](https://pebblefw.s3.amazonaws.com/pebble/ev2_4/release-v3.8/pbz/Pebble-3.12.3-ev2_4.pbz)  |         |           |           |         |         |         |
| Pebble (other editions)                         | [3.12.3](https://pebblefw.s3.amazonaws.com/pebble/v1_5/release-v3.8/pbz/Pebble-3.12.3-v1_5.pbz) |         |           |           |         |         |         |
| Pebble Steel                                    | [3.12.3](https://pebblefw.s3.amazonaws.com/pebble/v2_0/release-v3.8/pbz/Pebble-3.12.3-v2_0.pbz)  |         |           |           |         |         |         |
| Pebble Time                                     |            | [4.0](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.0-snowy_dvt.pbz) | [4.0.1](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.0.1-snowy_dvt.pbz) | [4.0.2](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.0.2-snowy_dvt.pbz) | [4.1](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.1-snowy_dvt.pbz) | [4.2](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.2-snowy_dvt.pbz) | [4.3](https://pebblefw.s3.amazonaws.com/pebble/snowy_dvt/release-v3.8/pbz/Pebble-4.3-snowy_dvt.pbz) |
| Pebble Time Steel                               |            | [4.0](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.0-snowy_s3.pbz) | [4.0.1](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.0.1-snowy_s3.pbz) | [4.0.2](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.0.2-snowy_s3.pbz) | [4.1](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.1-snowy_s3.pbz) | [4.2](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.2-snowy_s3.pbz) | [4.3](https://pebblefw.s3.amazonaws.com/pebble/snowy_s3/release-v3.8/pbz/Pebble-4.3-snowy_s3.pbz) |
| Pebble Time Round                               |            | [4.0](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.0-spalding.pbz) | [4.0.1](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.0.1-spalding.pbz) | [4.0.2](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.0.2-spalding.pbz) | [4.1](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.1-spalding.pbz) | [4.2](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.2-spalding.pbz) | [4.3](https://pebblefw.s3.amazonaws.com/pebble/spalding/release-v3.8/pbz/Pebble-4.3-spalding.pbz) |
| Pebble 2 (SE and HR)                            |            | [4.0](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.0-silk.pbz) | [4.0.1](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.0.1-silk.pbz) | [4.0.2](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.0.2-silk.pbz) | [4.1](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.1-silk.pbz) | [4.2](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.2-silk.pbz) | [4.3](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/Pebble-4.3-silk.pbz) |

### Migration firmware
Use these to migrate earlier Pebble models from 1.x/2.x to 3.x.

| Model                                           | 3.8-mig9 | 3.8-mig10 |
|:----------------------------------------------  | -------- | --------- |
| Pebble (Kickstarter edition, HW revision: V2R2) | [3.8-mig9](https://pebblefw.s3.amazonaws.com/pebble/ev2_4/release-v3.7/pbz/3.x-migration_ev2_4_v3.8-mig9.pbz) | [3.8-mig10](https://pebblefw.s3.amazonaws.com/pebble/ev2_4/release-v3.8/pbz/3.x-migration_ev2_4_v3.8-mig10.pbz) |
| Pebble (other editions)                         | [3.8-mig9](https://pebblefw.s3.amazonaws.com/pebble/v1_5/release-v3.7/pbz/3.x-migration_v1_5_v3.8-mig9.pbz) | [3.8-mig10](https://pebblefw.s3.amazonaws.com/pebble/v1_5/release-v3.8/pbz/3.x-migration_v1_5_v3.8-mig10.pbz) |
| Pebble Steel                                    | [3.8-mig9](https://pebblefw.s3.amazonaws.com/pebble/v2_0/release-v3.7/pbz/3.x-migration_v2_0_v3.8-mig9.pbz) | [3.8-mig10](https://pebblefw.s3.amazonaws.com/pebble/v2_0/release-v3.8/pbz/3.x-migration_v2_0_v3.8-mig10.pbz) |

### Recovery firmware
These are listed for historical reasons only. **Do not use**.

| Model                                           | 4.0.1 |
|:----------------------------------------------  | ----- |
| Pebble Time                                     | |
| Pebble Time Steel                               | |
| Pebble Time Round                               | |
| Pebble 2 (SE and HR)                            | [4.0.1](https://pebblefw.s3.amazonaws.com/pebble/silk/release-v3.8/pbz/recovery_silk_v4.0.1-prf6.pbz) |