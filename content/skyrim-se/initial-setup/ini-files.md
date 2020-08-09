---
title: "INI Files"
weight: 6
type: docs
description: >
  Optimising the INI files with BethINI.
---

## Generate Fresh INI Files

The basic game settings are saved in two INI files, **Skyrim.ini** and **SkyrimPrefs.ini**, and split up (somewhat arbitrarily) between them. In order to ensure that your INIs are completely untouched and vanilla, we will regenerate them before optimising them.

### Remove old files

If you had Skyrim SE installed previously, follow these steps:

* Locate your default INI files in the following directory:
  * `C:\Users\{USERNAME}\Documents\My Games\Skyrim Special Edition`
* If you have old save games you wish to keep, back up the **saves** folder now.
* Delete everything inside the **Skyrim Special Edition** folder.

### Generate new INIs

Continue with regenerating the INI files from scratch:

* Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your Game Library.
* Hit **Play** to open the regular launcher.
* A window will come up, informing you that Skyrim SE will now be configured based on your hardware.
* Click **OK** twice to confirm and hit **Exit** once it’s done.

![Regenerating INIs](/Pictures/setup/regenerating_inis.png)

## Install BethINI

* Download the latest version of [BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875) manually from the Nexus.
* Extract the downloaded archive to `Your Modding Folder\Tools\BethINI`.
* Close Mod Organizer 2.
* Double-click **BethINI.exe**.

## BethINI Configuration

### BethINI - Setup

* After starting BethINI, you will be prompted with a window asking you to choose your game.
* Select **Skyrim Special Edition** from the drop-down menu.
* Once BethINI has loaded up, go to the first tab, **Setup**.
* All filepaths should be configured correctly out of the box, however it’s best to double-check:
  * **Game Path** should point at your **root** folder, `steamapps\common\Skyrim Special Edition`.
  * **Mod Organizer** should point at your MO2 folder, `{Your File Path}\Mod Organizer 2`.
  * **INI Path** should point at your MO2 profile: `ModOrganizer 2 > The Phoenix Flavour`.

> Changing the INI Path will prompt BethINI to restart. Click No when asked about using the skyrimcustom.ini file.

![BethINI Setup](/Pictures/setup/bethini_setup.png)

### BethINI - Basic

Continue with the second tab, **Basic**.

- Set **Resolution** to the correct value for your monitor.
- Make sure to check **Recommended Tweaks**.
- **BethINI** presets should be toggled automatically.
- Select the **Medium** preset.
- Disable both **VSYNC** and **Lock Frame Rate**.

> Vanilla VSYNC and frame lock are not optimal, both will be handled by mods later on. As for the selection of the **Medium** preset, I recommend it because it's a good balance between graphic fidelity and performance. Many of the settings can and will be changed to improve visuals but as a baseline, **Medium** is perfect.

![BethINI Basic](/Pictures/setup/bethini_basic.png)

### BethINI - Interface

Continue with the fifth tab, **Interface**.

- Uncheck **Mod Manager Menu**. This will disable the menu entry leading to the Bethnet mods.
- Enable **Dialogue Subtitles** and **General Subtitles** if you need them (you can toggle them ingame as well).
- I prefer my **Lock Sensitivity** at `0.0450` but this will come down to personal taste and your mouse configuration.

> Unchecking Bethesda Modding Platform is not recommended because it's buggy. There are mods that achieve the same thing.

![BethINI Interface](/Pictures/setup/bethini_interface.png)

### BethINI - Detail

Continue with the sixth tab, **Detail**.

- **Water:** Check `Reflect Objects`.
- **Decal Quantity:** Set to `High`.
- **Godrays**: Set them to `None` (performance-intense, ENB has better godrays).
- **Field of View:** Increase this if you prefer a wider FoV.
- **Particles:** Increase the particle count to `1500`.
- **Lens Flare:** Matter of taste. Personally I disable this.
- **Anamorphic Lens Flare:** Looks ugly, recommended to be turned off.
- **Shadow Resolution:** Set to `2048` (unless you have a very slow CPU).
- **Exterior Draw Distance:** Set to `8000`.
- **Tree Shadows:** Check the box for this setting.

> **Object LOD** reflections are broken in SSE, but the mod SSE Engine Fixes includes a fix. **Depth of Field** should not be disabled in the INI as it will make underwater look perfectly clear. By turning DOF all the way down in the ingame settings, you can disable it without breaking underwater visuals (if you dislike the DOF and/or want to use an ENB DOF effect instead).

![BethINI Detail](/Pictures/setup/bethini-detail.png)

### BethINI - View Distance

Continue with the seventh tab, **View Distance**.

- **Grass Fade:** Set to `15000` or higher.

![BethINI View Distance](/Pictures/setup/bethini_view_distance.png)

### BethINI - Visuals

Continue with the eighth tab, **Visuals**.

- Set **Contrast** to `-0.1800`. This should eliminate the "black crush" some people are experiencing in Skyrim SE.

![BethINI Visuals](/Pictures/setup/bethini_visuals.png)

## Save Changes

- Return to the second tab, **Basic**, and click `Save and Exit`.
- Restart Mod Organizer 2.
- You might be notified about the missing skyrimcustom.ini in which case you can just click **OK**.