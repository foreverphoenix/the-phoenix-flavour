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

## Downgrading to pre-AE

Because the Script Extender and certain other mods are version dependent, you must run a specific version of Skyrim SE. In the post-Anniversary Edition age of Skyrim modding, we are going to be running the last pre-AE patch of Skyrim SE, `1.5.97.0`, so we can use the version of SKSE that all mods are compatible with.

You can check your current Skyrim SE version number by going into the Properties for the **SkyrimSE.exe**, the main executable.

- Right-click **SkyrimSE.exe** in your **Stock Game** folder and select **Properties**.
- Switch to the **Details** tab and check under **Product version**.

![Skyrim SE 1.6.323.0](/Pictures/tpf/initial-setup/skyrim-se-1-6-323-0.png)

### Downgrade Patcher

In order to revert to the last pre-AE version of Skyrim SE, `1.5.97.0`, we will be using Halgari's downgrade patcher.

- Open the [Unofficial Skyrim Special Edition Downgrade Patcher](https://www.nexusmods.com/skyrimspecialedition/mods/57618?tab=files) Nexus page.
- Click the **Manual Download** button for the **Patcher.exe** main file.
- I recommend saving the executable to a new folder within `\Your Modding Folder\Tools\`.

Once the patcher is fully downloaded, double-click the executable to run it.

- Click **OK** if the patcher could not locate SSE automatically.
- Click the folder icon under **Game Location** and navigate to your **Stock Game** folder.
- Double-click the **SkyrimSE.exe** and click **Start Patching**.

The process will take a few minutes. Wait until the tool has finished before you proceed.

If you check the **SkyrimSE.exe** now, it should be back to version `1.5.97.0`.

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

## Test Run

Finally we can open Mod Organizer 2 again which should now be using the new Stock Game folder. Let's try launching Skyrim through MO2 to make sure everything was updated correctly.

If Skyrim launches without issues, quit from the main menu and continue with the next step.

![MO2 Update EXEs](/Pictures/tpf/initial-setup/mo2-launch-skyrim.png)

---

#### Continue with the [Creation Kit](/tpf/initial-setup/step-5/) page.
