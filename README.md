This are the sources of kernel 2.6.32.9 for zte racer phones, is based on 
v4mshi repo at: https://github.com/V4MSHI/zte_racer_2.6.32, msm_ts.c
was missing from that repo and also the correct config file, both and 
other changes were added in this repo.

This sources should allow you to correctly compile a kernel that boots,
everything works (there are some issues with compass on android 2.3 roms) 
and calibration needs rework.

To compile:

make ARCH=arm CROSS_COMPILE=$YOUR_ARM_EABI_CC msm7627_zte_mooncake_defconfig

make ARCH=arm CROSS_COMPILE=$YOUR_ARM_EABI_CC -j`grep 'processor' /proc/cpuinfo|wc -l`
