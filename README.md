This is a set of projects and a template to enable the compilation of
stm32cubefx generated projects with a standard gnu arm toolchain.

At the top level is a python tool to generate makefile fragments from the
stm32cube gpdsc files (generated by configure cubemx projects to output gpdsc).
This python tool requires the "untangle" library.

To use, modify the top level make file fragment gpdsc.mk TOOLCHAIN variable
point to an appropriate gcc arm toolchain
(https://launchpad.net/gcc-arm-embedded)

Each of the projects can be built by entering the appropriate subdirectory and
invoking make.

There are a few tools generated (e.g. tee in the vcom project) that may be of
help in testing.  The projects are

 1. PushButton -- lights an LED when the blue user button is pressed
 2. vcom       -- creates a USB virtual com port loopback
 3. ramfs      -- creates a USB mounted ram file system
 4. fatfs      -- mounts an SD card on SPI2
 5. sd         -- mounts an SD card on SPI2 over USB


