## Raw data

Gadgetbridge currently stores raw data in its database. Raw data has to be read as "data as sent by the device": what kind of processing is done within each device is beyond our knowledge.

### Miband (original with colored leds)

* Data is aggregated per minute 
 * the timestamp sent by the miband may be any second of a given minute
 * when repeating a transfer (because the previous transmission was not ack'ed, for any reason) it may happen that the timestamp changes to a different second (within the same minute). This is currently an issue as multiple samples are being stored within gadgetbridge database for the same minute.
* Multiple minutes are sent with a single transfer
 * The amount of minutes within each chunk depends on the miband firmware, it's not predictable
 * It may span from some minutes to entire hours. The longer the period, the more likely the corruption of the data (as the only references are the beginning of each chunk).
* Each minute contains three values: number of steps, activity type, activity intensity
 * The known activity types are: "normal", "deep sleep", "shallow sleep", "device not worn"

### Miband 1a (white leds, no HR sensor)

### Miband 1s (white leds, HR sensor)

The firmware sports 3 different modes to measure the heart rate:
* a single measurement (as initiated from the debug screen)
* automatic measurement during sleep
* continuous measurement, about one peer second (as used in the live activity tracking screen)

Only the measurement during sleep is recorded on the band. The other measurement values are sent to the mobile only, so you have to be connected to get them. Maybe there are other ways to get the heart rate data recorded but we don't know them.

### Pebble health

* Data is aggregated per minute
 * the timestamp is rounded to the minute
* Usually fifteen minutes are sent with a single transfer
 * Multiple sets (each 15 minutes long) are aggregated in a single transfer, especially
* Activity and sleep information use separate message
 * Currently the sleep start/end time are applied over a previously received time range by Gadgetbridge
 * See https://github.com/Freeyourgadget/Gadgetbridge/wiki/Pebble-datalog for further details

## Sources
Ling Bao and Stephen S. Intille
Activity Recognition from User-Annotated
Acceleration Data
http://robotics.usc.edu/~gaurav/CS546/readings/bao_pc2004.pdf

Ainsworth BE, Haskell WL, Whitt MC, Irwin ML, Swartz AM, Strath
SJ, O’Brien WL, Bassett DR Jr, Schmitz KH, Emplaincourt PO,
Jacobs DR Jr, Leon AS.
Compendium of physical activities: an update of
activity codes and MET intensities.
http://www.juststand.org/portals/3/literature/compendium-of-physical-activities.pdf

Vincent T. van Hees, Ulf Ekelund 
Novel daily energy expenditure estimation by using objective activity type classification: where do we go from here?
http://jap.physiology.org/content/jap/107/3/639.full.pdf 


Fitbit blog: https://blog.fitbit.com/246/

Actigraphy even with pulse oximetry has very limited ability to accurately  Eg r = 0.15 for a more elaborate device than any supported by Gadgetbridge vs in lab sleep study:
https://www.ncbi.nlm.nih.gov/pubmed/15382839
Though better in this systematic analysis: 
JAMA Otolaryngol Head Neck Surg. 2013;139(12):1343-1350. doi:10.1001/jamaoto.2013.5338. pubmedID: 24158564 
