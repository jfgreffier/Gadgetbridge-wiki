The information present in this page is the result of reverse engineering the communication with the device. Not all messages are fully understood and some may be wrong. If you have more information, feel free to add it.

__This article is work in progress__

### Device operation logic

These smart watches operate in a autonomous way without requiring permanent connection to another device (e.g, smartphone). Once configured, they will operate accordingly. Some devices, such as the Makibes F68 provide a screen that can be used to configure their operation. Others will rely on a configuration provided by a host device.

Configuration is achieved by sending specific messages. There is no feedback and it is not possible to obtain the configuration. 

Values are sent in sets of 8bits. Values with more than 8bits must be split into multiple bytes in a specific manner.

#### All Day Heart Rate Measurement
Sets periodic monitoring of heart rate with an interval yet to be determined.

Message format: [0x35, ARG]
ARG values:
* Monitoring On: 0x0A
* Monitoring Off: 0xFF


Internally they are composed by a circular buffer with 144 slots, each representing 10 minutes of operation. It is possible to query

## Messages provided by the device

### Current Stats
Enabling All Day Heart Rate Measurement will make the device send periodic messages with current Calories, Steps, Heart Rate, Active Time, and Battery.

Message format: [0x33, Steps0, Steps1, Distance0, Distance1, Calories0, Calories1, Calories2, Calories3, Battery, Unknown, HeartRate, Active0, Active1]
Fields:
* Steps (number): Steps1 * 256 + Steps0
* Distance (meters): Distance1 * 256 + Distance0
* Calories (kCal): Calories1 * 256 + Calories3*256 + Calories1 + Calories0
* Battery: 0-100
* HeartRate: in Beats Per Minute. 0 if measurement failed (not in wrist). 255 is measuring
* ActiveTime (minutes): Active1 * 256 + Active0
  
