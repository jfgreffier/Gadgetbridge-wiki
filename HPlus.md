# Current Status

This applies both to the Zeblaze Zeband, Zeband Plus, Makibes F68, and many others, as they share most of the same protocol.

## Working
* Discovery and pairing
* Setting weight, height, age, date, time, day of week
* Synchronise activity data: all stored not all is displayed
* Notifications (Display + vibration) with differentiation between phone calls and messages
* Display firmware version and battery status
* "Real time" (10m) heart rate monitoring: the devices do not seem to provide true real time values.
* Sleep monitoring: individual sleep phases stored but not presented. Only light and deep is presented
* Calories and distance stored but not presented
* Real time steps
* Alarms
* Configuration of some specific settings: Language, Real time HR State, Goals, Screen time.

## Not working:
* Inactivity Alarms: Messages are known. Requires some more code.
* Configuration of some specific settings: (HR thresholds, Inactivity alarms, Enable/Disable SMS and Phone notifications in the device, Find Me)
* Swimming statistics: Needs tinkering with the devices as messages are unknown
* Activity only considers HR... So there is no activity charts if All Day HR monitoring is disabled.
* Firmware update: Standard Nordic DFU process. No code developed

## Development/work planned/ideas to be explored
* Find if there is a configurable HR monitoring interval
* Find how inactivity timers work
* Some messages are not understood and require further tinkering
* Temporarily enable All Day HR Monitoring, for 1-2 seconds, in order to get latest data from band. This would be a simple synchronization method for steps, distance and calories.


# For Developers

[[HPlus Protocol]]