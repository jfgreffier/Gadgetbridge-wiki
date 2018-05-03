Since version 0.26.0, Gadgetbridge added feature that allows to export the activities (workouts) recorded with the Amazfit Bip. All workout types are supported and for outside activities (like Walking, Running, Cycling, ...) that contain GPS data, a GPX file can be exported to your phone or shared with any android application. The GPX file also contains Heart Rate data, if it was recorded.

## Activity data synchronization 

In Gadgetbridge push the running man icon in the device card and then press the sync floating action button or swipe down. Please note that only one workout will be fetched, **you have to sync again to get the next activity and so on**, automatic fetching will be added in a later release.

![Main page icon](https://i.imgur.com/TuRakze.png)  

## Activities page

Tapping on an activity opens a GPS application to visualize and analyze data. Long press on an activity  to share the GPX file with other applications or to delete it.

![Activity page](https://i.imgur.com/zHI4G4E.png)

Exported GPX files can be found in `android/data/nodomain.freyourgadget.gadgetbridge/files` along with log files. The prefix is "gadgetbridge-track-" followed by the date/time

## Not supported features
Please be aware that not every detail of the workout is currently being stored in Gadgetbridge:
* "treadmill" activities are exported, but no data files is associated with them (no gps data)
* additional details of activities (calories count, pace, etc) are not included (you still can find them on the watch)