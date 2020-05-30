---
title: "The Creation Kit"
weight: 3
type: docs
description: >
  Installing and customising the official modding tool.
---

## 3.1 Acquisition

With the release of Skyrim SE, Bethesda also published a new version of their official tool kit, the Creation Kit (or CK for short), updated for the new 64bit engine. Unfortunately the CK 2.0 can no longer be downloaded directly from Steam but requires the Bethesda Launcher and a Beth.net account.

> The Bethesda Launcher is not required beyond installing the Creation Kit and you can safely uninstall it after that is done.

- Go to Bethesda.net, the official website.
- Scroll all the way down to the footer (bottom of the page).
- Click the **Download** button in the **Bethesda Launcher** section.
- Double-click the downloaded executable.

![Download Beth Launcher](Pictures/setup/download_beth_launcher.png)

## 3.2 Installation

* Let the executable guide you through the installation process.
* When that is done, you must log-in with your Beth.net account or register a new one.
* Once you’re logged in, check the list of game icons on the left.
* Click the two arrows `>>` at the top to open the full list.
* Select **Creation Kit: Skyrim** (with the white icon) and click **Install**.
* The CK should be installed directly into your **root** folder (see picture).
* Wait for the files to download.

![Creation Kit Installation Path](Pictures/setup/ck_installation_path.png)

## 3.3 Disable Auto Updates

* In the Bethesda Launcher, go to **Game Options**.
* Toggle off **Auto Updates**.
* Close the Bethesda Launcher.

![Disable Auto Updates](Pictures/setup/ck_disable_auto_updates.png)

## 3.4 Custom INI

The custom INI file will allow you to load mods with multiple master files as well as fix some Creation Kit issues and crashes.

* Download this tweaked **[Creation Kit Custom INI](https://www.nexusmods.com/skyrimspecialedition/mods/19817)** (the main file) manually from the Nexus.
* Extract the INI file into your **root** folder.

## 3.5 Creation Kit Fixes

It’s Bethesda, what did you expect?

- Download **[SSE Creation Kit Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/20061)** (CK64 Fixes release 2.x) manually from the Nexus.
- Extract the three DLL files and the INI into your **root** folder.
- **Optional:** Move the archive to `Your Modding Folder\ARCHIVE\CK Fixes` to keep as a backup.

> We are not downloading the other CK Fixes main file because it is not needed for anyone except mod authors.

## 3.6 Vanilla Scripts

The Creation Kit installation includes a **Scripts.zip** which contains all source files for the vanilla Skyrim scripts. With these source files it is possible to edit and recompile vanilla scripts. This is usually unnecessary unless you plan on tinkering with the scripts themselves which we are in fact going to do at the very end of the guide.

### 3.6.1 Unpacking Scripts.zip

* Navigate to your **root** folder and launch **CreationKit.exe** from there.
* You will be asked to unpack **Scripts.zip**, click **Yes**.
* Once that is done, you can close the Creation Kit.

### 3.6.2 Fixing Filepaths

- Rename the **Source** folder in your **Data** folder to **Scripts**.
- Double-click the **Scripts** folder.
- Rename the **Scripts** folder inside to **Source**.
- The resulting filepath should be:
  - `Skyrim Special Edition\Data\Scripts\Source`
