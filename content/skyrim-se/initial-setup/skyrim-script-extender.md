---
title: "Skyrim Script Extender"
weight: 5
type: docs
description: >
  Properly installing the Skyrim Script Extender.
---

## Download

* Download [SKSE64](http://skse.silverlock.org/). You need build **2.0.19** for the current version of Skyrim SE.
* Save the downloaded archive to `Your Modding Folder\ARCHIVE\SKSE64`.

If on the main page for SKSE there is a different version number than the one noted above, Skyrim and the Script Extender were likely updated and you need to download the previous version from the archive page (see picture below).

![SKSE Download](/Pictures/setup/skse_download.png)

## Installation

### Binaries

* Extract the archive’s contents to `Your Modding Folder\temp`.
* Move the following three files into your Skyrim SE **root** folder:
  * **skse64_skyrim version number.dll**
  * **skse64_loader.exe**
  * **skse64_steam_loader.dll**

![SKSE Binaries Installation](/Pictures/setup/skse-binaries-installation.png)

### Scripts

* Go back to your **temp** folder with the remaining files.
* Move the **Data** folder to `Mod Organizer 2\mods`.
* Rename the folder to **SKSE - Data 2.0.x** (where x is the current version number).
* Delete all remaining files inside your **temp** folder.
* Switch back to Mod Organizer 2.
* Press F5 to refresh and the new mod will show up below the official master files.
* Click the checkmark to activate the mod.

![SKSE Scripts Installation](/Pictures/setup/skse-scripts-installation.png)

## SKSE INI

* Open the [SKSE64 ini pre-download for lazy users](https://www.nexusmods.com/skyrimspecialedition/mods/1651) Nexus page.
* Click "Mod Manager Download" for the `SKSE64 INI PRE DOWNLOAD v1.2` main file.
* Back in Mod Organizer 2, switch to the **Downloads** tab.
* Double-click the mod there and click **OK** to install it.
* Move it below **SKSE64 - Data v2.0.x** in the mod order and activate it.

## SKSE Launcher

* Restart Mod Organizer 2.
* The SKSE Launcher executable will now be automatically added to the executables list in MO2.
* Select **SKSE** in the list and click **Run**.

> At this point (and when testing later on) you’ll benefit a lot from having this page open on a secondary monitor or alternatively your phone or tablet in order to avoid having to tab out.

![Run SKSE](/Pictures/setup/run-skse.png)

## Verify Installation

* Once you are in the Skyrim SE main menu, bring up the console by pressing the tilde key on your keyboard (above TAB, next to 1).
* Type in ``getskseversion`` and hit Enter. It should return the version number of your SKSE64 installation.
* After confirming that SKSE64 was installed correctly, type **qqq** in the console and hit Enter to quickly close the game.

![Verify SKSE64](/Pictures/setup/verify_skse64.jpg)