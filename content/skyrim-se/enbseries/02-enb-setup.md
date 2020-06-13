---
title: "02 ENB Setup"
weight: 2
type: docs
description: >
  Downloading and installing the latest binaries with ENB Man.
---

## 2.1 ENB Man

* Download [ENB Man](https://www.nexusmods.com/skyrim/mods/57620) (the main file) manually from the Nexus.
* Extract **ENBMan.exe** to `Your Modding Folder\Tools\ENB Man`.
* Run **ENBMan.exe** and click the green plus to add a new game.
* Click the folder icon and point ENBMan at your **SkyrimSE.exe** (located in your root folder).
* You might want to edit the name to indicate that it’s the Special Edition (I’ve changed it to **Skyrim SE**).
* Click the green checkmark to confirm.
* Double-click the new **Skyrim SE** profile.

![Game Setup](/Pictures/enbseries/enb-game-setup.png)

## 2.2 ENBSeries Binaries

### 2.2.1 Download Binaries

* Download the latest version of [ENBSeries for Skyrim SE](http://enbdev.com/download_mod_tesskyrimse.htm).
* Open the downloaded archive and double-click the **WrapperVersion** folder.
* Extract the following files from the **WrapperVersion** folder to `Your Modding Folder\temp`:
  * d3d11.dll
  * d3dcompiler_46e.dll
  * enblocal.ini

### 2.2.2 Import to ENB Man

* Back in ENB Man, click the arrow under **Binaries** and select **Add**.
* Enter **ENBSeries** and the version number as name (eg **ENBSeries 0.427**).
* Click the green checkmark to confirm.
* Drag the three files from your temp folder into the **Binary** window.
* Click the green checkmark to confirm.
* Delete the files from your **temp** directory.

![Install ENB Binaries](/Pictures/enbseries/install-enb-binaries.png)

## 2.3 Global INI Settings

### 2.3.1 Import enblocal INI

* Click the gears icon under **Global Settings**.
* A new window will come up. Click the green plus icon.
* Enter **enblocal.ini** as name. It will now appear in the list.
* Double-click your new **enblocal.ini**.
* In the new window, click **Import Settings** in the top bar.
* Navigate to `Your Modding Folder\Tools\ENBMan\Games\Skyrim SE\Binaries\ENBSeries 0.4xx`.
* Double-click the **enblocal.ini** inside to import it and check all boxes.

### 2.3.2 Save Global Configuration

* Click **Save** in the top bar (the hard drive icon) and close the window.
* Back in the **Global Configuration Files** window, check **enblocal.ini.**
* Click the green checkmark to close the window.

![Global INI Settings](/Pictures/enbseries/global-ini-settings.png)