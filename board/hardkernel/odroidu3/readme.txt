Odroid U3 board with Samsung Exynos 4412 SoC

How to build it
===============

  $ make odroidu3_defconfig

Then you can edit the build options using

  $ make menuconfig

Compile all and build rootfs image:

  $ make

Note: you will need to have access to the network, since Buildroot will
download the packages' sources.

Result of the build
-------------------

After building, you should obtain all output files in output/images/


How to write the SD card or eMMC
================================

Once the build process is finished you will have an image called "sdcard.img"
in the output/images/ directory.

Copy the bootable "sdcard.img" onto an SD card or eMMC with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX

Insert the SDcard into your ODROID-U3, and power it up. Your new system
should come up now.

