Mobile Pentestration Testing and Ethical Hacking


EXP NO-1 — Browser-Based Android & ADB Essentials

Aim - To understand Android Debug Bridge (ADB) using WebADB and perform basic Android device enumeration, shell access, package management, activity management, and file-system navigation.

Description - This experiment demonstrates basic Android device interaction through a browser-based ADB interface. The practical includes connecting an authorized Android device, identifying the device using ADB, accessing the Android shell, inspecting installed packages, launching the Settings activity, and navigating the Android file system.


Exp No. 2 — Android Studio Installation and SDK Configuration

Aim - To install Android Studio and verify the Android SDK and required SDK tools for Android application development.

Tools -
Platform - Windows,
IDE	- Android Studio,
Android SDK	- Installed,
SDK Platform	- Android 17 (API 37),
Android Emulator	- Installed

Procedure -
1.	Installed Android Studio with the required Android SDK and emulator components.
2.	Opened Android SDK Manager and verified the installed SDK platform.
3.	Verified the required SDK tools including Build-Tools, Platform-Tools, Emulator, Command-line Tools, and Emulator Hypervisor Driver.
4.	Confirmed that the required SDK components were successfully installed and available.


Exp No. 3 – Android Architecture, Boot Process & Partition Layout

Aim - To examine the Android system architecture, boot-related information, mounted filesystems, and available block-device mappings of an Android emulator using ADB shell commands.

Procedure -
1.	Installed and configured Android Studio with the required Android SDK and emulator components. 
2.	Created and started a Pixel 9 Android Virtual Device. 
3.	Verified that the emulator was detected and connected through ADB. 
4.	Accessed the Android shell of the running emulator. 
5.	Examined the Android version, SDK/API level, and CPU architecture. 
6.	Inspected the Linux kernel information of the Android emulator. 
7.	Checked boot-related properties, including slot and verified-boot information. 
8.	Examined the mounted filesystems and storage usage of the emulator. 
9.	Inspected the available block-device mappings and their symbolic links. 
10.	Navigated through the /system, /vendor, and /product directories to examine the Android system file structure. 
11.	Recorded the observed system architecture, storage, filesystem, and partition-related information for analysis.

Commands Used -

adb devices

adb shell

getprop ro.build.version.release

getprop ro.build.version.sdk

getprop ro.product.cpu.abi

uname -a

getprop ro.boot.slot_suffix

getprop ro.boot.verifiedbootstate

cat /proc/cmdline

df -h

cat /proc/mounts

cat /proc/partitions

ls -l /dev/block/by-name

ls /system

ls /vendor

ls /product

exit
