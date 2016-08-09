## Mi Fit
It looks like it is not feasible to have both Mi Fit and Gadgetbridge installed at the same time. https://github.com/Freeyourgadget/Gadgetbridge/issues/330 suggests that Mi Fit restarts itself and automatically connects to your Mi device, preventing Gadgetbridge from functioning properly.

Maybe it is sufficient to deactivate Mi Fit instead of uninstalling it completely.

## Moto G (2013)

The first gen Moto works fine with the Mi Band when updated to Android 5.1 (most should be), tested with Mi Band firmware 04.15.12.10. Everything seems to work.

Other versions like Android 4.4.x (KitKat) may have problems with the Mi Band - occurred with Mi Band firmware versions 
* 1.4.0.3 (everything in Gadgetbridge works **except** fetching activity data)
* 1.0.9.14 (nothing works, cannot even connect properly)

## Pebble 

1. Upgrade Pebble's firmware (tested 3.12.2), either with the official application or by flashing. 
2. Disable official Pebble app. 
3. Install F-Droid and Gadgetbridge. 
4. Connect to your Pebble by clicking your Pebble device. 

Pebble's official application complicates with Mi Fit. This work around enables to use both devices at the same time. Do software installation with the official Pebble app and do then (2-4)

Pebble: Pebble Classic hardware V3R3, ...    