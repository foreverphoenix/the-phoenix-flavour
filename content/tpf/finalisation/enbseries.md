---
title: "ENBSeries"
weight: 10
type: docs
description: >
  Installation of ENBSeries with Serio's ENB.
---

## What is ENBSeries?

ENBSeries is a post-processing injector by Boris Vorontsov. Unlike ReShade, it is not universal but built for specific games and hooks directly into the engine. Effects are therefore highly advanced and specific to each games. ENB is also capable of fixing bugs and improving performance plus it offers additional features such as VSYNC, a screenshot hotkey, and a toggleable FPS counter.

The effects vary in their performance impact. A full preset, especially when Skyrim is run on high resolutions, can bring even high-end PCs to their knees. Fortunately, Skyrim SE with its generally improved performance runs a great deal better with ENBSeries presets and 60FPS+ on a reasonable resolution (1080p) are comfortably attainable on most machines.

TPF uses **Serio's ENB**, preset for Cathedral Weathers that is fairly performance-friendly and doesn't break vanilla imagespaces (for Nighteye). For better compatibility with our lighting overhaul, we will be using a version of it tweaked specifically for the guide.

### Is installing ENBSeries mandatory?

Yes and no.

ENB and Serio's preset are part of the guide. You are not supposed to skip these instructions. However, disabling ENBSeries is as simple as pressing a single key ingame or clicking "Uninstall" in ENB Man.

The problem is that the guide was made with ENB in mind. For example, Skyrim's native ambient occlusion was disabled early on in the guide in favour of ENB AO. A number of mods installed up until this point are exclusively for ENB, fixing mesh brightness or adding effects.

Ultimately, you shouldn't encounter any major issues when disabling ENB. If you don't like the effect or find the performance impact too jarring, you can essentially skip this step or uninstall ENB later on. The point is that I will not be responsible for any visual inconsistencies or bugs stemming from a user's refusal to use ENBSeries.

If you choose not to use ENBSeries, it is advisable to re-enable Skyrim's native ambient occlusion and lower the particle count, both done in the SkyrimPrefs.ini file.

## ENBMan

ENBMan is one of several ENB manager tools available. It happens to my favourite which is why we are using it for TPF. One downside of ENBMan is that importing files directly from archives usually doesn't work so an extra step is required, extracting files, and then importing them in ENBMan. That's a small inconvenience for an otherwise highy convenient tool though.

- Download [ENBMan](https://www.nexusmods.com/skyrim/mods/57620?tab=files) (the main file) manually from the Nexus.
- Extract **ENBMan.exe** to `Your Modding Folder\Tools\ENB Man`.
- Run **ENBMan.exe** and click the green plus to add a new game.
- Click the folder icon and point ENBMan to your **SkyrimSE.exe** (located in your root folder).
- You might want to edit the name to indicate that it’s the Special Edition (I’ve changed it to **Skyrim SE**).
- Click the green checkmark to confirm.
- Double-click the new **Skyrim SE** profile.

![Game Setup](/Pictures/tpf/finalisation/enb-game-setup.png)

## ENBSeries Binaries

* On the website for [ENBSeries for Skyrim SE](http://enbdev.com/download_mod_tesskyrimse.htm), click on the latest version number (near the bottom).
* Scroll down and click the **download** below the changelog.
* Open the downloaded archive and double-click the **WrapperVersion** folder.
* Extract the following files from the **WrapperVersion** folder to `Your Modding Folder\temp`:
  * d3d11.dll
  * d3dcompiler_46e.dll
  * enblocal.ini

### Import to ENBMan

* Back in ENBMan, click the arrow under **Binaries** and select **Add**.
* Enter **ENBSeries** and the version number as name (eg **ENBSeries 0.452**).
* Click the green checkmark to confirm.
* Drag the three files from your temp folder into the **Binary** window.
* Click the green checkmark to confirm.
* Delete the files from your **temp** directory.

![Install ENB Binaries](/Pictures/tpf/finalisation/install-enb-binaries.png)

## Global INI Settings

* Click the gears icon under **Global Settings**.
* A new window will come up. Click the green plus icon.
* Enter **enblocal.ini** as name. It will now appear in the list.
* Double-click your new **enblocal.ini**.
* In the new window, click **Import Settings** in the top bar.
* Navigate to `Your Modding Folder\Tools\ENBMan\Games\Skyrim SE\Binaries\ENBSeries 0.4xx`.
* Double-click the **enblocal.ini** inside to import it.
* Press CTRL+A to select all settings and click the green checkmark button in the toolbar to enable them.

### Better Hotkeys

I'm personally not a fan of the default ENB ingame hotkeys. "KeyUseEffect", for instance, is on Shift+F12. At the same time, F12 is the Steam hotkey for "Take Screenshot". You can see how that might result in many unwanted screenshots.

Check the screenshot below and mirror my values in the input section to get the following hotkeys:

- **KeyCombination:** Disabled.
- **KeyDof:** Disabled.
- **KeyEditor:** F11
- **KeyFPSLimit:** Disabled.
- **KeyScreenshot:** Disabled.
- **KeyShowFPS:** F7
- **KeyUseEffect:** F10

This means you can quickly toggle ENB ingame with F10, open the GUI to customise the preset with F11, and bring up a nifty FPS counter anytime with F7. No default keys are affected (like F5 and F9 for Quick Save and Quick Load respectively) and screenshots you can continue to take with F12 using the Steam overlay.

> If you want different hotkeys, use [this super useful website](https://keycode.info/) to figure out any key's numeric value.

![ENB Better Hotkeys](/Pictures/tpf/finalisation/enb-better-hotkeys.png)

### Save Global Configuration

- Click the green checkmark at the bottom, then click **Yes** to confirm and save your changes.
- Back in the **Global Configuration Files** window, check the box next to **enblocal.ini.**
- Click the green checkmark to close the window.

![ENB Better Hotkeys](/Pictures/tpf/finalisation/enb-global-ini.png)

## Serio's ENB

* Open the [Serio's ENB](https://www.nexusmods.com/skyrimspecialedition/mods/30506?tab=files) mod page.
* Download the **Serio's ENB - TPF Edits** miscellaneous file manually.
* Open the downloaded archive and double-click the folder inside.
* Extract the following files to `Your Modding Folder\temp`:
  * enbseries
  * enblocal.ini
  * enbseries.ini

### Disable Distant Reflections 

- Open the **enbseries.ini** in a Notepad++.
- Scroll down to **Line 1122**.
- Set **DisableDistantReflections** to **true**.
- Hit CTRL+S to save your changes and close the window.

> This will improve the way water looks in the distance.

### Create a new preset

* In ENBMan, click the arrow under **Presets** and select **Blank preset**.
* Enter a name for the new preset: `Serio's ENB for Cathedral Weathers 1.10`.
* Click the green checkmark to confirm.

![Create New Preset](/Pictures/tpf/finalisation/create-new-preset.png)

### Import files into preset

* Drag-and-drop all files from the **temp** folder into ENB Man.
* Click **No** both times when asked to add the palettes to ENB Man.
* Remove all files inside the **temp** folder.

*Reference picture shows a different preset but the process is the same.*

![Import Preset Files](/Pictures/tpf/finalisation/install-enb-preset.png)

### Activate the preset

* Select the latest version of ENBSeries under **Binary** and tick the checkbox.
* Click the green checkmark at the bottom of the window to install the preset.

*Reference picture shows a different preset but the process is the same.*

![Enable Preset](/Pictures/tpf/finalisation/activate-enb-preset.png)