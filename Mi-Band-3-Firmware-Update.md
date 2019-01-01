## CAUTION
This feature **has the potential to brick your Mi Band 3. You are doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

## Choosing the right firmware version for your Model

Device Name           | HW Revisions | needed files
----------------------|--------------|------------
Mi Band 3             | V0.18.3.2 V0.18.3.4 V0.18.3.6 V0.18.4.1 V0.18.4.3 | Mili_wuhan.fw, Mili_wuhan.res
Mi Band 3 (with NFC)  | V0.20.131.33   | Mili_chongqing.fw Mili_chongqing.res

Note: After flashing some firmware versions the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again. Do this if you have problems connecting after a firmware update, you wont lose any data. After that continue with flashing the .res file.

## Installing the firmware
Copy the desired Mi Band 3 .fw and .res files to your Android device and open the .fw file from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process. Repeat with the .res file (you don't have to do this if the previous version you
flashed had exactly the same .res version).   
If you get the error "Element cannot be installed" or "The file format is not supported" try a different file manager. [Amaze](https://f-droid.org/en/packages/com.amaze.filemanager/) should work.

## About Languages and fonts
There are two font files for the Mi Band 3, Mili_wuhan.ft (the normal, pre-installed one) and Mili_wuhan.ft.kj which is only for Japanese and Korean (So far ONLY supported in Firmware 1.3.0.8, not 1.4.0.6). The language set in Gadgetbridge has to match the font file (.ft.kj file for Japanese and Korean, .ft file for everything else) - else the menu text is blank and the Mi Band will ask you to update if you reconnect, which means you have to install the matching font file. Also language switching will change the available characters, even if they share the same font. For example switching to German will enable ä,ö,ü but disable all Chinese characters.

## Known Firmware Versions (Mi Band 3 without NFC)

### 0.0.0 series (Alpha, not recommened to try)

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
0.0.0.8  | 3.2.0.1   | no | ? | 3  | ca4907e6ad5f5714d0cdfc834c27dc23 | 6fda92d7beaaa5a90b756836f72e1093
0.0.0.9  | 3.2.2     | no | ? | 4  | 9b22823e032a0e686c9d67c4bad4dcbe | 7031b4b74a860beb0d0d8734c2ee6588
0.0.0.15 | 3.2.2.2   | no | ? | 8  | 52bafd7161d82fc384e4d6a637552528 | 78f93c3ad65cdc9fdb6f729356b66343
0.0.0.21 | 3.2.2.3   | no | ? | 10 | 6334ceaa9444a343867328ff3d6fb8a3 | 83ab66ca9ea6a32a0eda9aacca5e680a
0.0.0.29 | 3.2.3.1   | no | ? | 12 | ff796309ee758057b1f5ddc8407844f6 | a4b1a11252f5c79a024fed213bbb60b0
0.0.0.30 | 3.2.5     | no | ? | 12 | 7b01597a7d72d5c5ad576c2bf726a3e4 | a4b1a11252f5c79a024fed213bbb60b0
0.0.0.35 | 3.2.5.1   | no | ? | 13 | 18756050d6397c094d03e383a7124a49 | 83ed6c31cd0e7f972501dd554dfcff70
0.0.0.36 | 3.2.5.2   | no | ? | 14 | 2e73191d3af03919cee13f53639b3600 | 5d75abcc8f92e9d2d6cb9fd2d58dfe5d
0.0.0.40 | 3.2.7.1   | no | ? | 16 | 71c90b194f474449be7660f3dbea6830 | 32562a63766697f777f7dcc1dc1e11f7
0.0.0.42 | 3.2.7     | no | ? | 17 | c420a69d6387965f7ad148d31ca33c9f | cf92efd216110269bae8cf60617e18de
0.0.0.48 | 3.2.8.1   | no | ? | 17 | b7118f5438aa710856776c140a85cf9d | cf92efd216110269bae8cf60617e18de
0.0.0.54 | 3.3.0.1   | no | ? | 19 | 7cbd641f472045ef84795a81342663ac | a8e069f81e95809ce91e962ec2efb486
0.0.0.55 | 3.0.0.2   | no | ? | 19 | cdab230ce94d7f74c7ef1e3d1e15040a | a8e069f81e95809ce91e962ec2efb486
0.0.0.65 | 3.3.2.1   | no | ? | 23 | ce1400be96226e68ecdbc0ff3c675fde | a0febd689fa05616807665cb25851903

### 1.0.1 series (Probably beta, not recommended to flash, device name is still "Wuhan")

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.0.1.0  | 3.3.2.1   | no | ? | 26 | 7b4e6d52f9f2aca67482e58b96058ac5 | 0957a421d54f6aeae0dbe11f80090c34
1.0.1.5  | 3.3.1     | no | ? | 27 | 40eace0caab14b83ce89c78f4ee108bf | 9becdd15814462c050249d216321330a
1.0.1.10 | 3.3.4.1   | no | ? | 28 | 79a737a3a6cdce9bd09aeeb060559092 | 03c9edeb32186c775464bf25aa06aea6
1.0.1.17 | 3.3.2     | no | ? | 28 | 959a3938131558c31e2ce5706e6c8fa5 | 03c9edeb32186c775464bf25aa06aea6
1.0.1.50 | 3.3.6     | no | ? | 29 | 92a3541414faf7338bc2b119e6c655f8 | fd7e7236d1cd4380b433876802a23f37

### >1.1.0 series 

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.1.0.14 | 3.4.1     | no  | ? | 33 | 95cacbb55b73cba072be60da649b8964 | 57d2724c4d9b7af6f52ba07007c36251
1.2.0.8  | 3.4.4.1   | no  | ? | 34 | d5fdd509d40c0a3a65bb2b01efdb9475 | 0787aede985e4c3b3a08f30f41c4da89
1.3.0.4  | 3.4.4     | no  | ? | 35 | 28a5d5b8d858ed1fb9c2e982d6d451f1 | 108869297b7d33a7fcd4c9dc3bb7eae5
1.3.0.8  | 3.4.6.8   | yes | ? | 37 | bfb6f624ac30288b06fbfe1874b59bf6 | 6aff668df38678a4f99308a103f3d96c
1.4.0.6  | 3.4.5     | no  | ? | 37 | 185de410470ad4af118cbbe47fc99023 | 6aff668df38678a4f99308a103f3d96c
1.4.0.12 | 3.4.6.6   | no  | ? | 40 | b88a78645b6ceba7f352c70471018e67 | 36019608bbe73ba09acf15c4dc1d9a09
1.5.0.2  | 3.4.6     | yes  | ? | 40 | d35b91d0e1c33edfbc128412b285159d | 36019608bbe73ba09acf15c4dc1d9a09
1.5.0.7  | 3.4.7.10  | no  | ? | 40 | e25aa35f47df6a5d256e158c1fd5e7e1 | 36019608bbe73ba09acf15c4dc1d9a09
1.5.0.11 | 3.4.7.27  | no  | ? | 40 | 4013ff5318f2f5be99a64a71f00acb4c | 36019608bbe73ba09acf15c4dc1d9a09
1.6.0.16 | 3.4.7     | no  | ? | 40 | efa49a6d1e0e48add3099d4e819874b6 | 36019608bbe73ba09acf15c4dc1d9a09
1.8.0.0  | 3.5.2     | yes  | ? | 42 | 7dd4b563f47584d923729e07165ecba2 | 8b6394b18f81c25ad9c5b5c10a027b01
2.0.0.4  | 3.5.3     | yes  | ? | 44 | d3c210c3fde4f02da8a012bd78875756 | 0dfb4d6a39c7d3651c7a5c26dd45846c
2.2.0.12 | 3.5.5.3   | yes  | ? | 46 | c0e8a785f58b31b83d8b9dd9686ef73a | 36639114613677305ccc935234d09ea8
2.2.0.14 | 3.5.5     | yes  | ? | 46 | b9365c294b1d54f852e6d44a57c86456 | 36639114613677305ccc935234d09ea8
2.2.0.14 | 3.5.6     | yes  | ? | 46 | b9365c294b1d54f852e6d44a57c86456 | 36639114613677305ccc935234d09ea8

## Known Firmware Versions (Mi Band 3 with NFC)

### 0.0.0 series (Alpha, not recommened to try)

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
0.0.0.31 | 3.4.0.1   | no | ? | 32 | ef39594666b06badee7889e956b872fd | fcd43383c85180380ee7bcd908cfd574
0.0.0.47 | 3.4.2     | no | ? | 33 | 04dbb9ecba849cbb4a2690c5497745f7 | 57d2724c4d9b7af6f52ba07007c36251

### >1.0.0 series
fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.0.0.3  | 3.4.4.1   | no | ? | 34 | 22c116ed6112ccc0360dbe693da7c6a2 | 0787aede985e4c3b3a08f30f41c4da89
1.1.0.20 | 3.4.6.8   | no | ? | 37 | c6a8a78e9a71e3fe184ad6e032ea060d | 6aff668df38678a4f99308a103f3d96c
1.1.0.4  | 3.4.3     | no | ? | 34 | a6073b0e3806191f033997a2231bcb1f | 0787aede985e4c3b3a08f30f41c4da89
1.2.0.0  | 3.4.6.6   | no | ? | 40 | 0a4b4a2167713605666842ca6a0e959e | 36019608bbe73ba09acf15c4dc1d9a09
1.2.0.2  | 3.4.7.2   | no | ? | 40 | 017d8c919ca6fc31da55e3e09196d091 | 36019608bbe73ba09acf15c4dc1d9a09
1.2.0.26 | 3.4.7     | no | ? | 40 | 9c44dc42acaac35f882e08d35d57702d | 36019608bbe73ba09acf15c4dc1d9a09
1.2.0.30 | 3.5.0     | no | ? | 40 | 28ae6347c526d9ce07f404427d34b7b7 | 36019608bbe73ba09acf15c4dc1d9a09
1.2.0.8  | 3.4.7.58  | no | ? | 40 | 0e285b28cb6abde8bfc24c800c7171e2 | 36019608bbe73ba09acf15c4dc1d9a09
1.3.0.0  | 3.5.2     | no | ? | 42 | 69567576eec1338584d469830c8e8a28 | 8b6394b18f81c25ad9c5b5c10a027b01
1.3.0.3  | 3.5.2.2   | no | ? | 43 | 5e8d086cd35de2e26d2629485c20cb47 | 8e471c4a0610788cc4bce9c9bb1825a3
1.4.0.2  | 3.5.3.1   | no | ? | 44 | 857ea0786a76a1c44c962fc418d35bfa | 0dfb4d6a39c7d3651c7a5c26dd45846c
1.4.0.4  | 3.5.3     | no | ? | 44 | b79dc37bc482a3c292ff05a9dcca68d3 | 0dfb4d6a39c7d3651c7a5c26dd45846c
1.5.0.2  | 3.5.4     | no | ? | 44 | 950c505a783824ae921ff95cc8114543 | 0dfb4d6a39c7d3651c7a5c26dd45846c
1.6.0.6  | 3.5.5.3   | no | ? | 46 | 2849fd65e08c02a57d11fa4971162cc9 | 36639114613677305ccc935234d09ea8
1.6.0.10  | 3.5.5.4   | no | ? | 46 | b8ac10f8a76bc3d396cfd09e7f3cd69d | 36639114613677305ccc935234d09ea8
1.6.0.10  | 3.5.6   | no | ? | 46 | b8ac10f8a76bc3d396cfd09e7f3cd69d | 36639114613677305ccc935234d09ea8