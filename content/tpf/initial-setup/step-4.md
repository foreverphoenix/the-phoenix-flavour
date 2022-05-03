---
title: "Step 4: Stock Game Folder"
weight: 4
type: docs
description: >
  Creating a separate copy of Skyrim SE for TPF.
---

## About Stock Game Folder

The Stock Game folder method was figured out by especially wrinkly brains on the Wabbajack Discord to solve the issue of various lists having root folder files that would conflict. The biggest problem at the time was ENB (you can only have one preset installed at the same time), but since the release of Skyrim AE, different mod lists are also using different versions of Skyrim.

In order to make the TPF setup, including its root folder, fully standalone we will copy over the game files into our Mod Organizer 2 directory. This will require some additional steps for installing certain modding tools and cost 13GB of extra space, but will allow you to run multiple different modded setup at the same time while leaving your actual root folder completely untouched.

**Close Mod Organizer 2 before you proceed.**

### Creating the Stock Game folder

Navigate to your Mod Organizer 2 installation directory and create a new folder called **Stock Game** inside.

Next, go into your **root folder**: `\Steam\steamapps\common\Skyrim Special Edition\` and copy all its contents, including the executables and folders into the new **Stock Game Folder**.

It should look like this:

![Vanilla Stock Game](/Pictures/tpf/initial-setup/vanilla-stock-game.png)

## Optimised Textures

The Stock Game folder, while brilliant, requires an extra ~13GB of space since it is a full copy of the base game. Thankfully we can replace the texture BSAs with optimised ones which will reduce the folder's size by about 5GB. Since TPF's texture replacers cover (almost) all textures anyway, having (very slightly) reduced quality versions of the vanilla textures makes no difference whatsoever.

- Open the [Unofficial Performance Optimized Textures](https://www.nexusmods.com/skyrimspecialedition/mods/21166?tab=files) Nexus mod page.
- Click the **manual download** button for the main file (see picture below).
- Once the archive has been fully downloaded, open it.
- Extract the BSAs to `\Mod Organizer 2\Stock Game\Data\` and confirm to overwrite.

![Download UPOT](/Pictures/tpf/initial-setup/download-upot.png)

## Updating MO2

MO2 currently still uses the game files in the default root folder so we need to change that.

- Find the **ModOrganizer.ini** in the MO2 folder and open it in your preferred text editor.
- In **Line 4** under **Game Path**, change the file path to the **Stock Game** folder, e.g.:

![Stock Game INI](/Pictures/tpf/initial-setup/stock-game-ini.png)

Save your change and close the INI file.

### Updating the executables

Although you are unlikely to be using the **SkyrimSE.exe** and **SkyrimSELauncher.exe** any time soon, I still recommend updating their executable settings for the new Stock Game folder in Mod Organizer 2:

- Open the **Executables** settings in Mod Organizer 2 (click the gears icon in the Toolbar).
- Change the file paths under **Binary** and **Start In** for both executables to the EXE file and Stock Game folder respectively.
- Make sure to click **Apply** before you close the settings window.

![MO2 Update EXEs](/Pictures/tpf/initial-setup/mo2-update-exes.png)

## MO2 Plugins

Mod Organizer 2 is extendable with third-party plugins.

### Crash Log Tools

Crash Log Tools by Parapets improves crash logs created by [a mod](https://www.nexusmods.com/skyrimspecialedition/mods/59596) that will be installed later on.

- Download [Crash Log Tools](https://www.nexusmods.com/skyrimspecialedition/mods/66743?tab=files) from the Nexus (click the **Manual Download** button).
- Open the archive and extract the folder inside to `\Mod Organizer 2\plugins\`

## Test Run

Finally we can open Mod Organizer 2 again which should now be using the new Stock Game folder. Let's try launching Skyrim through MO2 to make sure everything was updated correctly.

If Skyrim launches without issues, quit from the main menu and continue with the next step.

![MO2 Update EXEs](/Pictures/tpf/initial-setup/mo2-launch-skyrim.png)

---

#### Continue with the [Creation Kit](/tpf/initial-setup/step-5/) page.
