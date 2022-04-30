---
title: "Step 6: Skyrim Script Extender"
weight: 6
type: docs
description: >
  Properly installing the Skyrim Script Extender.
---

## Download

SKSE is highly version dependendent so please make sure to download the correct version:

- Download [SKSE64](http://skse.silverlock.org/). You need build **2.1.5** for Skyrim SE `1.6.353`.
- Save the downloaded archive to `\Your Modding Folder\ARCHIVE\Skyrim Script Extender\`.

![SKSE Download](/Pictures/tpf/initial-setup/skse-download.png)

## Installation

Open the downloaded archive and extract the following three files into your **Stock Game** folder:

- **skse64_1_6_353.dll**
- **skse64_loader.exe**
- **skse64_steam_loader.dll**

![SKSE Binaries Installation](/Pictures/tpf/initial-setup/skse-binaries-installation.png)

### SKSE Scripts

While the SKSE binaries belong into the root folder, its scripts can be installed as a mod in Mod Organizer 2.

- Extract the **Data** folder from the SKSE archive to `\Mod Organizer 2\mods\`.
- Rename the folder to **SKSE Scripts**.
- Switch back to Mod Organizer 2.
- Press F5 to refresh and the new mod will show up just below the **UTILITIES** separator.
- Click the checkmark to activate it.

## SKSE INI

Certain settings for SKSE can only be enabled / configured in a custom INI file.

- Navigate to `\Mod Organizer 2\mods\` and create a new **SKSE INI** folder inside.
- Open the new folder and create another folder called **SKSE** within it.
- Inside the **SKSE** folder, right-click and select **New** >> **Text Document**.
- Rename the file to **SKSE.ini** (make sure to change the file extension from TXT to INI).

![Create SKSE INI](/Pictures/tpf/initial-setup/create-skse-ini.png)

### INI Settings

Open your new **SKSE.ini** in your preferred editor and add the following:

```
[Display]
iTintTextureResolution=2048

[General]
ClearInvalidRegistrations=1
```

**Save your changes and close the editor.**

---

**iTintTextureResolution** will allow you to use higher resolution textures for tint masks like war paints, makeup, or dirt overlays. Without this tweak, they would look low res and blurry regardless of the resolution of the installed textures. Anything higher than 2K is unnecessary for anything other than extreme closeups in screenshots.

**ClearInvalidRegistrations** runs automatically after loading a save, cleaning up invalid OnUpdate() registrations to prevent save bloat after removing certain mods. This should not be necessary with TPF, but was included just in case.

## SKSE Launcher

From now on, you always have to launch the game through SKSE for it to work properly.

- Restart Mod Organizer 2.
- The SKSE Launcher executable should have been automatically added to the executables list in MO2.
- Select **SKSE** from the list and click **Run**.

> At this point (and when testing later on) you’ll benefit a lot from having this page open on a secondary monitor or alternatively your phone or tablet in order to avoid having to tab out.

![Run SKSE](/Pictures/tpf/initial-setup/run-skse.png)

### Verify Installation

- Once you are in the Skyrim SE main menu, bring up the console by pressing the tilde key on your keyboard (above TAB, next to 1).
- Type in **skse** and hit Enter. It should return the version number of your SKSE64 installation.
- After confirming that SKSE64 was installed correctly, type **qqq** in the console and hit Enter to quickly close the game.

![Verify SKSE64](/Pictures/tpf/initial-setup/verify-skse64.jpg)

---

#### Continue with the [INI Files](/tpf/initial-setup/step-7/) page.