## CAUTION
This feature **has the potential to brick your Mi Band 2**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

## Choosing the right firmware version for your Model

Device Name | HW Revisions | `*.fw` file
------------|--------------|------------
Mi Band 2   | V0.1.3.2 V0.1.3.3 V0.1.3.4 | Mili_pro.fw
Mi Band 2   | ?            | Mili_pro_tph.fw
Mi Band 2   | V0.16.2.2    | Mili_pro_tph_as7000.fw
Mi Band 2   | ?            | Mili_pro_tph_indian.fw
Mi Band HRX | ?            | Mili_pro_i.fw

## Installing the firmware
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.

**Important:** Mi Band 2 upgrades from 1.0.0.* firmware versions to newer versions (>1.0.1.* ) require to upgrade to an intermediate firmware version first. This intermediate version is 1.0.0.53 and is included in all Mi Fit APKs that supply such newer firmware. Besides the `Mili_pro.fw` file there will also be the file `Mili_pro_53.fw`. Install the latter *before* installing the `Mili_pro.fw` file.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

Starting with Firmware version 1.0.1.28 the Mi Band 2 supports text and special icon notifications. In order to get it working you need to have Gadgetbridge version >=0.18.0 and install the font files after installing the corresponding firmware file. These font files are located in the same directory as the firmware files and named `Mili_pro.ft*` (currently `Mili_pro.ft` and `Mili_pro.ft.en`). The installation process is the same as with the firmware file.

**Note 2:** Text and special icon support is still under development and has currently limited functionality.

**Note 3:** After flashing some firmware versions the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again. Do this if you have problems connecting after a firmware update, you wont loose any data. 

# Firmware 1.0.x.x

| Version / Function | 1.0.1.54 | 1.0.1.53 | 1.0.1.50 | 1.0.1.47         | 1.0.1.39                          | 1.0.1.34                          | 1.0.1.28                          | 1.0.0.53                          | 1.0.0.39                          | 1.0.0.34 | 1.0.0.19                          |
| ----------------------- | -----------------------|------ |------ |------ | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| recommended                   | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model) | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model) | no | no |yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model)      | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model)    | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model)  | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model) | yes[*](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Mi-Band-Firmware-Update#installing-the-firmware-on-mi-band-2-model)                               | no      | no      |
| alarms                        | work | work | work | ? |work                              | work                              | work (no smart alarms)       | ? | work                              | work (smart alarms partly?)      | work (smart alarms partly?)      |
| notifications                 | work | work | work | ? |work                              | work                              | work                              | work | work                              | work                              | work                              |
| activity recognition          | no deep sleep[1] | no deep sleep[1] | no deep sleep[1] | no deep sleep[1] | works                             | works                             | works                             | ? | works                             | works                     | works                     |
| text and special icon notifications | partial | partial | partial | ? | partial | partial | partial |no |no | no | no
| heart rate measurement        | works | works | works | ? | works                             | works                          | works                             | works | works                             | stopped working at some point (known firmware issue, not GB-related) | ? |
| Gadgetbridge FW installer no. | 47364 | 32121 | 50471 | ? |3929                             | 51770 | 32450 | 49197 | 41899                             | ? | ? |
| CRC32                         | ? | 4c44ea29 | 26913267 | ? |80f6ccbe                          | 01d1ef2d | ? | ? | 68efecd7                          | ? | ? |
| Mi Fit APK version            | 3.1.0 | 3.0.5 | 3.0.4-2.4.2 | >2.4.0 |2.3.0                             | 2.2.12 | 2.2.9 | >2.2.0 | 2.2.0                             | ? | ? |

[1]: deep sleep detection does not work properly with Gadgetbridge, see https://github.com/Freeyourgadget/Gadgetbridge/issues/686#issuecomment-343773224
