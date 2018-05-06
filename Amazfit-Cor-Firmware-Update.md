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

### 0.0.2 series

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
0.0.2.2  | 2.4.2   | no | ? | 1 | f3ff0f1d621fa3960de5f42b5b64295f | n/a
0.0.2.3  | 3.0.0   | no | ? | 1 | bb358323aefbf6ec67d6fc25dbd7fac8 | 4d8d8af74857ff6224dea9a7d02a86b3

### 1.0.5 series

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.0.5.00 | 3.0.3   | no | ? | 2 | 04e46562c0e7f8a2394649b7fa98be7a | 2a39e5ff2bfed7b793588014565c1eda
1.0.5.12 | 3.0.5   | no | ? | 7 | 2c18d8c0e81d83ab3a6811689fabaaf4 | 479c51cece9672220672130568f16879
1.0.5.25 | 3.0.7   | no | ? | 8 | f0687f0a9bf3f88957919f79e6fd94ca | 9b061313a390efa6b26b479dccc8c24c
1.0.5.26 | 3.0.6   | no | ? | 9 | 55104eb85661e809e9b8cb2e75f32d7f | 6aebdc56751ce034b279cd4a2803b435
1.0.5.60[1] | 3.1.0   | no | ? | 27 | d4d99997e245fc1de97f0fa39c738a78 | 8c29d4dd630f7e6111c7e6fee760be0f
1.0.5.78[2] | 3.1.2   | no | ? | 33 | 3062f6e54993a14a78da7b40c30f2d8c | f1721253f815d7b73978f87af9203c0e
1.0.5.90 | 3.1.3   | no | ? | 36 | 40612776cb0133a158e72ab58e01028d | 736d21f8ce95ca446475bea9a00bbaf4
1.0.5.99 | 3.1.6.1 | no | ? | 39 | 9cecf4d92fe19c22915d3c61941d4729 | 4a01c32f6c26113769bc876c3d75689c

### 1.0.6 series

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.0.6.13 | 3.1.7.1 | no | ? | 40 | 8e9dc8af1057dec7572e7589055abffb | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.22 | 3.1.9   | no | ? | 40 | 3faa7285494e56adb8dad170acc25a41 | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.27 | 3.1.8.1 | no | ? | 40 | c8daa146e21cad357e5160dc46a5920e | 90d41c9944a7ad75d7af6861bc61bf70
1.0.6.31 | 3.2.0.1 | no | ? | 41 | 8f83160a5267100846346af075f247fb | bb966b847c16c61c84814d4fb4088fd7
1.0.6.41 | 3.2.2.1 | no | ? | 42 | e8dc6fd899f6788688c812bd5daada39 | c81365b58464ab507a973f24dfbe0854
1.0.6.44 | 3.2.1   | no | ? | 42 | d746d82d9b0274b7e5fd1b0b37f63792 | c81365b58464ab507a973f24dfbe0854
1.0.6.49 | 3.2.2.2 | no | ? | 45 | d1cf29ae7d9b3076a4b542e17a3e20e7 | f20c1a505a284e876b2d9cf61814b79c
1.0.6.71 | 3.2.2.3 | no | ? | 46 | fabb90486cd4c5fae91c96783e0a1132 | e26222890f649711581c54839eb53121
1.0.6.75 | 3.2.3.1 | no | ? | 48 | 805027d89163a6ee4ff01444b859ced1 | fa6dddb6f8ceea6d8cc2cb38cf016ef9
1.0.6.76 | 3.2.5   | no | ? | 48 | a47e0658093fb80bda909bdb9779d4d8 | fa6dddb6f8ceea6d8cc2cb38cf016ef9
1.0.6.77 | 3.2.5.1 | no | ? | 48 | 1bfee3c8b6af9fe516fe49bb76648d5d | fa6dddb6f8ceea6d8cc2cb38cf016ef9
1.0.6.79 | 3.2.5.2 | no | ? | 48 | a1996fb6a2bde314b694aba327e63b03 | fa6dddb6f8ceea6d8cc2cb38cf016ef9
1.0.6.91 | 3.2.7.1 | no | ? | 51 | e2795b1a9772d4b97b567e59575826c0 | 2de86e337c2d20c9fb7ab8660dc2e4f1


### 1.0.7 series

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.0.7.03 | 3.2.7.2  | no | ? | 53 | 692e63855d91e1eb531cc66f28094edf | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.08 | 3.2.7    | no | ? | 53 | fb77aad4c1078b6b9045cbe4af4a8700 | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.23 | 3.2.8.1  | no | ? | 53 | 039d3d758a5562c72e8d43bddead8132 | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.25 | 3.3.0.1  | no | ? | 53 | 8f43b6bb13ccef887ea3ad65aac434ca | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.29 | 3.3.0.2  | no | ? | 53 | 4bcbffbdf8e20886e6c9a9cb51c6a388 | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.35 | 3.3.2.1  | no | ? | 53 | ebc94645be170c41ebbc93d8859c9d05 | 074a12cb87acb7b83ec70af603f1e9c3
1.0.7.43 | 3.3.2.2  | no | ? | 54 | cc1ea0a7dbf9bc2bc78ac74ceee33663 | 5d164d87fc84de462669fe5d98e43896
1.0.7.52 | 3.3.1    | no | ? | 55 | 661fa80295611a49e6bf7e1038bce0d1 | aea4c56d1ec22565ffad1383828128c6
1.0.7.53 | 3.3.4.1  | no | ? | 55 | b8623a3937c14b1b00f285498b6f0950 | aea4c56d1ec22565ffad1383828128c6
1.0.7.57 | 3.3.4.6  | no | ? | 55 | 9ddf349968d3bd9199aef88fecf91636 | aea4c56d1ec22565ffad1383828128c6
1.0.7.71 | 3.3.4.9  | no | ? | 55 | 932c5c8224542d9f431156e3956550f4 | aea4c56d1ec22565ffad1383828128c6
1.0.7.77 | 3.3.4.10 | no | ? | 56 | d3e632c1f4e05db9550b78abf7d86072 | 46349cac19c06e5848f88c041c84f5a0
1.0.7.81 | 3.3.4.11 | no | ? | 56 | 6fef26395a92b6803ed932c1b5ba1f81 | 46349cac19c06e5848f88c041c84f5a0
1.0.7.88 | 3.3.2    | no | ? | 56 | 23a06a60446572f6870e585fd303e4d2 | 46349cac19c06e5848f88c041c84f5a0




[1]: flash tested on lg g5 and worked correctly GB:???
[2]: flash tested on lg g5 and worked correctly GB:0.2.2.4 
