# This is a collection of proposals, not a roadmap!


## Initial UI Proposal / brainstorming
* use a drawer in the main activity: in the drawer list show a list of currently known devices: in the main fragment the available action for the currently selected device (doesn't have to be necessarily connected)
 * the drawer could contain also a link to settings (to add new devices etc)
 * the main fragment could show big buttons (think two buttons per row) with graphic with all and only the actions that make sense for the selected device (sync, show activity data, set alarms, manage pebble apps...)
 * PROBLEM: what do we show to users that start GB for the first time / do not have any configured device?
* use a snackbar instead of the notifications when possible (e.g. syncronization progress)

## Further additions
* Drawer could contain all set up devices (each device has a set of sub-items) and an "Add device" button, as well as settings. 
* SOLUTION for the first time launch: A fragment that tells them they should add a device


* One annoyance with close devices is several require a paid subscriptions to get the raw activity data as a flat file to analyze yourself.  
 * proposed solution:  a button in activity tracker that allows exporting raw data as some easily read format (comma delimited, tab delimited etc).  Ideally an option to save to device or email the file.   


## Also see
* [More Intuitive User Interface](https://github.com/Freeyourgadget/Gadgetbridge/issues/301)
