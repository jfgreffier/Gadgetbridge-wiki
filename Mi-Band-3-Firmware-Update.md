## CAUTION
This feature **has the potential to brick your Mi Band 3**! We never tested it personally but according to at least one tester it works in the master branch (not yet released) **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

## Choosing the right firmware version for your Model

Device Name | HW Revisions | needed files
------------|--------------|------------
Mi Band 3   | V0.18.3.4    | Mili_wuhan.fw, Mili_wuhan.res

## Installing the firmware
Copy the desired Mi Band 3 .fw and .res files to your Android device and open the .fw file from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process. Repeat with the .res file (you don't have to do this if the previous version you
flashed had exactly the same .res version)

## Known Firmware Versions

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

### 1.1.0 series (adds a lot of languages)

fw ver   | MiFit ver | tested | known&nbsp;issues | res ver | fw-md5 | res-md5 
---------|-----------|--------|-------------------|---------|--------|---------
1.1.0.14 | 3.4.1     | no | ? | 33 | 95cacbb55b73cba072be60da649b8964 | 57d2724c4d9b7af6f52ba07007c36251
