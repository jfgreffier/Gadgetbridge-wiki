## CAUTION
This feature **has the potential to brick your Mi Band**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

Some less interesting technical information is in [[Mi Band Firmware Information]].

## Mi Band model
Which Mi Band do you have? There are different models and each of them needs a different `*.fw` file.

1. Model 1 (coloured LEDs): `Mili.fw`

1. Model 1A (white LEDs): `Mili_1a.fw`

1. Model 1S (white LEDs + heart rate sensor): `Mili_hr.fw`

1. Model 2 (with display + heart rate sensor): `Mili_pro.fw`

## Known firmwares' md5 / SHA256
As mentioned above, we are not allowed to distribute firmware files, these md5 values may be used to check if the firmware file you obtained is valid/is not corrupted.
**To check the md5 you may use the command `md5sum` on a GNU/Linux distribution.**

1. Model 1 (coloured LEDs): `Mili.fw`
 * 01.00.09.27 - de4e5f3bf1fb5b610b3261c7f3557ca7
 * 01.00.10.14 - 1c43d7f03c911f9ba8844ddd44bd8304
 * 01.00.11.06 - 2833690a70ec8c6699ccd3ac08b933cc
 * 01.00.12.00 - 3a941165b7b4e296ecd68cdfb0e01062
 * 01.00.15.00 - SHA256: 7B29C5EA0325338AD703291A78D6107DEC458D1409CEF987F8E8A7FD570EB9C0

1. Model 1A (white LEDs): `Mili_1a.fw`
 * 05.15.11.20 - 356a8e1f006c541b76b306d4dbfbfaea
 * 05.15.12.10 - bbb904842a807acf1e2be5e2b41d888b

1. Model 1S (white LEDs + heart rate sensor): `Mili_hr.fw`
 * 04.15.11.20 - 7be80f0061efdf660e25a2d7cb3b6660
 * 04.15.12.10 - 24d8b84f8964489b893d1cb4581dc85f
 * 04.16.4.22 - 3b3b1427078b23808dce480a85665423

1. Model 2 (with display + heart rate sensor): `Mili_pro.fw`
 * 1.0.0.39 - a98ee8d6a04b3bb4aff472e2cc91c21b
 * 1.0.0.53 - abdd122897234f40b556f775ba0b9dc2 (included in all newer Mi Fit APKs as `Mili_pro_53.fw`)
 * 1.0.1.28 - 804903543b7958c1b4f9b5c0e420bcb5
 * 1.0.1.34 - 3ae6d0abe06006fbcf0d1685ad8231bb
 * 1.0.1.39 - Firmware and Font files:
   + Mili_pro.fw:     470641716d9e63115b839cb38eaafce7
   + Mili_pro.ft:     aa1d93a7ade6fb4cd35d63ce38100df3
   + Mili_pro.ft.en:  6e18d7ddd212d74ad8d272f6738ecd6c
 * 1.0.1.47 - 045edd2b2df5876f777a14eb3bc29966
 * 1.0.1.50 - e7ecb89b71236452c1bf4a89521bc30a
 * 1.0.1.53 - 42197ff93b9f4b0c6c9eee2b5b2308f5
 * 1.0.1.54 - fa69dceb28458d99a905583ee2f8e2ef


## Installing the firmware on Mi Band 1, 1A, 1S models
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

## Installing the firmware on Mi Band 2 model
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.
On Samsung, you might need to share the fw file, then choose FW/App Installer.

**Important:** Mi Band 2 upgrades from 1.0.0.* firmware versions to newer versions (>1.0.1.* ) require to upgrade to an intermediate firmware version first. This intermediate version is 1.0.0.53 and is included in all Mi Fit APKs that supply such newer firmware. Besides the `Mili_pro.fw` file there will also be the file `Mili_pro_53.fw`. Install the latter *before* installing the `Mili_pro.fw` file.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

Starting with Firmware version 1.0.1.28 the Mi Band 2 supports text and special icon notifications. In order to get it working you need to have Gadgetbridge version >=0.18.0 and install the font files after installing the corresponding firmware file. These font files are located in the same directory as the firmware files and named `Mili_pro.ft*` (currently `Mili_pro.ft` and `Mili_pro.ft.en`). The installation process is the same as with the firmware file.

**Note 2:** Text and special icon support is still under development and has currently limited functionality.