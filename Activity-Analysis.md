## Raw data

Gadgetbridge currently stores raw data in its database. Raw data has to be read as "data as sent by the device": what kind of processing is done within each device is beyond our knowledge.

Actigraphy even with pulse oximetry has very limited ability to accurately Eg r = 0.15 for a more elaborate device than any supported by Gadgetbridge vs in lab sleep study (Penzel, Kesper,  Pinnow, Becker, & Vogelmeier, 2004). Though better in this systematic analysis (Yalamanchali, Farajian, Hamilton, Pott, Samuelson, & Friedman, 2013).

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

The firmware supports 3 different modes to measure the heart rate:
* a single measurement (as initiated from the debug screen)
* automatic measurement during sleep
* continuous measurement, about one per second (as used in the live activity tracking screen)

Only the measurement during sleep is recorded on the band. The other measurement values are sent to the mobile only, so you have to be connected to get them. Maybe there are other ways to get the heart rate data recorded but we don't know them.

### Miband 2 (with display, button, HR sensor)

Besides the display it basically provides the same functionality as Miband 1s in Gadgetbridge (including original Miband functionality).

### Pebble health

* Data is aggregated per minute
 * the timestamp is rounded to the minute
* Usually fifteen minutes are sent with a single transfer
 * Multiple sets (each 15 minutes long) are aggregated in a single transfer, especially
* Activity and sleep information use separate message
 * Currently the sleep start/end time are applied over a previously received time range by Gadgetbridge
 * See https://github.com/Freeyourgadget/Gadgetbridge/wiki/Pebble-datalog for further details

## Sources

Ainsworth, B. E., Haskell, W. L., Whitt, M. C., Irwin, M. L., Swartz, A. M., Strath, S. J., O'brien, W. L., Bassett, D. R., Jr., Schmitz, K. H., Emplaincourt, P. O., Jacobs, D. R. Jr., & Leon, A. S. (2000, September). Compendium of physical activities: An update of activity codes and MET intensities. Medicine & Science in Sports & Exercise, 32, 498-516. doi:10.1097/00005768-200009001-00009. Retrieved from http://www.juststand.org/portals/3/literature/compendium-of-physical-activities.pdf 

Bao L., & Intille S. S. (2004). Activity Recognition from User-Annotated Acceleration Data. In Ferscha, A., & Mattern, F. (Eds.), Pervasive Computing: Second International Conference, PERVASIVE 2004, Vienna Austria, April 21-23, 2004, Proceedings (1-17). Berlin-Heidelberg, Germany: Springer-Verlag. doi: 10.1007/978-3-540-24646-6_1. Retrieved from http://robotics.usc.edu/~gaurav/CS546/readings/bao_pc2004.pdf 
 
Fitbit Blog. Retrieved from Fitbit blog: https://blog.fitbit.com/246/ [blogs URL’s use sentences instead of a number; link broken]

Penzel, T., Kesper, K., Pinnow, I., Becker, H. F., & Vogelmeier, C. (2004, August). Peripheral arterial tonometry, oximetry and actigraphy for ambulatory recording of sleep apnea. Physiological measures, 25(4), 1025-1036. doi:10.1088/0967-3334/25/4/019. Retrieved from https://www.ncbi.nlm.nih.gov/pubmed/15382839 

van Hees T. V., & Ekelund, U. (2009, September 1). Novel daily energy expenditure estimation by using objective activity type classification: where do we go from here? Journal of Applied Physiology, 107(3), 639-640. doi:10.1152/japplphysiol.00793.2009. Retrieved from http://jap.physiology.org/content/107/3/639.full.pdf%2Bhtml  

Yalamanchali, S., Farajian, V., Hamilton, C., Pott, T. R., Samuelson, C. G., & Friedman, M. (2013, December 1). Diagnosis of obstructive sleep apnea by peripheral arterial tonometry. JAMA Otolaryngology - Head & Neck Surgery, 139(12), 1343-1350. doi:10.1001/jamaoto.2013.5338. Retrieved from https://www.ncbi.nlm.nih.gov/pubmed/24158564 

