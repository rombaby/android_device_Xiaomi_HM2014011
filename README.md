<<<<<<< HEAD
----Thanks for fire855 & superdragonpt, who are contributing to the working CyanogenMod of MTK hardware(MT6582&MT6592).---

This is a device tree for Xiaomi Redmi_1s_TD(HM2014011). Powered by ferhung.
# Build

* init
  Grab the CyanogenMOD source:

        # repo init -u git://github.com/fire855/android.git -b cm-12.1
        
        # repo sync

* full build
        
        # source build/envsetup.sh

        # brunch cm_HM2014011-eng

# Limitations

Services requires root:

`system/core/rootdir/init.rc`

  * surfaceflinger depends on sched_setscheduler calls, unable to change process priority from 'system' user (default user 'system')

  * mediaserver depends on /data/nvram folder access, unable to do voice calls from 'media' user (default user 'media')

# In China we can't get 204 from Google server
  * Android 5.1 source change to skip network validation in some environment like China can't connect to http://clients3.google.com/generate_204.
        # To see: https://github.com/ferhung/Skip_network_validation

=======
# android_device_Xiaomi_HM2014011
