## Mi Fit
It looks like it is not feasible to have both Mi Fit and Gadgetbridge installed at the same time. https://github.com/Freeyourgadget/Gadgetbridge/issues/330 suggests that Mi Fit restarts itself and automatically connects to your Mi device, preventing Gadgetbridge from functioning properly.

Maybe it is sufficient to deactivate Mi Fit instead of uninstalling it completely.

## Moto G (2013)
It looks like the Moto G, at least with Android 4.4.x (KitKat) has a problem with the Mi Band. It might be a problem with the Bluetooth stack of KitKat or even Moto G's Bluetooth device. 
Occurred with Mi Band firmware versions 
* 1.4.0.3 (everything in Gadgetbridge works **except** fetching activity data)
* 1.0.9.14 (nothing works, cannot even connect properly)
