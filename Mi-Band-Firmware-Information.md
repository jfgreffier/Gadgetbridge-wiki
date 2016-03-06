This page contains remarks about the different Mi Band firmware version tested with Gadgetbridge. If you are using Gadgetbridge with a firmware version that is not listed here – or find that the information provided here are not correct – please provide your impressions and remarks to the team!

# Firmware 1.0.9.*

## 1.0.9.3 (Mi Band 1, coloured LEDs)
* __activity recognition__: works well, but it doesn't seems to recognize any sleep outside of "night hours".
* __connection__: no remarks
* __battery life__: no remarks

## 1.0.9.14
* __activity recognition__: no remarks
* __connection__: the bluetooth connection seems to be problematic after some time
* __battery life__: no remarks

## 1.0.9.27
* __activity recognition__: the sleep detection seems a bit off: a low activity level after 21:00 is often reported as light sleep
* __connection__: the bluetooth connection seems to be problematic after some time
* __battery life__: no remarks

## 1.0.9.48
* __activity recognition__: seems to be working well, there are many false positives regarding the band not worn state: in some cases the band is recognized as not worn even if it is.
* __connection__: bluetooth range seems better compared to other version
* __battery life__: no remarks

# Firmware 1.0.10.*

## 1.0.10.3 (Mi Band 1, coloured LEDs)
* __activity recognition__: no remarks
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779779

## 1.0.10.6
* __activity recognition__: no remarks
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779782

## 1.0.10.11
* __activity recognition__: seems to be working well, the "band not worn" detection looks good
* __connection__: no remarks
* __battery life__: no remarks
* __gadgedbridge fw installer nr.__: 16779787

## 1.0.10.14
* __activity recognition__: no remarks
* __connection__: Connecting and synchronizing seems to be slightly faster and more reliable than with previous firmware versions. However, for notifications the vibration feature does not work with Gadgetbridge versions prior to 0.6.2.
* __battery life__: no remarks
* __gadgetbridge fw installer nr.__: 16779790

# Firmware 4.19 (Mi Band 1S)


## 4.15.11.19
* __alarms__: ?
* __notifications__: work
* __activity recognition__: does not work (likely due to change of data format for transmitting heart rate sensor data.)
* __connection__: works
* __battery life__: ?
* __gadgetbridge fw installer nr.__: ?

# Firmware 5.15.* (Mi Band 1A with white LEDs)
## Recommended version: 5.15.7.14 (see below)

## From 5.15.7.29 upwards, notifications do not work well, or at all

## 5.15.11.19
* __alarms__: mostly works (randomly fails)
* __notifications__: mostly works (randomly fails)
* __activity recognition__: works
* __connection__: works
* __battery life__: good
* __sleep detection__: doesn't work (band recognises sleep but not wake-up)
* lift and twist wrist to check activity goal progress through LEDs: doesn't work
* __gadgetbridge fw installer nr.__: ?

## 5.15.7.14 (recommended for Mi 1A) (MiFit 1.5.912-1539)
* __alarms__: work
* __notifications__: work
* __activity recognition__: works
* __connection__: works
* __battery life__: good
* __gadgetbridge fw installer nr.__: 84870926

## 5.15.7.2
* __alarms__: do not work
* __activity recognition__: ?
* __connection__: ?
* __battery life__: ?
* __gadgetbridge fw installer nr.__: ?

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