# iBasso DX220 firmware add-on by Lurker

## Introduction
Android 8.1 for DX220 protects main partitions with [Verity](https://source.android.com/security/verifiedboot), which makes it tricky for end user to flash custom firmware. [Magisk](https://magiskmanager.com/) allows developers to alter system systemless-ly, i.e. without any direct modification of the protected parts of the firmware image. That's why my modifications for 8.1 are distributed as add-ons: you must have installed and running the original firmware, then you apply (flash over) an add-on. It makes the download smaller and update process faster!

To check the current add-on version in Android mode, go to _Settings_, _About DX220_, _Build number_ at the bottom.

**WARNING:** Add-ons are *not* compatible with encrypted devices!<br />
**WARNING:** Do *not* update Magisk via MagiskManager! It will cause problems!

## How to apply or update the add-on
There are two packages to choose from: either Windows-only (using included AndroidTool), or any platform (using [DX220-bootable SD-card](https://github.com/Lurker00/DX220-Firmware-Add-on/tree/master/FirmwareUpdater)). The ZIP archive with the add-on contains `readme.txt` file with full instruction. Please read and follow it.

For Windows, you should have installed drivers from Rockchip. You can download them [here](https://github.com/Lurker00/DX220-Firmware-Add-on/tree/master/files).

**Note:** Updating an add-on removes additional [Magisk](https://magiskmanager.com/) modules. You'll have to re-install them after the update.

If you need Magisk Manager, please install it manually from the [official source](https://github.com/topjohnwu/Magisk/releases/).

## How to return back to the official firmware
After iBasso released OTA-like update (1.09.092, 1.10.123...), it is enough to re-apply any official firmware update, then do a factory reset.

## How to update the official firmware
True OTA does not work with add-on, because the build number is different. You need to download the update from [iBasso site](http://ibasso.com/down.php), put it to SD-card or Internal storage, and start manual upgrade. Then you may install an add-on compatible with the new firmware version, if any.

## Changes made
It's up to the end user to decide whether these changes affect sound or not. I believe some of them make sound better, and none of them make sound worse.

### Android
* Google Play Market added.
* Reduced power consumption during music playback and in suspend mode.
* Overall performance increased.
* During music playback, the device is managed to prevent idle state tasks.
* Performance tweak for popular music players (Neutron, UAPP, Tidal, Spotify). Such a tweak is used on Rockchip SoC based devices for benchmark apps, iBasso sets it for its Mango Player.
* The process of [device registration](https://www.google.com/android/uncertified/) is much simplified (required to make Google Play Services work on uncertified device).
* [Magisk](https://magiskmanager.com/) can be used to install additional modules, and to provide root access.
* [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md), which is also useful for its [System settings](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md#system-settings).
* Custom build of [HibyMusic](https://play.google.com/store/apps/details?id=com.hiby.music), which plays bit perfect PCM up to 32/384kHz with no additional efforts, and is fully compatible with [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md) for bit perfect DSD and SACD ISO playback.
* Removed APKPure, CoolAPK.

### Mango
* Removed Android services, that are not used in this mode.
* Performance increased.

### Common
* Safer parameters of battery charger to prevent overheating.
* Better thermal control.
* A different approach to control brightness at low levels.

**Note**: MagiskManager icon is, actually, a stub injected by Magisk core. It is intended by the developer to help installing full MagiskManager, but I disable it to stop annoying. Should you need [MagiskManager, please install it manually](https://github.com/topjohnwu/Magisk/releases).

## History of public releases
* [**1.24**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.24) - release for official firmware 1.16.241.
* [**1.23**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.23) - release for official firmware 1.15.233.
* [**1.22**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.22) - release for official firmware 1.13.202.
* [**1.21**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.21) - release for official firmware 1.12.149.
* [**1.20**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.20) - release for official firmware 1.11.140.
* [**1.19**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.19) - release for official firmware 1.10.123.
* [**1.18**](https://github.com/Lurker00/DX220-Firmware-Add-on/releases/tag/v1.18) - release for official firmware 1.09.092.
