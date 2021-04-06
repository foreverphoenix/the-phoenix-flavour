---
title: "Visual Upgrade"
weight: 2
type: docs
description: >
  Additional mods to improve the graphics.
---

## About this section

The main guide has always tried to stay as performance-friendly as possible in its choices of INI settings, mods, ENB, and so forth. Even though I'm lucky enough to own an RTX 3080 now, I wanted to keep base TPF useable for a variety of systems. However, for those with more powerful hardware there are now some additional mods.

There are two sections on this mod page: Grass overhaul (for Folkvangr) and ENB (for Rudy ENB). You can install either, both, or none.

## Grass Overhaul

My personal favourite grass overhaul is Folkvangr nowadays and only the increased performance impact over the TPF default Veydosebrom has kept me from including it in the main guide.

If you choose to install Folkvangr (you can skip it if you like), expect an FPS loss of around 5-10FPS (not noticeable for me since I play capped at 60).

Disable the following mods in your mod order:

- **Trees & Plants:** Veydosebrom Regions
- **Trees & Plants:** Veydosebrom Regions - Fall Forest
- **Trees & Plants:** Cathedral 3D Pine Grass

### **[Folkvangr - Grass and Landscape Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/44899?tab=files)**

An absolutely incredible grass overhaul. Does stray from vanilla quite a bit but I haven't yet found a single place I didn't like. I prefer it over Veydosebrom.

#### Download Instructions

- **Main Files:** Folkvangr - Grass and Landscape Overhaul

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Folkvangr - Grass and Landscape Overhaul.ini`

#### INI Tweak

- Open the **INI Editor** in Mod Organizer 2.
- Switch to the **skyrimcustom.ini** tab.
- Change the following value:

```
iMinGrassSize=60
```

- Click **Save** and close the window.

> Thanks to the MO2 profile-specific INI files option, this change will only apply to the TPF-X profile and not affect the base TPF profile.

## Rudy ENB

At this time, Rudy ENB is probably the most feature-rich and certainly one of the most impressive ENB presets out there. It has a slew of requirements which we will need to cover also.

If you decide to install Rudy ENB, you need to install all other files from this section as well.

### **[Rudy ENB - Weather Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/39113?tab=files)**

#### Download Instructions

- **Main Files:** Rudy ENB Cathedral Weathers required files Part I
- **Main Files:** Rudy ENB Cathedral Weathers required files Part II >> `merge with the main file`

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Cathedral Weathers.ini`

### **[Rudy ENB Files](https://www.nexusmods.com/skyrimspecialedition/mods/39113?tab=files)**

#### Download Instructions

- **Main Files:** Rudy ENB SE for Cathedral Weathers

Download the file manually.

#### Installation Instructions

We will extract the required files from the archive before installing them in ENB Man.

- In Windows Explorer, go to your temp folder: `Your Modding Folder\temp`. It should be empty.
- Open the download Rudy ENB archive.
- Go to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\[ Skyrim SE folder ]`.
- Extract both files and the folder to your temp folder.

These are the base ENB files that may now be overwritten by addons.

- Go to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\ADDONS`.
- Double-click the **Lighting mods** folder and then **Normal Game**.
- Open the **If Luminosity is placed after Window Shadows** folder.
- Extract the **enbseries** folder into your temp folder.
- Click **Yes** when asked to merge folders and replace files.

This installed the ENB code for the night eye fix. The matching plugin-based tweaks will be part of the next mod.

- Open **ENB Man**, the preset management tool installed during the main guide.
- Double-click the **Skyrim SE** profile.
- Click the big arrow under **Presets** and select **Blank Preset**.
- Enter **Rudy ENB for Cathedral Weathers** and click the green checkmark.
- Move the folder and both files from the temp folder into ENB Man.
- Under **Binary**, make sure the latest version is selected and checked.
- Click the green checkmark at the bottom to install the preset.
- If asked to update modified files from your previous preset, click the green checkmark.
- Close ENB Man. Rudy ENB is now installed.

### **[Misc Tweaks - Night Eye Redux - ENB Fix](https://www.nexusmods.com/skyrimspecialedition/mods/38348?tab=files)**

A tiny patch for Night Eye Redux, merging the tint color changes from the ENB night eye fix with the changes from NER. This allows you to use night eye with Rudy ENB.

#### Download Instructions

- **Optional Files:** Misc Tweaks - Night Eye Redux - ENB Fix

### **[Bright Snow Fix for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/41737?tab=files)**

Lowers brightness of the snow flake texture so it's not overblown with ENB. Didn't find this necessary with Serio's ENB but it helps with Rudy.

#### Download Instructions

- **Main Files:** Bright Snow Fix

### **[Dynamic Volumetric Lighting and Sun Shadows](https://www.nexusmods.com/skyrimspecialedition/mods/44483?tab=files)**

Synchronises sun and exterior shadows. This mod is a hard requirement for Rudy ENB.

#### Download Instructions

- **Main Files:** Dynamic Volumetric Lighting and Sun Shadows

### **Rudy ENB - DVLaSS INI**

Rudy comes with its own preset for DLVaSS.

#### Installation Instructions

- In Mod Organizer 2, create a new empty mod: **Rudy ENB - DVLaSS INI**.
- Right-click the new mod and click **Open in Explorer**.
- Open the Rudy ENB archive (with the ENB files) once again.
- Navigate to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\ADDONS`.
- Double-click the **Rudy ENB DVLaSS ini.rar** and open the **Data** folder inside.
- Extract the **SKSE** folder into the mod folder you created before.
- In Mod Organizer 2, press F5 to refresh.

### **DynDOLOD - Generate Terrain Underside**

While there is a terrain underside mesh available on the DLVaSS mod page, it is recommended to use DynDOLOD to generate one for one's setup. This is a new feature in DynDOLOD 3.0 that you need to enable now. DynDOLOD will be regenerated later on.

#### INI Tweak

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\`.
- Open the **DynDOLOD_SSE.ini** in Notepad++.
- Scroll down to **Line 270** and uncomment it (remove the semicolon `;`).
- Scroll down to **Line 275** and change **TerrainUnderside=** to **1**.
- Save and close the file.