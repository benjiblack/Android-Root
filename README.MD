# Rooting Android: A brief introduction.

---
## What is root?

"Root" is the friendly term given to superuser access in Linux to access to system level resources. Essentially admin rights.

Root access can allow you to Access, View & Modify:

- System Files.
- Private application data in the internal /data/ partition.
- Private application data in any external partition.
- The root folder at /
- Mounted storage at /storage/
- And much more.

## Why do you want/need root access?

>As an app developer you may want or need root access to test and debug your application if you use private storage for your app.

>>In Android, every app has special 'sandboxed' folders that only _your_ app can access. This can enable you to develop apps that take in user generated content and securely store it out of the reach of other applications and users.

>>However, when developing apps, we often need to be able to see and manage these folders to run tests, debug and verify.

### SuperSU & BusyBox
>##### SuperSU by Chainfire:
>An application that resides in the **system** partition that manages access to root privileges for apps & adb.SuperSU is responsible for the popup messages asking to confirm or deny root permissions.

>> **Note**:
>>Chainfire's SuperSU is not the only superuser permission manager, though it is by far the most popular and included in most root packages and toolkits.


>##### BusyBox: The Swiss Army Knife of Embedded Linux:
>BusyBox combines tiny versions of many common UNIX utilities into a single small executable. It provides replacements for most of the utilities you usually find in GNU fileutils, shellutils, etc

---
# What are Download mode, Recovery mode & the Bootloader.

> Commands to enter various boot modes are listed below for the ADB Shell.

- **Download mode:** (Only on some devices) A special boot mode that enables you to directly overwrite system partitions from a computer either via ADB Shell or by special firmware flashing tools like ODIN for Samsung devices.
_May require OEM Unlock on newer devices._ 

> adb reboot download

- **Recovery Mode**: A special boot mode that is usually only used by manufacturers for factory data reset. However, third party recovery mode software is available for most devices enabling you to flash a .zip package containing payloads for any partition as well as manage, delete and recreate partitions in general. _Third party recovery solutions are often required for the root process. Depends on the device in question._

> adb reboot recovery

- **The Bootloader:** is the part of the firmware that handles telling the device which partition to boot from: System, Recovery, Download Mode etc.. _Often, the bootloader blocks the execution of unverified code and therefore blocks third party recovery tools from being installed. Be prepared to have to 'unlock' your bootloader to gain root access._

> adb reboot bootloader

---
# Finding resources.
### Part 1: Where to look.
[XDA Developers Forums!](https://www.xda-developers.com)

Seriously. That's the #1 place you should _always_ begin. Do a search for your specific device and browse the device subforum for help and tutorials.
### Part 2: Things to consider.

Make sure when searching for help and information to keep in mind which variant of your device you are using. Devices can vary wildly between different carriers and software versions.

For example: The Samsung Galaxy S5 on T-Mobile can be rooted with custom recovery fairly easily. However, for the Verizon GS5, it's a nightmare. **Always verify your device against the instructions!**

>Following instructions for a device other than your own, no matter how similar, can easily result in a BRICK. While most software bricks can be somewhat easily resolved, there are some times when there's no coming back. Your device is gone forever.

### Part 3: _**BE CAREFUL WHAT YOU DOWNLOAD.**_
Don't click that random result from a sketchy website and just go crazy downloading unknown tools and installers.

Search for downloads, help, totorials and information on trusted sites first. Random Google results as a very last resort.

>Very often the download links presented on lesser known websites will lead to malware and tons of pornographic popup ads. _**Absolute last resort!**_

---
# Roms.
### Part 1: What Android is... And what it is _not_.
Android is a GNU/Linux based open source mobile operating system known as the Android Open Source Project (AOSP).

Android is NOT the Samsung, LG, HTC, SONY or any other OEM's skin, software or modifications.

Android does not come with the Google Play store or Google Services.

### Part 2: Roms!

- Roms are packages that contain an operating system usually based on the AOSP. 
- Often include tweaks for visual improvements and customizations.
- Usually support third party kernels for performance tweaks.
- Often just don't work.
- Can breathe new life in old hardware. 

>Example: I have a T-Mobile G1 (The first commercially available Android Phone) that's running Android 4.4 KitKat.

- Roms are usually installed in third party recovery tools and usually require the /system/, cache and /data/ partitions to be wiped before installation.

### Part 3: Google / GApps.

As stated before, Android itself does not include the Google Play Store or Google Play Services.

These packages are required for many apps and generally desired for full functionality in Android anyway.

Therefore it is recommended that you download the 'GApps' package the corresponds to the version of Android you are installing.

GApps often comes in different flavors depending on your needs including:

- Minimized packages including only the most basic functionality to access the play store and basic services like Google text-to-speech.
- Small packages that also include basic apps such as Gmail and other 'essential' apps.
- Normal packages that include, more or less, the usual Google apps and services included in your average smartphone.
- Complete packages that seek to include all of the above _and_ the most used and requested Google apps.
- And many more configurations depending on where you get the package from.

The most important installation is at least a minimized package. As long as you can get to the Play Store, you can get anything the other packages lack.


















