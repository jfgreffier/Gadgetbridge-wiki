# Important foreword:
* The following text __almost certainly__ contains some errors.
* The information on this page are mostly deductions made by the developers by looking at bluetooth dumps while often risking to brick their devices, but would not be possible without the official SDK documentation and other projects' source code progress would be much slower.
* __Be grateful__ for the time and dedication of the people who decide to find out how things work and to document them for the general public.
* If you spot errors in this page, please __fix them__ and let us know! We will be grateful (see above :-) )
* Do not take the content of this page as "the Truth", it's just a bunch of hypotheses. You are the only person responsible for what you do with it. Remember that the following text __almost certainly__ contain errors.
* When this page states "probably" it usually means "this is how this value is used in Gadgetbridge".
* You are the __only__ person responsible for what you do with the information contained in this page!

Last but not least:
* Do not forget that you are the __only__ person responsible for what you do with the information contained in this page.

# Pebble Datalog

The pebble watch sends datalog packets at random intervals to its bluetooth peer whenever it is connected. This messages were previously acknowledged (ACKed) and discarded, because they contained no information that could be made use for. With the release of firmware 3.8 and the introduction of pebble Health, some of these messages were identified and decoded, and this page was born. __The general packet structure of bluetooth messages is not discussed here: this page focus on the Datalog-related part of the message.__ Please see the source code to understand how the whole message is structured.

## Datalog sessions

Pebble applications may send datalog messages, but must register/open a session beforehand. The session contains the information about:
* an id (assigned by the Pebble OS)
* the application UUID (NB: for system apps it's 0)
* a "tag" (chosen by the pebble app)
* the size of each item in the message (NB: a single datalog message *may* contain more items!)
* an "itemtype" (signed/unsigned integer or byte array)

After opening a session, further messages may be sent that contain the actual data to be transferred. These contain:
* an id (used to relate this message to the corresponding session)
* number of items left
* a CRC
* payload (datalog message content)

Of course watch apps may as well close the datalog sessions, using the aforementioned id.

# Pebble Health datalog - firmware version 3.10

Pebble Health - despite having its own UUID - sends the datalog message using UUID 0. Two distinct messages were identified, one for steps/activity data and one for sleep data, they may be identified thanks to the associated tag:
* Steps data has tag _81_; its item size is 99
* Sleep data has tag _83_; its item size is 18

## Steps data payload

The 99 bytes of the item contain some metadata and information about 15 minutes of activity, several packets are usually sent in one message when the watch wasn't connected for some time to Gadgetbridge; while connected, it was observed that each message contains only one packet and is sent every 15 minutes. Items may be concatenated within the same datalog message.

### Metadata

Metadata are contained at the beginning of each item. They are:
* __a short__ (two bytes) with fixed value of "5", probably the record version
* __an integer__ (four bytes) with a timestamp, probably the timestamp of the first record of this item
* __a byte__ with unknown meaning
* __a byte__ with the fixed value of "6", probably the length of each record
* __a byte__ with the fixed value of "F"(15), probably the number of records

### Record-data

Records follow the metadata and one another without any separator, the length of each record and the length may be used to point to a specific record. Further the timestamp must be incremented manually by knowing the index of the record of interest. Each record (of version "5", with length "6") contains the following information:
* __a byte__ with the steps count for the minute
* __a byte__ with unknown value, possibly the orientation for the minute (see [pebble docs](https://developer.pebble.com/docs/c/Foundation/Event_Service/HealthService/#HealthMinuteData) )
* __a short__ (two bytes) with probably the "vector magnitude count" (see [pebble docs](https://developer.pebble.com/docs/c/Foundation/Event_Service/HealthService/#HealthMinuteData) )
* __a byte__ with unknown value, __it may be that this byte and the next one are actually a short__
* __a byte__ with fixed value 0, __it may be that this byte and the next one are actually a short__

## Sleep data payload

The sleep data contain no metadata and information about (usually) one night of sleep. If during the night there were separate sleep sessions, they are reported as separate items. Items may be concatenated within the same datalog message. What is sent if the watch was not connected for more than one whole day has not been tested, but an educated guess is that more items will be used within the same datalog message. 

### Record-data

_In the case of sleep data an item contains a single record._ Its content are:
* __a short__ (two bytes) with fixed value 3600, probably the offset to UTC (because of the current season and the latitude of the developer)
* __an integer__ (four bytes) with a timestamp, probably the __first__ minute of "bed time"
* __an integer__ (four bytes) with a timestamp, probably the __last__ minute of "bed time"
* __a short__ (two bytes) with the number of seconds of deep sleep

# Pebble Health datalog - firmware version 3.11
A new message was introduced, identified by tag 84. It contains shallow and deep sleep data details.
The steps message (tag 81) was updated.
More details will follow.

# Pebble Health datalog - firmware version 3.12
The message with tag 84 was modified, further activity types were added, but they are still unknown. 
More details will follow.

# Pebble Health datalog - firmware version 3.12
No changes were detected so far.

# Analytics Datalog
All Pebble models before Firmware 3.8 already used three different datalog sessions coming from UUID 0 (tag ids 78,79 and 80). The original python libpebble suggested these were analytics and the Gadgetbridge developers also believe so. We will continue to discard these messages and no effort has been made to analyze the contents of these binary data packets.