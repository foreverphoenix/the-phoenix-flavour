---
title: "Step 7: INI Files"
weight: 7
type: docs
description: >
  Optimising the INI files with BethINI.
---

## BethINI Installation

The configuration files for Skyrim, **Skyrim.ini** and **SkyrimPrefs.ini**, are best configured through the **BethINI** tool. It is the first of several tools that we are going to install.

- Create a new folder called **Tools** in your Mod Organizer 2 directory: `\Mod Organizer 2\Tools`.
- Download the latest version of [BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875) manually from the Nexus.
- Extract the **BethINI Standalone** folder into your new **Tools** folder.

---

**Close Mod Organizer 2.** It should not be running when configuring INI files.

## BethINI Configuration

Double-click **BethINI.exe** to start configuring your INI files.

- You will be prompted with a window asking you to choose your game.
- Select **Skyrim Special Edition** from the drop-down menu.
- Once BethINI has loaded up, go to the first tab, **Setup**.

Make sure to update the file paths as follows:

- **Game Path** should point to your Stock Game folder: `\Mod Organizer 2\Stock Game\`.
- **Mod Organizer** should point to your MO2 folder: `\Mod Organizer 2\`.
- **INI Path** should point to your MO2 profile: `ModOrganizer 2 > The Phoenix Flavour`.

> Changing the Game and INI paths will prompt BethINI to restart.

- Click **No** when asked about using the **SkyrimCustom.ini** file.

![BethINI Setup](/Pictures/tpf/initial-setup/bethini-setup.png)

### BethINI - Basic

Continue with the second tab, **Basic**.

- Set **Resolution** to the correct value for your monitor.
- Make sure to check **Recommended Tweaks**.
- **BethINI** presets should be toggled automatically.
- Select the **High** preset.
- Disable both **VSYNC** and **Lock Frame Rate**.

> VSYNC and frame cap will be enforced by a mod later on.

![BethINI Basic](/Pictures/tpf/initial-setup/bethini-basic.png)

### BethINI - Interface

Continue with the fifth tab, **Interface**.

- Uncheck **Mod Manager Menu**. This will disable the menu entry leading to the Bethnet mods.
- Enable **Dialogue Subtitles** and **General Subtitles** if you need them (you can toggle them ingame as well).
- I prefer my **Lock Sensitivity** at `0.0450` but this will come down to personal taste and your mouse configuration.

> Unchecking **Bethesda Modding Platform** is not recommended because it doesn't fully remove all unwanted menu options.

![BethINI Interface](/Pictures/tpf/initial-setup/bethini-interface.png)

### BethINI - Detail

Continue with the sixth tab, **Detail**.

- **Particles:** Increase the particle count to `7500`.
- **Lens Flare:** Matter of taste. Personally I disable this.
- **Anamorphic Lens Flare:** Looks ugly, recommended to be turned off.
- **Shadow Bias:** Set to `0.3` to mostly fix the weird pyramid shapes in snowy regions.
- **Detailed Draw Distance:** Set to `3500`.
- **Ambient Occlusion:** Uncheck the box for this setting (covered by ENB).

> **Depth of Field** should not be disabled in the INI as it will make underwater look perfectly clear. By turning DOF all the way down in the ingame settings, you can disable it without breaking underwater visuals.

![BethINI Detail](/Pictures/tpf/initial-setup/bethini-detail.png)

### BethINI - View Distance

Continue with the seventh tab, **View Distance**.

- **Grass Fade:** Set to `15000` for to increase the distance at which grass is rendered.

![BethINI View Distance](/Pictures/tpf/initial-setup/bethini-view-distance.png)

### BethINI - Visuals

Continue with the eighth tab, **Visuals**.

- Lower **Grass Density** to **20**.
- Increase **Grass Diversity** to **15**.

![BethINI Visuals](/Pictures/tpf/initial-setup/bethini-visuals.png)

## Save Changes

Return to the second tab, **Basic**, and click **Save and Exit**.

Restart Mod Organizer 2. You might be notified about the missing skyrimcustom.ini in which case you can just click **OK**.

---

#### Continue with the [Additional Tools](/tpf/initial-setup/step-8/) page.