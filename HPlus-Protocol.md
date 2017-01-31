The information present in this page is the result of reverse engineering the communication with the device. Not all messages are fully understood and some may be wrong. If you have more information, feel free to add it.

__This article is work in progress__

### Device operation logic

These smart watches operate in a autonomous way without requiring permanent connection to another device (e.g, smartphone). Once configured, they will operate accordingly. Some devices, such as the Makibes F68 provide a screen that can be used to configure their operation. Others will rely on a configuration provided by a host device.

Configuration is achieved by sending specific messages. There is no feedback and it is not possible to obtain the configuration. 

Values are sent in sets of 8bits. Values with more than 8bits must be split into multiple bytes in a specific manner.

Internally they have by a circular buffer with 144 slots, each representing 10 minutes of operation. It is possible to query

#### All Day Heart Rate Measurement
Sets periodic monitoring of heart rate with an interval yet to be determined.

Message format: `[0x35, ARG]`

ARG values:
* Monitoring On: `0x0A`
* Monitoring Off: `0xFF`

_Not sure how other values influence the monitoring period_

## Messages provided by the device

### Current Stats
Enabling All Day Heart Rate Measurement will make the device send periodic messages with current Calories, Steps, Heart Rate, Active Time, and Battery. 

These messages are sent whenever movement is detected even if there are no changes. Expect duplicated messages. 

Message format: `[0x33, S0, S1, D0, D1, C0, C1, C2, C3, B, Unknown, HR, A0, A1]`

Fields:
* Steps (number): `S1 * 256 + S0`
* Distance (meters): `D1 * 256 + D0`
* Calories (kCal): `C1 * 256 + C3 * 256 + C1 + C0`
* Battery: B ranging from 0 to 100
* HeartRate: HR in Beats Per Minute. 0 if measurement failed (not in wrist). 255 is measuring
* ActiveTime (minutes): `A1 * 256 + A0`

### Day Summary

These messages are sent if requested, providing a summary of the day. The device will store an unknown number of days. When requested, it will provide all days stored in the memory.

It is unknown why the device may report two different IDs for these messages.

Message format : `[0x38 or 0x39,  S0, S1, D0, D1, C0, C1, C2, C3, Y0, Y1, Month, Day, A0, A1, MaxHR, MinHR]`

Fields:
* Steps (number): `S1 * 256 + S0`
* Distance (meters): `D1 * 256 + D0
* Calories (kCal): `C1 * 256 + C3 * 256 + C1 + C0`
* Year: `Y1 * 256 + Y0`. Year of the measurement
* Month: month of the measurement
* Day: day of the measurement
* ActiveTime (minutes): `A1 * 256 + A0`
* MaxHR: Maximum Heart Rate during the day
* MinHR: Minimum Heart Rate during the day

