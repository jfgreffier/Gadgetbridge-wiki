## CAUTION
This feature **has the potential to brick your Amazfit Cor**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

The Amazfit Cor requires the  `Mili_tempo.*` files. For **tested versions** and **known issues** check [below](#known-firmware-versions).

## Installing the firmware
Copy the desired Amazfit Cor firmware and resource files as a `*.res` and `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge FW/App Installer activity should then be started and guide you through the installation process.

### Recommended flashing order:
1. Mili_tempo.fw
2. Mili_tempo.res (The Cor will tell you when needed)

Flashing the `*.fw` triggers a reboot and will show a screen which will ask you to flash the .res if your version is outdated.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.


## Known firmware Versions

Original Firmware Version: ?.?.?.??

fw ver    | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
----------|-----------|--------|-------------------|---------|--------|---------
0.0.2.2  | 2.4.2   | no | ? | 1 | f3ff0f1d621fa3960de5f42b5b64295f | n/a
0.0.2.3  | 3.0.0   | no | ? | 1 | bb358323aefbf6ec67d6fc25dbd7fac8 | 4d8d8af74857ff6224dea9a7d02a86b3
1.0.5.00 | 3.0.3   | no | ? | 2 | 04e46562c0e7f8a2394649b7fa98be7a | 2a39e5ff2bfed7b793588014565c1eda
1.0.5.12 | 3.0.5   | no | ? | 7 | 2c18d8c0e81d83ab3a6811689fabaaf4 | 479c51cece9672220672130568f16879
1.0.5.25 | 3.0.7   | no | ? | 8 | f0687f0a9bf3f88957919f79e6fd94ca | 9b061313a390efa6b26b479dccc8c24c
1.0.5.26 | 3.0.6   | no | ? | 9 | 55104eb85661e809e9b8cb2e75f32d7f | 6aebdc56751ce034b279cd4a2803b435
1.0.5.60[1] | 3.1.0   | no | ? | 27 | d4d99997e245fc1de97f0fa39c738a78 | 8c29d4dd630f7e6111c7e6fee760be0f
1.0.5.78[2] | 3.1.2   | no | ? | 33 | 3062f6e54993a14a78da7b40c30f2d8c | f1721253f815d7b73978f87af9203c0e
1.0.5.90 | 3.1.3   | no | ? | 36 | 40612776cb0133a158e72ab58e01028d | 736d21f8ce95ca446475bea9a00bbaf4
1.0.5.99 | 3.1.6.1 | no | ? | 39 | 9cecf4d92fe19c22915d3c61941d4729 | 4a01c32f6c26113769bc876c3d75689c
1.0.6.13 | 3.1.7.1 | no | ? | 40 | 8e9dc8af1057dec7572e7589055abffb | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.22 | 3.1.9   | no | ? | 40 | 3faa7285494e56adb8dad170acc25a41 | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.27 | 3.1.8.1 | no | ? | 40 | c8daa146e21cad357e5160dc46a5920e | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.31 | 3.2.0.1 | no | ? | 41 | 8f83160a5267100846346af075f247fb | bb966b847c16c61c84814d4fb4088fd7
1.0.6.41 | 3.2.2.1 | no | ? | 42 | e8dc6fd899f6788688c812bd5daada39 | c81365b58464ab507a973f24dfbe0854
1.0.6.44 | 3.2.1   | no | ? | 42 | d746d82d9b0274b7e5fd1b0b37f63792 | c81365b58464ab507a973f24dfbe0854

[1]: flash tested on lg g5 and worked correctly GB:???
[2]: flash tested on lg g5 and worked correctly GB:0.2.2.4 