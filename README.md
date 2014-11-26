s5-lollipop
===========

How to install cyanogenmod, android l and root the Samsung Galaxy S5

#### Wipe user data and cache
* Boot into recovery
* Wipe user data
* Wipe cache partition

#### Flash custom recovery

* Get [cwm-swipe.img](http://forum.xda-developers.com/devdb/project/dl/?id=5088&task=get)
* Install ADB ( You can find various tutorials on how to do this by doing a google search)
* Push cwm-swipe.img to device and flash recovery
  * `adb push cwm-swipe.img /data/local/tmp/recovery.img`
  * `adb shell su -c dd if=/data/local/tmp/recovery.img of=/dev/block/platform/msm_sdcc.1/by-name/recovery`

#### Flash custom ROM and Gapps
* Get ROM and gapps from [XDA-Developers](http://forum.xda-developers.com/galaxy-s5/unified-development/rom-cyanogenmod-12-0-android-5-0-t2945538)
* Boot into recovery
  * `adb reboot recovery`
* Choose install from zip
* Choose install from adb
  * `adb sideload <path_to_zip>.zip`
* Reboot into recovery again
* Choose install from zip and install from adb
  * `adb sideload <path_to_gapps_zip>.zip`
* Reboot

#### Install SuperSU
* After startup, reboot into recovery
* Choose install from zip and install from adb
  * `adb sideload <path_to_supersu_zip>.zip`
* Reboot, and after startup, start SuperSU

### Verify root
* Download Root Checker from Play Store
* Grant access to Root Checker on SuperSU prompt
* Press Verify root and check if root succeeded
* And you are done!

#### Known issues
* Failed to mount when installing ROM
  * Just reboot, it is installed
