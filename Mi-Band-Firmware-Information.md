This page contains remarks about the different Mi Band firmware version tested with Gadgetbridge. If you are using Gadgetbridge with a firmware version that is not listed here – or find that the information provided here are not correct – please provide your impressions and remarks to the team!

The firmwares are sorted by device. The recommended version comes first, then other versions sorted from newer to older.

<!--
Template for each firmware:
## 1.0.
* __alarms__:
* __notifications__:
* __activity recognition__: 
* __connection__: 
* __battery life__: 
* __gadgetbridge fw installer nr.__: 

-->

# Mi Band 1S (Firmware 4.x)
## 4.15.12.10 Mi Band Firmware + 1.3.74.76 HR Firmware (recommended)
* __alarms__: work
* __notifications__: work
* __activity recognition__: works
* __connection__: works
* __battery life__: good
* __heart rate measurement__: works
* __gadgetbridge fw installer nr.: 68094986


## 4.15.11.19 Mi Band Firmware + correspeonding Heart Rate Firmware
* __alarms__: do not work
* __notifications__: work
* __activity recognition__: unusable, detects far too many sleep hours
* __connection__: works
* __battery life__: good
* __gadgetbridge fw installer nr.__: ?
* __heart rate measurement__: does not work


# Mi Band 1A (with white LEDs, no heartrate sensor)
## 5.15.7.14 (recommended) (MiFit 1.5.912-1539)
* __alarms__: work
* __notifications__: work
* __activity recognition__: works
* __connection__: works
* __battery life__: good
* __gadgetbridge fw installer nr.__: 84870926

## From 5.15.7.29 upwards, notifications do not work well, or at all

## 5.15.11.19
* __alarms__: mostly works (randomly fails)
* __notifications__: mostly works (randomly fails)
* __activity recognition__: works
* __connection__: works
* __battery life__: good
* __sleep detection__: doesn't work (band recognises sleep but not wake-up)
* __lift and twist wrist to check activity goal progress through LEDs__: doesn't work
* __gadgetbridge fw installer nr.__: ?

## 5.15.7.2
* __alarms__: do not work
* __activity recognition__: ?
* __connection__: ?
* __battery life__: ?
* __gadgetbridge fw installer nr.__: ?

# Mi Band 1 (coloured LEDs)

## 1.0.10.14
* __activity recognition__: no remarks
* __connection__: Connecting and synchronizing seems to be slightly faster and more reliable than with previous firmware versions. However, for notifications the vibration feature does not work with Gadgetbridge versions prior to 0.6.2.
* __battery life__: no remarks
* __gadgetbridge fw installer nr.__: 16779790

## 1.0.10.11
* __activity recognition__: seems to be working well, the "band not worn" detection looks good
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779787

## 1.0.10.6
* __activity recognition__: no remarks
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779782

## 1.0.10.3
* __activity recognition__: no remarks
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779779

## 1.0.9.48
* __activity recognition__: seems to be working well, there are many false positives regarding the band not worn state: in some cases the band is recognized as not worn even if it is.
* __connection__: bluetooth range seems better compared to other version
* __battery life__: no remarks

## 1.0.9.27
* __activity recognition__: the sleep detection seems a bit off: a low activity level after 21:00 is often reported as light sleep
* __connection__: the bluetooth connection seems to be problematic after some time
* __battery life__: no remarks

## 1.0.9.14
* __activity recognition__: no remarks
* __connection__: the bluetooth connection seems to be problematic after some time
* __battery life__: no remarks

## 1.0.9.3 (Mi Band 1, coloured LEDs)
* __activity recognition__: works well, but it doesn't seems to recognize any sleep outside of "night hours".
* __connection__: no remarks
* __battery life__: no remarks
