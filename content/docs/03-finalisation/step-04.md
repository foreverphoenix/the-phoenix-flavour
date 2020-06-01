---
title: "ENBSeries"
weight: 4
type: docs
description: >
  Downloading and installing the latest binaries with ENB Man.
---

## 4.1 General Notes

ENBSeries with a decent preset is the most performance-intense graphical improvement. It can also have a huge impact visually. To get stable 60FPS with an ENB preset you need a decently strong PC and quite possibly tone down some settings but it is very doable. Even if you’re not interested in all the bells and whistles, ENB ambient occlusion, complex particle lights and colour correction alone are certainly worthwhile.

With ENB Man - the preset management tool we will be using - you can easily switch between presets. ENB presets can be edited and toggled directly ingame at any time.

## 4.2 ENBSeries Overview

### 4.2.1 ENBSeries binaries

These are the core files required to run ENBSeries. They are forbidden to be shared with presets and can only be acquired from the official website. They consist of two plugins, `d3d11.dll` and `d3dcompiler_46e.dll`, that belong into your **root** folder.

### 4.2.2 enbseries.ini

The bulk of configuration changes are stored in the ==enbseries.ini== file in which you can tweak all general settings and toggle them on or  off. This INI is unique to its preset and also belongs into your **root** folder.

### 4.2.3 enbseries folder

This folder should be located in your **root** folder and it includes all additional effect files (INI files and additional folders). The included effects vary from preset to preset, depending on what the author is utilising. In rare cases, the effect INIs are outside the **enbseries** folder and kept in the **root** folder as well (this is the case for the guide’s preset, Visceral ENB).

### 4.2.4 enblocal.ini

The `enblocal.ini` stores your personal settings and it’s completely independent from your preset which is why we are going to set up a global configuration that you can easily tweak and apply at any time for any preset. Settings you can control through the INI file are hotkeys, forcing VSYNC / frame lock, preset shader cache, some fixes and additional graphical options such as antialiasing.

## 4.3 ENB Man Setup

* Download [ENB Man](https://www.nexusmods.com/skyrim/mods/57620) (the main file) manually from the Nexus.
* Extract **ENBMan.exe** to `Your Modding Folder\Tools\ENB Man`.
* **(Optional)** Add **ENBMan.exe** to your Desktop / Taskbar.
* Run **ENBMan.exe** and click the green plus to add a new game.
* Click the folder icon and point ENBMan at your **SkyrimSE.exe** (located in your root folder).
* You might want to edit the name to indicate that it’s the Special Edition (I’ve changed it to **Skyrim SE**).
* Click the green checkmark to confirm.
* Double-click the new **Skyrim SE** profile.

![ENB Man 1 - Game Setup](/Pictures/finalisation/enb1_game_setup.png)

## 4.4 ENBSeries Binaries

* Download the latest version of [ENBSeries for Skyrim SE](http://enbdev.com/download_mod_tesskyrimse.htm).
* Open the downloaded archive and double-click the **WrapperVersion** folder.
* Back in ENB Man, click the arrow under **Binaries** and select **Add**.
* Enter **ENBSeries** and the version number as name (eg **ENBSeries 0.390**).
* Click the green checkmark to confirm.
* From the archive’s **WrapperVersion** folder, drag the following files into the empty **Binaries** window:
  * `d3d11.dll`
  * `d3dcompiler_46e.dll`
  * `enblocal.ini`
* Click the green checkmark to confirm.

![ENB Man 2 - Binaries](/Pictures/finalisation/enb2_binaries.png)

## 4.5 Global INI Settings

### 4.5.1 Import enblocal INI

* Click the gears icon under **Global Settings**.
* A new window will come up. Click the green plus icon.
* Enter **enblocal.ini** as name. It will now appear in the list.
* Double-click your new **enblocal.ini**.
* In the new window, click **Import Settings** in the top bar.
* Navigate to `Your Modding Folder\Tools\ENBMan\Games\Skyrim SE\Binaries\ENBSeries 0.4xx`.
* Double-click the **enblocal.ini** inside to import it and check all boxes.

### 4.5.2 Save Global Configuration

* Click **Save** in the top bar (the hard drive icon) and close the window.
* Back in the **Global Configuration Files** window, check **enblocal.ini.**
* Click the green checkmark to close the window.

![ENB Man 3 - Global INI Settings](/Pictures/finalisation/enb3_global_ini_settings.png)