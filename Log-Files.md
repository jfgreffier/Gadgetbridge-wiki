#Log File Location

If you enable logging in the "Debug" screen, the log file will be stored on your external sdcard in `/sdcard/Android/data/nodomain.freeyourgadget.gadgetbridge/files/gadgetbridge.log`

**Note**: up to version 0.9.4, you needed to quit and restart Gadgetbridge to make the log setting work.

# Bluetooth Logging (Btsnoop)

In order to capture the bluetooth traffic, open Android's Settings -> Developer Options and check "Enable Bluetooth HCI-Snoop-Protocol". Then perform the action that you want to capture. After doing that, uncheck the option again.

You will find the logfile at /sdcard/btsnoop_hci.log