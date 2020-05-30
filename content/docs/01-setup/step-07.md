---
title: "Additional Tools"
weight: 7
type: docs
description: >
  Setting up additional modding software.
---

## 7.1 SSEEdit

### 7.1.1 Installation

* Download **[SSEEdit ](https://www.nexusmods.com/skyrimspecialedition/mods/164/)**manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\SSEEdit`.
* Open the downloaded archive and extract everything into the new folder.
* Open Mod Organizer 2 and go into the **Executables** settings (Tools > Executables or CTRL + E).
* Click the tiny blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit`and double-click **SSEEdit.exe**.
* Click **Apply** to save the new executable.

![Add SSEEdit to MO2](Pictures/setup/add_sseedit_to_mo2.png)

### 7.1.2 SSEEdit Cache Output

Every time a new plugin is loaded into SSEEdit, a refcache file will be generated for it so that the next time it won’t have to processed again – SSEEdit can simply read the cache file, significantly shortening the startup time.

In order to store the cached files with the program files themselves, we need to add an argument for it:

* Under **Arguments**, enter the following:
  * `-C:"...\Your Modding Folder\Tools\SSEEdit\cache\"`
* Replace the **"…\Your Modding Folder..."** part with the file path on your end. This is what I added:
  * `-C:"F:\Modding\Skyrim SE Mods\Tools\SSEEdit\cache\"`
* Click **Apply** to save.

> Whenever you update SSEEdit, the accumulated refache files will also be wiped (as they should be) and new ones will be generated and stored in the same directory when you next launch SSEEdit without you having to complete any additional steps. 

### 7.1.3 QuickAutoClean

* Click the tiny blue plus icon to add another new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit`and double-click **SSEEditQuickAutoClean.exe**.
* **Optional:** Change the title to something less verbose (like "SSEEdit – Quick Cleaning").
* Under **Arguments**, enter the following:
  * `-DontCache`
* Click **OK** to save and close the window.

> The **-DontCache** argument will prevent an obscure bug that destroys parts of Apocrypha during the cleaning of Dragonborn.esm.

![Add QuickAutoClean to MO2](Pictures/setup/add_quickautoclean_to_mo2.png)

## 7.2 zEdit

### 7.2.1 Installation

* Download the latest version of [zEdit](https://github.com/z-edit/zedit/releases) from Github:
  * zEdit_v0.6.5_-_Portable_x64.7z
* Create a new folder: `Your Modding Folder\Tools\zEdit`.
* Open the downloaded archive and extract everything into the new folder.
* Switch back to Mod Organizer 2 and open the **Executables** settings (Tools > Exectuables or CTRL + E).
* Click the tiny blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\zEdit` and double-click **zEdit.exe**.
* Click **OK** to close the window.

![zEdit Download](Pictures/setup/zedit_download.png)

### 7.2.2 Configuration

* Run zEdit through Mod Organizer 2.
* Click the gears icon to open the **Profile** settings.
* Make sure **Path** (for Skyrim SE) correctly points to your Skyrim SE **root** folder.
* Close the profile settings window.

### 7.2.3 zMerge Settings

* Select **zMerge** from the drop-down menu in zEdit and hit **Start Session**.
* Click the gears icon in the top right to open the settings.
* Switch to the **Integration Settings** tab and apply these settings:
  * **Mod manager:** Mod Organizer 2
  * **MO2 instance:** portable
  * **Mod manager path:** `{Your File Path}\Mod Organizer 2`
  * **Mod manager mods path:** `{Your File Path}\Mod Organizer 2\mods`
* Switch to the **Merge Settings** tab:
  * **Merge output path:** `{Your File Path}\Mod Organizer 2\mods`
  * **Integration:** uncheck **Disable plugins** and **Disable mods**
* Once you have made sure everything is configured correctly, hit **OK** and close zEdit.

## 7.4 Cathedral Assets Optimizer (CAO)

### 7.4.1 Installation

* Download the latest version of [Cathedral Assets Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/23316) manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\Cathedral Assets Optimizer`.
* Open the downloaded archive and extract everything into the new folder.

> You will be using CAO plenty of times during the installation of the guide, so I recommend adding it to your Windows Taskbar for quick access.

### 7.4.2 Profiles

With the latest versions of CAO, you can set up dedicated profiles to switch between the two primary uses of CAO at will. I created several profiles for different purposes to be used during the installation of  the guide.

* Download [The Phoenix Flavour - CAO Profiles Pack](https://www.nexusmods.com/skyrimspecialedition/mods/14223) from the guide’s Nexus page.
* Open the downloaded archive.
* Extract all folders to `Your Modding Folder\Tools\Cathedral Assets Optimizer\profiles`.

## 7.5 SSE NIF Optimizer

While the vast majority of SLE meshes can be fixed with Cathedral Assets Optimizer, there are some that will only work properly after running them through the original SSE NIF Optimizer.

### 7.5.1 Installation

* Download [SSE NIF Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/4089) manually from the Nexus.
* Extract the executable into Your Modding Folder. It’s just a single file so no separate directory is required.

## 7.6 Modwatch

* Download [Modwat.ch](https://www.nexusmods.com/skyrim/mods/56640) manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\Modwat.ch`.
* Open the downloaded archive and double-click the "Modwatch-win32-ia32" folder within.
* Extract everything into the new folder.