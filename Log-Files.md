# Log File Location

If you enable Gadgetbridge's logging in the "Settings" screen (under "Developer Options"/"Write Log Files"), the log file will be stored on your external sdcard in `/sdcard/Android/data/nodomain.freeyourgadget.gadgetbridge/files/gadgetbridge.log`.

**Note**: Up to version 0.9.4, you needed to quit and restart Gadgetbridge to make the log setting work.

# Log File Contents

Please keep in mind Gadgetbridge log files may contain **lots of personal information**, including but not limited to health data, unique identifiers (such as a device MAC address), music preferences, etc. Consider editing the file and removing this information before sending the file to a public issue report.

When sharing a log file, please try to make it as short as possible. If you already had logging enabled, disable and reenable it before doing the things that you want to get logged. Disable logging when you're done with that. That way, we will not have to wade through huge log files looking for the actual relevant lines.

# Android's Bluetooth Logging (BT Snoop)

In order to capture the Bluetooth traffic, open Android's "Settings" -> "Developer options" and check "Enable Bluetooth HCI snoop log". Then perform the action that you want to capture. After doing that, uncheck the option again.

You will find the logfile at `/sdcard/btsnoop_hci.log`.

**Note**: On some devices/Android versions the Bluetooth snoop log might be stored in a different location (e.g. `/sdcard/Android/data/btsnoop_hci.log` for a Samsung Galaxy S5). If you cannot find the log file, you can find out the correct path with (ADB must be installed):

    adb shell cat /etc/bluetooth/bt_stack.conf | grep BtSnoop

See [here](https://stackoverflow.com/questions/28445552/bluetooth-hci-snoop-log-not-generated#30352487) for further details.
