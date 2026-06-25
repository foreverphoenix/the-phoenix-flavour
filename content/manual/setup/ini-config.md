---
title: "INI Configuration"
weight: 4
type: docs
description: >
  In this step, we will discuss INI files and use BethINI Pie to configure the game's default set. We will also create a shared folder for modding tools.
---

## Vanilla INI Files (*)

{{< alert color="info" >}}If you are already familiar with Skyrim's INI files or you don't want to know the details, feel free to skip ahead to [the next section](/manual/setup/ini-config/#ini-files-and-mo2).{{< /alert >}}

Skyrim can be modified through a set of INI files:

- Skyrim.ini
- SkyrimPrefs.ini

Both can be found under `\Documents\My Games\Skyrim Special Edition\`, aka the **INI Folder**.

These INI files were regenerated during the [Clean Install](/manual/setup/clean-install/) and a performance preset (low, medium, high, etc) was applied when opening the launcher for the first time.

There is also a `SkyrimCustom.ini` which does not exist in vanilla but can be created in the same directory to overwrite the other two INIs.

{{< alert color="info" >}}You can always restore the default set of vanilla INIs by deleting them from the INI folder and launching the game through Steam to regenerate them.{{< /alert >}}

### Valid Settings

Not all settings are valid in all INI files.

- **Skyrim.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimCustom.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimPrefs.ini** can modify a limited range of settings ([documented here](https://stepmodifications.org/wiki/SkyrimSE:SkyrimPrefs_INI)).

The catch is that duplicate INI settings are overwritten in the following order:

- **SkyrimPrefs.ini** >> **SkyrimCustom.ini** >> **Skyrim.ini**

{{< alert color="info" >}} For example, if **bFXAAEnabled=** is set to **1** in the **Skyrim.ini** and set to **0** in the **SkyrimPrefs.ini**, the latter will overwrite and FXAA will be off (0) ingame.{{< /alert >}}

### Plugin INIs

INIs can also be attached to **plugins** (ESP, ESL, ESM). Similar to BSAs, they are loaded if they have the same name as the plugin.

Any setting that is <u>not valid</u> in the **SkyrimPrefs.ini** can be added to a plugin INI.

Plugins that load INI files are displayed with a paper clip icon in the load order.

![Plugin with INI](/Pictures/manual/setup/ini-config/plugin-with-ini.png)

## INI Files and MO2

Since the purpose of MO2 is to leave all original files and folders unmodified, it can also manage a separate set of INI files.

When we created our MO2 profile in the previous step, we enabled **profile-specific** INI files. That means copies of **Skyrim.ini** and **SkyrimPrefs.ini** from the INI folder were placed into our profile folder -- `\Mod Organizer 2\profiles\The Phoenix Flavour\` -- and will be used instead of the default INIs when we launch the game from that profile.

We will now modify those INI files through MO2 with the lovely tool BethINI Pie.

## Tools Folder

Before we can proceed with BethINI Pie, we need to create a folder to install the tool in. This folder will also serve as the directory for most of the tools that we install later on.

### Location

When it comes to picking an installation directory for tools, there are two choices:

1. **Inside the MO2 directory:** `\Mod Organizer 2\Tools\`. While tool authors often warn against running tools from within the MO2 directory, Wabbajack list authors (including myself) have done just that for years with no issues that I am aware of. That being said, keeping tools within your MO2 instance is mostly useful if you want to include them in a Wabbajack list.
2. **Inside a new high-level folder:** `Drive:\Modding Tools\`. I recommend using a centralised, shared folder for every setup that is not supposed to become a Wabbajack list. Advantages include the ability to share tools between setups and even games (Skyrim SE and Fallout 4 share many tools) and easier updating.

The folder must be <u>on the same drive</u> as Mod Organizer 2.

- Create a **Modding Tools** folder in a location of your choosing.

## BethINI Pie

[BethINI Pie](https://www.nexusmods.com/site/mods/631) is a tool for modifying the vanilla INI files: Skyrim.ini, SkyrimPrefs.ini, and (optionally) SkyrimCustom.ini. Its optimised settings are based on extensive testing by DoubleYouC, a member of the STEP team.

The tool can be used for Fallout (NV/4) and Starfield in addition to Skyrim (LE/SE).

- Download the latest main file from the [mod page](https://www.nexusmods.com/site/mods/631?tab=files).
- Create a new folder in your **Modding Tools** folder called `BethINI Pie 4.17`.
  - *Including the version number is optional but highly recommended.*
- Extract the downloaded archive into the new folder.

### MO2 Integration

To detect the profile INIs, BethINI Pie must be run through MO2.

- Click the **gears** icon in the **Toolbar** to open the **Executables** settings.

![MO2 Executables Settings](/Pictures/manual/mo2-executable-settings.png)

- Click the little blue plus icon and select **Add from file**.
- Navigate to `\Modding Tools\BethINI Pie\` and double-click the **BethINI.exe**.
- Click **OK** to add the new executable to MO2.

BethINI Pie should automatically be selected from the executables drop-down.

- Click **Run** to launch BethINI Pie through MO2.

![Run BethINI Pie](/Pictures/manual/setup/ini-config/run-bethini-pie.png)
