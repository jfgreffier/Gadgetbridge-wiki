The information present in this page is the result of reverse engineering the communication with the device. Not all messages are fully understood and some may be wrong. If you have more information, feel free to add it.

__This article is work in progress__

# Device operation logic

These smart watches operate in a autonomous way without requiring permanent connection to another device (e.g, smartphone). Once configured, they will operate accordingly. Some devices, such as the Makibes F68 provide a screen that can be used to configure their operation. Others will rely on a configuration provided by a host device.

Configuration is achieved by sending specific messages. There is no feedback and it is not possible to obtain the configuration. 

Values are sent in sets of 8bits. Values with more than 8bits must be split into multiple bytes in a specific manner.

Internally they have by a circular buffer with 144 slots, each representing 10 minutes of operation. It is possible to query

## Messages sent to the device

### Set Date

Sets the year, month and day.

Message format: `[0x08, Y0, Y1, Month, Day]`

Arguments:
* Y0: Year / 256
* Y1: Year % 256
* Month: Number of the month, from 1 to 12
* Day: Day of the month

### Set Time

Sets the current time.

Message format: `[0x09, Hour, Minute, Second]`

Arguments:
* Hour: Hour of the day, from 0 to 23
* Minute: Minutes of the hour, from 0 to 59
* Second: Seconds of the minute, from 0 to 59

### Set Day of the Week

Sets the day of the week to be presented (e.g, Sunday, Monday...)

Message format: `[0x2A, DayNumber]`

Arguments:
* DayNumber: Number of the day of the week, Sunday is 0


### Set All Day Heart Rate Measurement
Sets periodic monitoring of heart rate with an interval yet to be determined.

Message format: `[0x35, ARG]`

Arguments:
* ARG: Monitoring On: `0x0A`, Monitoring Off: `0xFF`

_Not sure how other values influence the monitoring period_

### Set Inactivity Timers
Sets an inactivity timer.

Message format: `[0x0A, H1, M1, H2, M2]`

Arguments:
* H1: Start Hour
* M1: Start Minute
* H2: End Hour
* M2: End Minute

_Operation was not tested_ Needs testing 

## Messages provided by the device

### Current Stats
Enabling All Day Heart Rate Measurement will make the device send periodic messages with current Calories, Steps, Heart Rate, Active Time, and Battery. 

These messages are sent whenever movement is detected even if there are no changes. Expect duplicated messages. 

Message format: `[0x33, S0, S1, D0, D1, C0, C1, C2, C3, B, Unknown, HR, A0, A1]`

Information Fields:
* Steps (number): `S1 * 256 + S0`
* Distance (meters): `D1 * 256 + D0`
* Calories (kCal): `C1 * 256 + C3 * 256 + C2 + C0`
* Battery: B ranging from 0 to 100
* HeartRate: HR in Beats Per Minute. 0 if measurement failed (not in wrist). 255 is measuring
* ActiveTime (minutes): `A1 * 256 + A0`

### Day Summary Data

These messages are sent if requested, providing a summary of the day. The device will store an unknown number of days. When requested, it will provide all days stored in the memory.

It is unknown why the device may report two different IDs for these messages.

Message format : `[0x38 or 0x39,  S0, S1, D0, D1, C0, C1, C2, C3, Y0, Y1, Month, Day, A0, A1, MaxHR, MinHR]`

Information Fields:
* Steps (number): `S1 * 256 + S0`
* Distance (meters): `D1 * 256 + D0`
* Calories (kCal): `C1 * 256 + C3 * 256 + C2 + C0`
* Year: `Y1 * 256 + Y0`. Year of the measurement
* Month: month of the measurement
* Day: day of the measurement
* ActiveTime (minutes): `A1 * 256 + A0`
* MaxHR: Maximum Heart Rate during the day
* MinHR: Minimum Heart Rate during the day

### SW Version

Message sent by the device if requested, proving the current software version.
There are two different formats:

Message format 1: `[0x18, Minor, Major]`

Message format 2: `[0x2E, 0, 0, 0, 0, 0, 0, 0, 0, Minor, Major]`

Information Fields:
* Minor: Minor Software Version
* Major: Major Software Version