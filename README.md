# TegraRcmSmash ![License](https://img.shields.io/badge/License-GPLv3-blue.svg)
A reimplementation of fusee-launcher in C++ for Windows platforms.
Lets you launch fusee payloads to a USB connected Switch in RCM mode.

## Driver setup
 1. Get your Switch into RCM mode and plug it into your Windows PC. It should show up somewhere (like Device manager) as "APX"
 2. Download and run Zadig driver installer from https://zadig.akeo.ie/
 3. From the device list, choose APX (if it's not showing up in the list, go to Options menu and check List All Devices)
 4. For the driver type, cycle the arrows until you see libusbK (v3.0.7.0) in the text box (IMPORTANT!)
 5. Click the big Install Driver button. Device manager should now show "APX" under libusbK USB Devices tree item.

## Usage
 TegraRcmSmash.exe [-V 0x0955] [-P 0x7321] [--relocator=intermezzo.bin] [-w] inputFilename.bin

## Binary releases
 Available at https://switchtools.sshnuke.net

## Compilation
 1. Download the binary package for libUSBK from https://sourceforge.net/projects/libusbk/ (by pressing the big green Download button)
 2. Run the installer exe and make note of where it installed to (default is C:\libusbK-dev-kit)
 3. Open your Advanced system settings and set the environment variable LIBUSBK_DIR to the path you noted
 4. Open TegraRcmSmash.sln with Visual Studio 2017 and build the Release or Debug configuration!

## Responsibility

**I am not responsible for anything, including dead switches, blown up PCs, loss of life, or total nuclear annihilation.**
