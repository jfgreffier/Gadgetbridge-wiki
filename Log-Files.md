# Log File Location

If you enable Gadgetbridge's logging in the "Settings" screen (in "Developer Options"/"Write Log Files"), the log file will be stored on your external sdcard in `/sdcard/Android/data/nodomain.freeyourgadget.gadgetbridge/files/gadgetbridge.log`.

**Note**: Up to version 0.9.4, you needed to quit and restart Gadgetbridge to make the log setting work.

# Android's Bluetooth Logging (BT Snoop)

In order to capture the Bluetooth traffic, open Android's "Settings" -> "Developer options" and check "Enable Bluetooth HCI snoop log". Then perform the action that you want to capture. After doing that, uncheck the option again.

You will find the logfile at `/sdcard/btsnoop_hci.log`.

**Note**: On some devices/Android versions the Bluetooth snoop log might be stored in a different location (e.g. `/sdcard/Android/data/btsnoop_hci.log` for a Samsung Galaxy S5). If you cannot find the log file, you can find out the correct path with (ADB must be installed):

    adb shell cat /etc/bluetooth/bt_stack.conf | grep BtSnoop

See [here](https://stackoverflow.com/questions/28445552/bluetooth-hci-snoop-log-not-generated#30352487) for further details.
